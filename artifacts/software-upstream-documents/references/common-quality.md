# Common quality rules

Apply these rules to every supported document type, within the selected profile's existing responsibility.

## Authoritative-document character

- Center the document on currently valid decisions, requirements, constraints, and safety conditions that it owns. Its purpose is to explain the present specification or policy to the next process and future maintainers.
- Completeness means that the document's required decisions and conditions are covered at the proper level. It does not mean preserving every statement from the inputs.
- Preserve the project's canonical-source and cross-document ownership rules. Keep the current specification in its owning authoritative document, detailed observations in investigation or verification records, change history in change records, and durable decision rationale in the project's decision-record area when one exists. Reference an owning document instead of copying its full content.

## Classify source meanings before drafting

Split mixed paragraphs into meaning-level items before creating or revising the artifact. Distinguish at least the following categories; a source paragraph may contain several. Keep source location, authority/status, owner, and intended disposition in a working inventory. This inventory and its category names are internal authoring aids, not content for the artifact, its metadata, or its revision history, and not a required new deliverable or permanent record.

| Source category | Treatment |
| --- | --- |
| Currently valid decision | State the adopted outcome once at its canonical location. |
| Active requirement, constraint, or safety condition | Preserve its binding meaning, scope, qualifiers, and exceptions. |
| Decision uniquely derivable from established facts or decisions | Synthesize one current statement after checking that no new choice is required. |
| Background or design intent | Keep only a short reason needed to interpret or safely change the decision. |
| Review finding | Apply the correction to wording, names, structure, or relationships; determine whether any substantive decision was actually adopted. |
| Investigation or experiment result | Use as evidence of what was observed, not as an adopted policy or proof beyond its scope. |
| Failure, NG example, or rare case | Find the resulting adopted decision, if any; distinguish an independent constraint from an incidental example. |
| Past specification, retired item, or rejected option | Exclude from current rules unless it still defines an active compatibility, migration, or change-scope condition. Do not resurrect it during consolidation. |
| Undecided or unconfirmed matter | Classify by decision ownership and confirmation status as described below. |
| Downstream elaboration | Describe the bounded handoff under an already established upstream policy. |
| Matter owned by an external canonical document | Reference its owner and relevant contract; do not decide or duplicate its specification here. |

Do not assign raw input paragraphs directly to existing chapters. Determine what each item means and how it bears on current decisions first. Recency or inclusion in review material alone does not establish approval; use the governing authority order and report unresolved conflicts.

## Synthesize decisions, do not transcribe history

- Where discussions or reviews reach a final adopted policy, write that outcome rather than the intermediate debate. Apply editorial review instructions throughout the artifact; a naming correction should produce correct names, not a paragraph explaining the review comment.
- Combine multiple confirmed statements when their scope and conditions uniquely establish one current decision. Preserve relevant qualifiers. Keep enough source mapping in the working inventory to verify the derivation; do not force readers through the derivation history.
- If several reasonable product, requirement, design, or planning choices remain, Codex must not select one, even if one seems preferable. Record the missing decision. An observed failure alone does not establish the replacement policy.
- Do not turn evidence into a generalized requirement without an adopted decision or a unique derivation from confirmed requirements. Do not send an already established decision to the unresolved list merely because it was not written in one sentence.

## Interpret negative information

Distinguish two uses of a prohibition or NG statement:

1. An independently binding safety condition, constraint, or prohibition requirement. Retain it with its applicable scope, even when a positive adopted policy also exists.
2. An old method, review finding, or NG example that is only the inverse of an adopted replacement. State the current adopted policy and, when needed, its short reason; omit redundant negative history when it adds no active condition.

A prohibition can be a complete constraint without being a complete solution. If the document must decide a method, responsibility, behavior, boundary, or plan, statements such as "do not use X" or "do not judge only by Y" do not settle that decision. Look for the adopted alternative; if none is established, record the missing decision and do not mark that part complete.

Write an adopted design rule so readers can first understand what the system, team, or process will do. State the adopted design or policy, then the short reason when it protects correct interpretation, and add a prohibited or avoided approach only when it remains an independent constraint or clarifies a non-obvious boundary. When several negative rules come from past failures, normalize them under the current positive principle instead of reproducing a catalog of incidents or inversions. This ordering rule does not weaken independently binding prohibitions or require every sentence to be rewritten positively.

## Keep necessary intent, bound the evidence

Attach a short rationale when misunderstanding the reason would make a future change likely to break the governing policy. State the decision first and make the reason subordinate. Keep decision and reason distinguishable without requiring separate rationale chapters.

