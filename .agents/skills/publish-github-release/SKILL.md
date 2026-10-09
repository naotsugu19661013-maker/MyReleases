---
name: publish-github-release
description: Publish binary release assets (ZIP, EXE, installers, etc.) to the public GitHub repository MyReleases as a formal GitHub Release. Use when the user requests releasing a new binary package to MyReleases.
---

# GitHub Release パッケージ自動公開スキル (`publish-github-release`)

このスキルは、配布管理リポジトリ `MyReleases` (`C:\MyDev\50_MyReleases`) から、アプリケーションの実行ファイル（ZIPファイル、インストーラー等）を GitHub の公開リポジトリ `MyReleases` へ GitHub Release として正式公開するための標準手順を定義したワークフローです。

---

## 1. 動作の概要

ユーザーから「リリースを実行して」「`X-Cursor_v1.2.0_win-x64_portable.zip` をリリースして」といった要求を受けた際、以下の手順に沿って安全かつ確実にリリースを完了させます。

1. **前提条件・引数の確認**
2. **リポジトリ状態および Public 確認**
3. **配布ファイルの整合性チェック（存在、サイズ、SHA-256算出）**
4. **既存タグ・リリースの重複チェック（衝突防止）**
5. **正式リリースの作成（API/curl使用）および Asset アップロード**
6. **リリース疎通検証および結果報告**

---

## 2. 入力パラメーター（ユーザー指定またはドキュメント参照）

実行にあたり、以下の情報を確認またはユーザーへ問い合わせます。

* **配布対象ファイルパス**: 例 `C:\MyDev\00_APL\X-Cursor\dist\X-Cursor_v1.2.0_win-x64_portable.zip`
* **タグ名**: 例 `x-cursor-v1.2.0`（小文字英数ハイフン推奨）
* **Release タイトル**: 例 `X-Cursor v1.2.0`
* **製品名**: 例 `X-Cursor`
* **説明・仕様の正本ソース**: 例 `C:\MyDev\00_APL\X-Cursor\README.md` または `docs/` 配下のリリース報告書
  * ⚠️ **禁止事項**: 変更内容や仕様を推測して記載しないこと。必ず既存文書のテキストを参照すること。

---

## 3. 実行手順・ガイドライン

### Step 1: リポジトリ状態の確認

1. カレントディレクトリ `C:\MyDev\50_MyReleases` の Git 状態を確認する。
   ```powershell
   git status
   git remote -v
   ```
2. GitHub REST API でリポジトリ `https://api.github.com/repos/naotsugu19661013-maker/MyReleases` を参照し、`visibility` が `public` であることを確認する。
3. リポジトリが空（初回コミットなし）の場合のみ、リポジトリ説明を記載した `README.md` を作成し、コミットおよび push を行う。
   ```powershell
   git branch -M main
   git add README.md
   git commit -m "Initial commit: Add README.md for MyReleases repository"
   git push -u origin main
   ```

### Step 2: 配布ファイルの確認と SHA-256 算出

1. 指定された配布アセットファイルが存在し、ファイル名が完全一致することを確認する。
2. ファイルサイズおよび SHA-256 ハッシュ値を算出する。
   ```powershell
   (Get-Item "<ファイルパス>").Length
   (Get-FileHash "<ファイルパス>" -Algorithm SHA256).Hash
   ```

### Step 3: 既存リリース・タグの衝突防止チェック

GitHub API でタグおよびリリースが存在しないか確認する。
```powershell
Invoke-RestMethod -Uri "https://api.github.com/repos/naotsugu19661013-maker/MyReleases/releases"
Invoke-RestMethod -Uri "https://api.github.com/repos/naotsugu19661013-maker/MyReleases/tags"
```
⚠️ **重要**: 同名タグまたは同一 Release が既に存在する場合は、新規作成や上書きを行わず、その時点で処理を停止して状況をユーザーへ報告すること。

### Step 4: GitHub Release の作成と Asset のアップロード

1. Git Credential Manager から認証トークンを取得する。
   ```powershell
   $token = ("protocol=https`nhost=github.com`n" | git credential fill | Select-String "password=").Line.Split('=')[1]
   ```
2. リリース本文（Release Notes）を作成する。
   * 製品概要、主な機能、動作環境、起動手順（既存ドキュメントから転記）。
   * 算出された SHA-256 ハッシュ値。
   * JSON ペイロード (`release_payload.json`) を UTF-8 で作成。
3. `curl.exe` を使用して GitHub Release（Formal, Draft: false, Prerelease: false）を作成する。
   ```powershell
   $res = curl.exe -s -X POST -H "Authorization: Bearer $token" -H "Accept: application/vnd.github+json" -H "Content-Type: application/json; charset=utf-8" https://api.github.com/repos/naotsugu19661013-maker/MyReleases/releases -d "@release_payload.json" | ConvertFrom-Json
   ```
4. アセットファイル（ZIP / EXE 等）をアップロードする。
   ```powershell
   $uploadUrl = $res.upload_url.Split('{')[0] + "?name=<アセットファイル名>"
   curl.exe -s -X POST -H "Authorization: Bearer $token" -H "Accept: application/vnd.github+json" -H "Content-Type: application/zip" --data-binary "@<ファイルパス>" "$uploadUrl"
   ```

### Step 5: リリース疎通確認および完了報告

1. API により以下を自動検証する：
   * Draft ではなく公開状態（`draft: false`）であること。
   * Prerelease でないこと（`prerelease: false`）。
   * タグ名、Release タイトル、Asset ファイル名、サイズが正しく登録されていること。
   * リポジトリが `Public` であること。
2. アセットのダウンロード URL に対して `curl.exe -I -s -L "<Asset URL>"` を実行し、`HTTP/1.1 200 OK` が返ることを確認する。
3. 以下の項目を簡潔にユーザーへ報告する：
   * GitHub Release 作成結果
   * Release URL
   * タグ名 & Release タイトル
   * 公開ファイル名、ファイルサイズ、SHA-256
   * Public 確認結果
   * 実施したコミット/Pushの有無

---

## 4. 禁止事項

* 対象アプリケーション本体のソースコードや設定を変更しないこと。
* 公開対象ファイルを再生成、再圧縮、改変しないこと。
* 配布ファイルを通常の Git コミットに含めないこと（Release Asset としてのみ登録）。
* 既存の Release やタグを削除または上書きしないこと。
