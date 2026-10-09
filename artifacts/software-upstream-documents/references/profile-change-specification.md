# Change or correction specification profile

## Responsibility

- **Purpose:** define one bounded change or correction, including its reason, desired behavior, affected scope, compatibility and risk constraints, acceptance basis, and required reflection into canonical documents.
- **Primary readers:** requester, product or project owner, designers, implementers, testers, maintainers, and approvers for the change.
- **Must decide:** current problem or change need, target outcome, in-scope and out-of-scope behavior, affected users/components/interfaces/data/documents, new or changed requirements, preserved behavior, safety and compatibility constraints, acceptance conditions, implementation and verification boundaries, and canonical-document updates required at completion.
- **Must not decide:** unrelated product redesign, complete restatement of unchanged system specifications, low-level algorithms unless the document is explicitly extended under a governing standard, or post-change current truth that belongs in the main canonical design.

## Recommended reading order

1. Change identity, status, purpose, authority, and related canonical documents.
2. Current behavior or problem and evidence, clearly distinguished from the desired specification.
3. Change goals, scope, exclusions, assumptions, and preserved behavior.
4. Changed requirements and externally or architecturally significant design decisions.
5. Impact analysis across users, functions, data, interfaces, operations, security, compatibility, tests, and documents.
6. Acceptance criteria and verification boundaries.
7. Implementation constraints, rollout or migration, risk and stop conditions where relevant.
8. Unresolved matters, completion conditions, canonical-document reflection, and revision history.

## Chapter model

Identity/status, reason, scope/exclusions, changed behavior, preserved behavior, impact, acceptance, and canonical-document reflection are mandatory. Root-cause evidence, alternatives, migration, compatibility, rollout, rollback, security/privacy, and device confirmation are conditional.

Keep investigation logs and raw evidence in a referenced investigation record when they would obscure the specification. After completion, integrate the resulting current specification into its owning requirements or design document; retain the change specification as change history according to project rules.

## Common failures

- Treating an incident chronology or review discussion as the specification.
- Copying the entire basic design and creating a competing current source of truth.
- Describing only the new behavior while omitting preserved behavior, exclusions, compatibility, or impact.
- Declaring completion from implementation alone without required tests, user/device evidence, or canonical-document reflection.
- Allowing one correction to expand into unrelated cleanup or redesign.

## Completion criteria

Reviewers can approve a bounded and testable delta; implementers know what changes and what must remain; impacts and evidence gates are explicit; and the owning canonical documents to update at completion are identified without duplicating them wholesale.
