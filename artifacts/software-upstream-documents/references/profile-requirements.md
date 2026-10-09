# Requirements definition profile

## Responsibility

- **Purpose:** establish an agreed, verifiable statement of what the system or target capability must satisfy and the boundaries within which it must operate.
- **Primary readers:** users or representatives, product and project owners, architects, designers, testers, operations stakeholders, and approvers.
- **Must decide:** stakeholders and actors, scope and exclusions, use contexts, functional requirements, data and external interaction needs at requirement level, non-functional requirements, constraints, acceptance basis, priorities, assumptions, and unresolved requirement decisions.
- **Must not decide:** internal component decomposition, class or method design, detailed algorithms, technology-specific realization unless imposed as an approved constraint, or implementation schedule.

## Recommended reading order

1. Purpose, approval scope, and document relationships.
2. Background, stakeholders, actors, and usage context.
3. Scope, system boundary, assumptions, constraints, and terminology.
4. User goals, scenarios, or business processes.
5. Functional requirements grouped by user or domain capability.
6. Data, external interface, and migration requirements at externally meaningful level.
7. Non-functional and cross-cutting requirements.
8. Acceptance criteria, priority, traceability, unresolved matters, and revision history.

## Chapter model

Purpose/scope, stakeholders, context/boundary, terminology, functional requirements, non-functional requirements, constraints, and acceptance/traceability are mandatory. User journeys, business rules, data, external systems, compliance, migration, and operational requirements are conditional.

Separate solution architecture into overview or basic design, screen details into screen design, low-level contracts into detailed specifications, and execution sequencing into an implementation plan.

## Common failures

- Describing a chosen implementation while omitting the user or business need.
- Using vague qualities such as “fast” or “easy” without a verifiable condition.
- Combining requirements, design proposals, test procedures, and open questions in one list.
- Duplicating the same requirement under several features with subtly different wording.
- Omitting exclusions, actors, error or boundary conditions, and traceability to acceptance.

## Completion criteria

Designers can derive a solution without guessing intended outcomes, testers can identify an acceptance basis, and reviewers can distinguish agreed requirements from assumptions and unresolved choices.