Do not fill the authoritative body with discussion chronology, review replies, individual failures, experiment logs, test-result detail, rejected-option detail, speaker attribution, or explanations of the editing work. Cite or link existing investigation, validation, review, change, or evidence records when the technical basis matters; summarize only the minimum background needed to understand the current rule. When the project has ADRs, decision records, or an equivalent managed area, prefer that owner for durable rationale, rejected alternatives, and reconsideration conditions. Do not create a new record-management scheme merely to satisfy this rule. A proposal may need decision-level alternatives or feasibility context, and a change specification may need a concise problem and evidence statement, as their profiles require. Such material remains context, not a substituted or inferred decision.

## Separate unresolved decisions, confirmation, and handoff

For each gap, first ask whether the profile requires this document to decide it and whether the available authoritative material already settles it. Distinguish:

| Status | What to state |
| --- | --- |
| Additional decision required here | The precise missing choice or conflict, its effect, and the responsible authority or required decision input when known. Do not invent an owner or imply that Codex can approve it. |
| Policy adopted, confirmation still required | The adopted policy separately from the unverified feasibility or condition; identify what remains to be checked and whether it blocks the profile's completion criteria. Do not present adoption as successful verification. |
| Downstream elaboration | The settled upstream policy, the bounded detail to elaborate, and the owning process or document when known. This is not an unresolved upstream decision. |

If a missing decision belongs to an external canonical document, identify that dependency and owner rather than deciding it here. If ownership is unclear, report the boundary uncertainty instead of arbitrarily assigning it downstream.

Reflect the decided portion and clearly separate the remaining matters from binding statements. Do not defer this document's required decisions to a later process, or keep downstream implementation details in its unresolved-decision backlog. At completion, always report newly detected unresolved matters, including explicit confirmation-pending items, or state that none were found. A required decision still open prevents a claim that the affected document is complete; not every bounded downstream detail does.

## Reading order and definitions

- Organize from necessary context and whole-system understanding toward specific decisions. Use the profile as an internal meaning and completion checklist, not a fixed chapter template. Existing structure may be retained or reconstructed according to clarity and project standards.
- When the document is long or structurally complex enough that readers cannot quickly see where major subjects are located, provide a concise table of contents or equivalent section map near the beginning. Show the main structure; do not require deep link trees or every minor heading. Omit navigation when a short, simple document is already easy to scan.
- Define a term when it differs from ordinary usage, needs distinction from a neighboring concept, serves as a consistent formal name, or could change a design or implementation judgment if misunderstood. State enough meaning, scope, and distinguishing conditions for readers to decide whether something belongs to that concept or a neighboring one. The goal is a usable conceptual boundary, not a large glossary; leave ordinary words used normally undefined.
- Introduce necessary definitions before or at first use, inline or in a glossary as appropriate. A profile's mention of terminology does not require a glossary or definitions that the content does not need. Use one formal name per concept and one meaning per term. Define needed abbreviations or aliases and use them consistently; do not alternate synonyms or paraphrases without a naming rule.
- Present the complete set or structure before referring to one numbered member. For example, explain the complete processing flow before discussing a later stage.
- Keep every chapter responsible for one recognizable subject and make transitions logically progressive. When an opening guide is needed, combine it into one concise introduction. Do not stack purpose, scope, contents, and "this chapter explains" paragraphs that preview what the immediately following body already makes clear. Keep drafting notes separate from the authoritative body; retain only guidance needed by the finished document's reader.
- Do not introduce a fundamental policy for the first time near the end or restate the document's purpose as a closing substitute for structure.

## Single source of truth inside the document

- Give each requirement, decision, responsibility, and policy one canonical statement.
- In other locations, describe only a distinct relationship, consequence, or minimal explicit cross-reference. Check meaning across summaries, purposes, scope statements, supplements, and cautions, not merely identical wording. "Prevent misunderstanding", "just in case", or "make it clearer" alone does not justify another equivalent statement; improve the canonical statement if it is unclear.
- Separate functional structure from cross-cutting requirements. Centralize safety, security, privacy, logging, diagnostics, error classification, quality, and similar concerns when they apply across multiple functions.

## Scope and level

