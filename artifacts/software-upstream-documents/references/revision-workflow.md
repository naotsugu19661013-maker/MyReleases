# Revision and quality workflow

Use this reference whenever an existing authoritative document is revised or audited.

## Semantic inventory before editing

Apply the full meaning-level classification in [common-quality.md](common-quality.md) to the current document and every supplied review, investigation, or change input before editing. Do not use paragraphs or old chapter numbers as the unit of truth. Include existing defined concepts, acceptance conditions, scope qualifiers, and exceptions so their active meaning is not lost.

For each relevant item, record its source and authority/status, classification, responsibility owner, and intended disposition: `retain`, `consolidate`, `synthesize from confirmed items`, `move`, `apply editorial correction`, `replace by adopted decision`, `external reference`, `separate unresolved/confirmation/handoff`, or `omit with reason`. Record approved or uniquely derived outcomes separately from the comments or evidence that led to them. This working inventory does not require a new permanent document, and its labels or production process must not leak into the artifact or revision history.

## Reconstruct, then write

1. Resolve duplicate meanings and containment relationships. Apply the concept-boundary and formal-name rules in [common-quality.md](common-quality.md#reading-order-and-definitions) before rewriting names; preserve distinct concepts instead of merging them merely because their wording is similar. Resolve contradictions only through the governing authority or uniquely established decisions; retain unresolved conflicts explicitly.
2. Confirm the selected profile's responsibility. Extract the current decisions and independent requirements/constraints, synthesize uniquely derivable decisions, and classify remaining gaps using common-quality. Do not interpret NG evidence as a chosen alternative.
3. Retain or reconstruct the reading order from the actual current content, existing canonical structure, and project standard. Use profile fields as internal criteria, not corresponding chapter headings. Add concise major-section navigation when the document's scale requires it; do not force navigation on a short document.
4. Assign active meanings to canonical destinations. Keep the current specification in the authoritative document, refer to existing evidence and decision records for their owned detail, and attach only necessary short intent. Keep historical input out of the current specification unless it still serves the document's responsibility.
5. Rewrite affected content as the current valid state. Convert existing or template-provided visual expressions under [audio-first document presentation](common-quality.md#audio-first-document-presentation), preserving their information and relationships through headings and prose. Apply review corrections to names, wording, structure, and relationships throughout the artifact; do not accumulate review explanations, append a response history, expose authoring labels, or merely turn negative sentences positive.
6. Separate additional decisions required here, adopted policies awaiting confirmation, and bounded downstream elaboration. Express handoff by responsibility or design area, retain the contracts and safety conditions that protect upstream intent, and identify which unresolved matters block completion.

## Structural review

Read the revised document alone, from the beginning, and answer all of these:

First run the chapter/item-level current-decision audit in common-quality. Then check structure:

- Can the intended reader understand every term at first use?
- Are any later stages, chapters, or concepts referenced before the whole structure is introduced?
- Is the overall structure visible early enough?
- Does detail appear before purpose, context, or the whole-system view?
- Is any decision redefined in more than one place?
- Are decisions, necessary rationale, and evidence indistinguishable in authority or status?
- Are confirmed specifications mixed with future work, author TODOs, feelings, or review replies?
- Does a fundamental policy first appear near the end?
- Is the purpose or positioning unnecessarily re-explained at the end?
- Does editing or review-history prose obscure the current specification? Existing project-mandated metadata/history does not justify putting discussion transcripts in the body.
- For a long or structurally complex document, is concise major-section navigation available near the beginning? For a short document, has unnecessary navigation been avoided?
- Have profile names, workflow names, semantic-inventory terms, check names, skill names, and other authoring labels been kept out of the body and revision history unless the project itself requires them?
- Are headings, audience descriptions, and technical terms natural for this document rather than mechanical translations of internal labels?
- Is downstream handoff concise and responsibility-based rather than a long inventory of APIs, parameters, fields, fixed values, classes, or implementation tasks?
- Does any chapter require readers to jump ahead or know the previous version?
- Would reading aloud expose repeated explanations or long undifferentiated bullet sequences?

Run the [semantic and sequential-reading self-review](common-quality.md#semantic-and-sequential-reading-self-review), then check the existing prose conditions against [common-quality.md](common-quality.md#prose-and-presentation):

- Are normal behavior, responsibilities, and judgments stated affirmatively with the conclusion first, before exclusions or prohibitions?
- When both intended behavior and its boundary are required, is the behavior stated first and the boundary in a separate sentence?
- Is each sentence's direction clear from the beginning, without an end-of-sentence negation reversing a long preceding explanation?
- Is negative or prohibitive wording limited to necessary exceptions, exclusions, boundaries, or independently binding prohibitions, with critical contracts fully preserved?
- Are specification, adoption, and completion judgments based on defined conditions or an explicit reference to their canonical document and section? Could an undefined qualifier lead agents or implementers to different specification judgments?
- Are enumerations complete or their scope explicit wherever omitted members would change the specification, responsibility, or acceptance condition?
- Does each sentence carry one main meaning, with logical relationships understandable during sequential read-aloud listening?

Any answer that exposes a defect requires correction; if the source material cannot resolve it, report the limitation and do not claim the affected document is complete.

## Content-retention review

Compare the new document with the semantic inventory, not just line diffs.

- Verify that every active prior decision, requirement, independent safety condition/prohibition, and defined boundary is present or has an authorized disposition. Content retention is retention of valid meaning, not every input statement.
- For omitted text, explain the semantic reason: redundant meaning consolidated, moved, external ownership, obsolete or replaced by an adopted decision, historical review/evidence not needed to explain the current rule, or unnecessary ordinary-term definition. Do not use these reasons to discard an active condition or necessary intent.
- Treat merged equivalent statements as retained, but verify that qualifiers and exceptions survived consolidation.
- Check new and old meanings in both directions: no unintended loss, unsupported new choice, or accidental resurrection of obsolete behavior. Verify each synthesized decision against its confirmed premises.
- Record unresolved conflicts instead of silently normalizing them.

## Completion evidence

Report:

- selected document profile and why;
- governing standards and canonical sources consulted;
- major structural changes;
- retention result, including any approved removals or unresolved conflicts;
- newly detected unresolved decisions, confirmation-pending matters, and bounded downstream handoff, distinguished by responsibility; explicitly state when none were detected;
- current-decision audit result, including any missing adopted policy or other completion blocker;
- structural-review result, including navigation, artifact-language, internal-term leakage, and downstream-handoff checks, plus the [semantic and sequential-reading gate](common-quality.md#semantic-and-sequential-reading-self-review) result for visual-expression absence, conversion retention, and listening comprehension;
- profile-specific completion result;
- document-management conflicts or needs left for separate consideration, without introducing a new management scheme;
- files changed and files intentionally left unchanged.
