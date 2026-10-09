# High-level design profile

## Responsibility

- **Purpose:** establish the broad solution shape, system boundary, major responsibilities, external relationships, and governing design approach before functional basic design is elaborated.
- **Primary readers:** project owners, architects, lead developers, operations and security stakeholders, and reviewers responsible for solution viability.
- **Must decide:** context and boundaries, major subsystems or service areas, responsibility allocation, principal information and control flows, external interfaces at conceptual level, deployment or operating context where relevant, major technology or architecture constraints, and cross-cutting direction.
- **Must not decide:** class structure, method algorithms, field-by-field API schemas, detailed screen states, database physical design, or sprint/task scheduling.

## Recommended reading order

1. Purpose, scope, requirements basis, and design goals.
2. System context, actors, external systems, and boundary.
3. Overall solution concept and architecture view.
4. Major components and their responsibilities.
5. Principal information, control, and lifecycle flows.
6. External relationships and operating/deployment view.
7. Cross-cutting architecture decisions and quality implications.
8. Constraints, rationale, risks, unresolved architecture matters, and downstream document ownership.

## Chapter model

Purpose/scope, context, whole architecture, major responsibilities, key flows, cross-cutting direction, and downstream ownership are mandatory. Deployment, data domains, external integration, migration, security zones, alternatives, and architecture decision references are conditional.

Separate functional behavior and detailed responsibility rules into basic design, user-visible interaction into screen design, and implementation mechanics into detailed design or implementation plans.

## Common failures

- Listing technologies without explaining the system structure they support.
- Starting with individual components before showing system context and the whole architecture.
- Duplicating requirements rather than showing how the architecture satisfies them.
- Using a high-level diagram as a substitute for responsibility and flow explanations.
- Drifting into class, endpoint, table, or algorithm specifications.

## Completion criteria

Readers share one coherent model of the system boundary, major parts, responsibility allocation, principal flows, constraints, and the design areas owned by later documents.