- Respect the selected profile's responsibility. Do not put class layouts, method-level algorithms, database implementation details, API field-by-field contracts, or equivalent low-level design into an upstream document unless the item is an externally observable or architecturally binding constraint owned by that document.
- Do not let an implementation plan redefine product behavior, or let a proposal commit to detailed implementation.
- Express downstream handoff as a small set of responsibilities or design areas to elaborate under the settled upstream policy. Do not inventory individual APIs, parameters, fields, candidate fixed values, classes, algorithms, or tasks merely because downstream work must decide them. Retain binding contracts, safety boundaries, open upstream decisions, and other conditions whose loss would permit the downstream design to change current intent.
- Aim for the minimum wording that enables an unambiguous judgment at the document's level, rather than maximum detail or minimum length. Review background, paraphrases, chapter guides, and reassurance for removal when judgment remains possible without them. Preserve contracts, responsibilities, safety conditions, scope, exceptions, boundaries, and necessary intent; added detail must come from authoritative decisions, not create a new specification.

## Audio-first document presentation

Apply this presentation rule to upstream documents created or revised for user confirmation, review, or approval, including their appendices and any comparison, review-finding, or test-result summaries included in them. Present their information through headings and prose that a listener can understand in reading order.

- Do not include diagrams, charts, images, tables, or pseudo-tables. This includes embedded or linked visual substitutes, Mermaid or ASCII diagrams, aligned columns, tab-separated or delimiter-separated rows, and code blocks used to simulate a table or diagram. Visual clarity, compactness, and essential mappings or comparisons do not justify an exception. An image caption or accompanying prose does not make a prohibited visual expression acceptable.
- Replace visual expressions with headings and connected sentences. Numbered or bulleted items may organize the prose when each item states an understandable relationship without depending on alignment, symbols, color, or spatial position. A table of contents may remain a sequential list of section names and links; it must not use a tabular layout.
- Preserve all information required within the document's responsibility. For each comparison, name the subject, comparison criterion, value or outcome, applicable conditions, and exception. For mappings, state both sides and the relationship explicitly. For flows or structures, state the participants, direction, order or dependency, branches, exceptional paths, and completion conditions that the source establishes. Do not infer a processing order from responsibility numbers. Empty cells, merged cells, ditto marks, and legends must be interpreted from the source; preserve distinctions such as not applicable, unknown, and not verified without inventing missing information.
- Use the semantic inventory and content-retention review to verify the conversion against the source, including quantities, units, identifiers, qualifiers, evidence scope, and confirmation status. Where the source leaves a relationship unresolved, report that uncertainty rather than filling it in. Follow the existing decision/evidence ownership rules; conversion does not require importing raw review or test records into an authoritative body.
- This restriction governs the document's presentation. It does not automatically restrict source code, machine-readable data, raw evidence outside the document, or this skill's internal routing, classification, and management information. Internal reference tables and profile criteria are authoring aids, not output layouts. A template or source visual must be converted when used in an in-scope document; a reference to an owning canonical document may remain, but it must not make understanding the current document depend on viewing a figure or table.
- A governing project format that mandates a prohibited visual expression is a conflict to report under the existing authority rules. Do not silently retain the visual expression, invent an exception, or claim that the affected document has passed the completion gate.

## Prose and presentation

