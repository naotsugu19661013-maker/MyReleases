# Development implementation plan profile

## Responsibility

- **Purpose:** define how approved requirements and designs will be realized, sequenced, verified, integrated, and controlled within an authorized scope.
- **Primary readers:** project owner, technical lead, implementers, reviewers, testers, release or operations stakeholders, and coordinators.
- **Must decide:** implementation scope and exclusions, authoritative design inputs, work breakdown by deliverable or responsibility, dependencies and order, ownership where required, environments and branches where governed, validation and acceptance gates, migration or rollout preparation, risks, rollback or stop conditions, and completion evidence.
- **Must not decide:** new product requirements, user-visible behavior, fundamental architecture, or safety policy that the referenced requirements and designs should own.

## Recommended reading order

1. Objective, authorized scope, exclusions, and governing documents.
2. Current state, assumptions, constraints, and readiness conditions.
3. Implementation strategy and work breakdown.
4. Dependencies, sequence, milestones or phases, and responsibilities.
5. Integration, data migration, compatibility, and environment handling where relevant.
6. Verification approach, gates, acceptance evidence, and user confirmation boundaries.
7. Risks, stop conditions, recovery or rollback approach.
8. Deliverables, completion definition, reporting, and unresolved planning decisions.

## Chapter model

Objective/scope, design inputs, strategy, work items, sequence/dependencies, verification gates, risks, and completion definition are mandatory. Schedule, staffing, environments, migration, rollout, rollback, procurement, and communications are conditional.

Reference requirements and design decisions by stable identifiers or sections; do not duplicate or reinterpret their full specification. Put class or algorithm design in detailed design and test case detail in test specifications.

## Common failures

- Rewriting product behavior inside the plan and creating a second source of truth.
- Listing tasks without dependencies, entry conditions, validation, or completion evidence.
- Treating automated regression, reviewer approval, and real-user or device confirmation as interchangeable.
- Mixing current scope with desirable future work or advancing later phases without authorization.
- Recording the author's working notes and TODOs as formal plan content.

## Completion criteria

The team can execute in a safe order against named authoritative inputs, knows the boundaries and gates, can distinguish each kind of evidence, and can determine completion without the plan redefining the product.
