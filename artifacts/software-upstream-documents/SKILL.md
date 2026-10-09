---
name: software-upstream-documents
description: Create, revise, or audit authoritative upstream software documents by extracting and organizing currently valid decisions from source materials. Covers proposals, requirements, high-level designs, basic designs, screen designs, implementation plans, and change specifications; excludes detailed design, API or class specifications, test specifications, manuals, minutes, and proofreading alone.
---

# Software Upstream Documents

Maintain an authoritative document that states the currently valid decisions within its responsibility, so the next process and future maintainers can understand the present specification or policy. Source materials are inputs to interpret, not text to transfer wholesale. Discussions, reviews, investigations, experiments, and work history do not become binding decisions merely by appearing in an input.

## Start with governing context

Before creating, revising, or auditing:

1. Locate and read applicable `AGENTS.md`, the latest approved source documents, the project document-management standard, and the document index or canonical-document guidance.
2. Identify the requested document type, target readers, approval purpose, scope, canonical sources, related documents, and permitted output path. Do not invent a storage or versioning scheme.
3. Resolve conflicts by the project's stated authority order. Report an unresolved authority conflict instead of silently choosing.
4. Read [references/common-quality.md](references/common-quality.md) and apply its source classification, decision synthesis, unresolved-matter rules, [audio-first document presentation](references/common-quality.md#audio-first-document-presentation), and final audit to every profile.
5. Select exactly one primary profile from the routing table below and read it completely. If a deliverable genuinely combines roles, keep one primary responsibility and explicitly separate or reference the secondary responsibility; do not merge profile chapter structures mechanically.
6. For an existing document revision or audit, also read [references/revision-workflow.md](references/revision-workflow.md). Apply its content-retention review only when a prior version or other authoritative comparison source is available.

## Profile routing

Choose by the decision the document must enable, not merely by its current filename.

| Requested or actual responsibility | Required profile |
| --- | --- |
| Decide whether and why to undertake a product or initiative | [Proposal](references/profile-proposal.md) |
| Agree what the system must satisfy and its boundaries | [Requirements definition](references/profile-requirements.md) |
| Establish the solution's broad shape and external relationships | [High-level design](references/profile-high-level-design.md) |
| Fix functional responsibilities and system behavior without implementation-detail design | [Basic design](references/profile-basic-design.md) |
| Fix user-visible screens, states, navigation, interaction, and accessibility behavior | [Screen design](references/profile-screen-design.md) |
| Plan how approved requirements and designs will be implemented and verified | [Development implementation plan](references/profile-implementation-plan.md) |
| Define one bounded change or correction, its impact, acceptance, and canonical-document reflection | [Change or correction specification](references/profile-change-specification.md) |

If the title and actual responsibility disagree, state the mismatch and use the responsibility that the user or governing standard confirms. Do not route detailed designs, class designs, API-level specifications, test specifications, user manuals, or meeting minutes into these profiles.

`Responsibility`, `Primary readers`, `Recommended reading order`, `Chapter model`, and `Completion criteria` are internal authoring and evaluation criteria, not an output template. They identify required meanings and completion conditions; they do not require matching headings, a chapter per listed item, a target-readers chapter, or a glossary. Do not expose profile names, workflow names, semantic-inventory terminology, check names, this skill's name, or other authoring labels in the artifact or revision history unless the project itself uses that term. Choose natural professional headings and vocabulary for the document and its domain; an audience concept may be omitted as a heading or expressed naturally as `Primary audience`, `Primary readers`, `Audience`, `利用対象`, `関係者`, or another suitable term. Do not mechanically translate or transliterate an internal English label. Choose structure from the document's responsibility, actual subject, existing canonical structure, project standard, and the order that best explains the current decisions. Keep every profile's responsibility boundary unchanged.

## Authoring workflow

### New document

1. Before drafting, classify source material into meaning-level items using the complete classification in common-quality. Identify the source, current authority/status, responsibility owner, and intended use of each relevant item. Do not paste input paragraphs directly into document chapters.
2. Extract adopted decisions and active requirements, constraints, and safety conditions. Combine confirmed items when they uniquely determine one current decision; do not invent product, requirement, design, or planning choices when multiple valid options remain.
3. Separate this document's unresolved decisions, adopted policies awaiting confirmation, downstream elaboration, and matters owned by external canonical documents. Continue with the decided portion.
4. Design the reading path and canonical location of each decision from the selected profile's responsibility and actual content. For a document whose scale makes the whole structure hard to scan, include a concise table of contents or equivalent navigation to the major sections; do not force one on a short document or enumerate every minor heading. Apply review findings as edits to the artifact, rather than adding the review's explanation.
5. Draft the current state, with only the short rationale needed to protect its meaning. Keep unresolved matters and handoff distinguishable from binding decisions.

### Existing document

Do not begin by patching old chapter numbers or appending review comments. Follow the semantic inventory and reconstruction process in [references/revision-workflow.md](references/revision-workflow.md). Preserve meaning, not obsolete prose or structure.

### Audit only

When the user asks to review or audit a document without explicitly asking for revision, treat the work as read-only. Do not change the target document, its metadata, or related documents. Report proposed corrections separately and wait for an explicit revision request before applying them.

Evaluate the document against [references/common-quality.md](references/common-quality.md), the selected document profile, and the structural-review criteria in [references/revision-workflow.md](references/revision-workflow.md). Use the content-retention review when a prior version, requirement inventory, or other authoritative comparison source is available; otherwise state that content retention could not be determined and why.

The audit report must distinguish observed evidence from interpretation and include:

- the selected document profile and why it applies;
- major issues that prevent reliable use as an authoritative document;
- improvement issues that are important but do not invalidate the document by themselves;
- the location and rationale supporting each finding;
- structural issues;
- content-retention issues or an explicit not-assessed result;
- conformance with the selected profile's completion criteria;
- an overall judgment, including any unresolved uncertainty.

Do not include a rewritten document, patch, or edited file merely because the request says “review” or “audit.”

## Required final review

Before presenting a created or revised document:

1. Run the current-decision audit in common-quality for every major chapter or item, then the structural review and, for revisions, the content-retention review in [references/revision-workflow.md](references/revision-workflow.md).
2. Confirm the selected profile's completion criteria and the prose and read-aloud quality rules in [references/common-quality.md](references/common-quality.md#prose-and-presentation). Pass its [semantic and sequential-reading self-review](references/common-quality.md#semantic-and-sequential-reading-self-review), including the visual-expression and meaning-retention gate, for both new documents and revisions before claiming completion or presenting them for confirmation, review, or approval.
3. Confirm that active requirements and decisions have one canonical statement and that intentional removals or moves preserve current meaning. Completeness does not mean retaining every input statement.
4. Read the output from beginning to end as a new target reader, without past versions or input discussions. Necessary terms, stages, components, and cross-references must be understandable when first encountered; the overall structure must be easy to navigate at the document's actual scale. Do not add dictionary definitions of ordinary terms.
5. Check applicable file naming, metadata, canonical-document, revision-history, index, and storage rules from the project standard.
6. Report the selected profile, authoritative inputs, material reorganizations, newly detected unresolved matters (or explicitly none), their responsibility and confirmation status, retention-check result, and validation performed. Report out-of-scope document-management issues separately. Do not claim completion while the final audit has unresolved defects, or approval that the user or responsible authority has not given.

Before presenting an audit, confirm that every audit-report item above is addressed, every finding has document evidence, unavailable retention evidence is identified, and no target file was changed.

## Boundaries

- Preserve confirmed requirements, prohibitions, safety conditions, and user decisions while consolidating redundant prose.
- Do not turn one product's incident, application name, component name, or process count into a universal template rule.
- Codex is not the final decision-maker. Do not invent missing product, requirement, design, or planning decisions or conceal them as assumptions. Equally, do not mark a uniquely established decision as unresolved merely because it must be synthesized from several sources.
- Keep downstream handoff concise and group it by responsibility or design area. Do not turn it into a field-by-field, parameter-by-parameter, fixed-value, API, class, or implementation-task inventory. Preserve safety conditions, unresolved matters, binding contracts, and other information whose omission would let downstream work change the upstream intent. A basic design is incomplete if detailed-design authors must invent its fundamental behavior or boundaries.
- Follow existing document-management rules without creating or changing Git, filename/version, commit/tag, paired-record, storage, archive, or project-wide documentation schemes. Report conflicts or missing governance separately; do not create new document types or folders to solve them.
- Do not modify related source code, deployments, versions, or unrelated documents unless separately requested.