- State ordinary specifications, responsibilities, behavior, and judgments affirmatively, with the conclusion first.
- Explain what the subject does or is before describing exclusions, exceptions, or prohibitions. When both intended behavior and its boundary are required, state the behavior first and the boundary in a separate sentence.
- Reserve negative or prohibitive wording for exceptions, exclusions, boundary conditions, and independently binding prohibitions whose meaning requires it. Preserve the full force of critical prohibition contracts.
- Define normal responsibilities through their intended actions and outcomes. A list of things a subject does not do is insufficient to define its normal responsibility.
- Give each sentence one main meaning. Separate premises, conclusions, rationale, and boundaries when combining them would obscure their relationship in sequential listening.
- Make a sentence's direction clear at the beginning. Avoid a long sequence of premises whose overall meaning is reversed by a negation at the end.
- Base specification, adoption, and completion judgments on defined conditions. Qualifiers such as `safe`, `appropriate`, `as needed`, `where possible`, `useful`, and `relevant`, including equivalents in other languages, require defined conditions when they determine such judgments.
- Define the judgment conditions for a necessary ambiguous concept, or explicitly reference the canonical document and section that owns those conditions. These words remain usable in context when they do not serve as undefined decision criteria.
- Use a complete enumeration or an explicit scope definition when omitted members would change a specification, responsibility, or acceptance condition. In those cases, avoid open-ended expressions such as `etc.` or `等`.
- Explain concepts, relationships, and reasoning in prose. Apply [audio-first document presentation](#audio-first-document-presentation) when organizing requirements, conditions, procedures, mappings, and comparisons.
- Avoid endless bullet chains, chapters with unrelated responsibilities, and wording that sounds pasted from successive reviews.
- Use natural professional language for the document's domain and audience. Do not mechanically translate internal English concepts or force profile labels into headings. English, Japanese, or established loanwords may be used when they are clearer in context.
- Keep authoring machinery out of the artifact: profile and workflow names, source-classification labels, semantic inventory, checklist names, skill names, and completion-process commentary normally belong only in the work report.
- Use names that identify the referent. Broad words such as `target`, `processing`, `information`, or `state` (including `対象`, `処理`, `情報`, and `状態`) need qualification when several referents are plausible, such as `input data`, `supported environment`, `user`, or `processing result`. Ordinary contextual use remains valid when its meaning is unambiguous.
- Use a concrete name or explicit canonical section reference when `this section`, `above`, `as follows`, or `previously described` (including `本節`, `上記`, `以下のとおり`, and `前述`) would force readers to search or guess. Make the local subject and applicable contract or exception understandable, using the necessary relationship and a precise reference rather than repeating the full rule.
- Evaluate comprehension when a screen reader or text-to-speech reads from top to bottom. A listener must be able to follow the structure, subject, conclusion, conditions, and logical relationships in order without relying on visual position. Repeated explanations and unexplained forward references are defects even when technically accurate.

## Semantic and sequential-reading self-review

Before completing a new or revised document or presenting it for confirmation, review, or approval, inspect the entire output, including appendices, embedded content, and linked visual substitutes, against [audio-first document presentation](#audio-first-document-presentation). Confirm that no prohibited visual expression remains. Then read it from beginning to end as a new listener, using only the headings and spoken text, and check:

- Is the same meaning repeated in different words rather than adding a distinct decision, condition, or relationship?
- Does any term carry multiple meanings, or any concept appear under multiple names without a defined naming rule?
- Can necessary definitions distinguish each concept from its neighbors?
- Does any broad name or contextual pointer require the reader to guess or search before its meaning is clear?
- Does every converted comparison, mapping, flow, or structure retain the source information and explicit relationships, including conditions, exceptions, quantities, and evidence or confirmation status, without relying on a visual layout or a separate visual artifact?
- Do explanations and transitions connect naturally from top to bottom, including chapter openings and first uses of terms?
- Can expendable explanation be removed while preserving every binding contract, responsibility boundary, condition, and exception?
- Has elaboration introduced a specification or choice unsupported by authoritative sources?

Correct detected defects within the authorized scope and source authority, then repeat the affected checks before completion. If a defect or format conflict cannot be resolved, report the affected content and reason and do not claim that the document is complete or ready for approval. This gate requires both absence of prohibited visual expressions and meaning-level sequential comprehension; a syntax scan or word-count check alone cannot establish a pass.

## Current-decision audit

For every major chapter or item, check:

- What currently valid decision, requirement, or condition does it establish within this document's responsibility? If it is context, intent, or a reference, is its supporting role necessary and clear?
- Is any discussion, review finding, investigation result, failure example, or rejected option being treated as a decision without authority?
- Does any design rule end with only a negative statement or prohibition where the document must state an adopted method or policy? Is the adopted direction and, when needed, its reason understandable while independently binding prohibitions remain preserved?
- Have uniquely established decisions been synthesized instead of unnecessarily marked unresolved? Has any choice unsupported by the sources been invented?
- Has a required upstream decision been deferred, or a downstream detail been misclassified as an unresolved upstream choice?
- Do the current decisions remain more prominent than their history, and is retained rationale short and useful? Has a rationale section become a replay of investigation reports, validation results, review records, or work logs?
- Are the authoritative document, evidence records, decision records, change records, and externally owned documents performing distinct roles, with references instead of unnecessary duplication?
- Does the body or revision history contain authoring process, profile/workflow/check names, semantic-inventory language, skill names, or other internal terminology that the product or project does not need?
- Does any chapter or explanation exist only to mirror profile fields or fill a template? Are headings and audience terms natural for this document, and are ordinary terms left undefined when no special meaning exists?
- If the document is long or structurally complex, can readers see and navigate its major structure near the beginning? If it is short, has unnecessary navigation or structure been avoided?
- Is downstream handoff grouped by responsibility or design area rather than expanded into an excessive technical-item inventory, while binding contracts, safety conditions, and genuine unresolved matters remain visible?
- Can the current artifact be understood without past versions or input discussions, using only necessary references to other canonical documents?

Resolve defects before claiming completion. When source limitations prevent resolution, report the decided portion and the specific remaining gap; do not label the document complete.
