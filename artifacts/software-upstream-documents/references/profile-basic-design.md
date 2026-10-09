# Basic design profile

## Responsibility

- **Purpose:** determine what the system or target function realizes and through what responsibility structure and externally meaningful behavior, without entering implementation-detail design.
- **Primary readers:** project and product owners, designers, implementers, testers, maintainers, and reviewers who must confirm the functional design.
- **Must decide:** functional boundaries, whole functional structure, components or processing stages and their responsibilities, inputs/outputs and contracts at design level, principal states and flows, error or result categories, cross-cutting requirements, safety boundaries, and the rules that detailed design must elaborate without changing basic intent.
- **Must not decide:** class or method decomposition, line-level algorithms, framework-specific selector or query formulas, physical database implementation, field-by-field private APIs, coding tasks, or other implementation mechanics unless they are externally or architecturally binding.

## Recommended reading order

1. Purpose, target readers, scope, related canonical documents, assumptions, and terminology.
2. Design goals, governing principles, and system or feature boundary.
3. Whole functional structure: all subsystems, blocks, or processing stages and their relationships.
4. Canonical responsibility and contract of each structural element, in flow order where applicable.
5. Principal end-to-end flows, states, results, and exceptional paths.
6. Cross-cutting requirements such as safety, security, privacy, logging, diagnostics, error classification, performance, and operability.
7. External and internal boundary conditions at basic-design level.
8. Necessary design intent and references to evidence or decision records, separated from the binding design.
9. Unresolved decisions and concise detailed-design handoff grouped by design responsibility.
10. Traceability, references, and revision history.

## Chapter model

Purpose/scope, terms, principles/boundary, whole structure, canonical responsibility definitions, key flows/results, cross-cutting requirements, and downstream handoff are mandatory. State models, data concepts, interfaces, security/privacy, diagnostics, performance, compatibility, migration, alternatives, short rationale, and evidence or decision-record references are conditional.

When stages or numbered processes exist, introduce the complete set and the end-to-end relationship before first use of an individual stage number. Define each stage's formal responsibility once. Later chapters may state only cross-stage relationships or cross-cutting constraints.

Separate screen-specific appearance and interaction into screen design; low-level algorithms, class structures, and concrete technology mechanics into detailed design; task sequencing into the implementation plan; and incident or application-specific observations into referenced investigation, validation, change, or decision records.

## Common failures

- Referring to a later numbered stage in terminology or principles before explaining the complete process.
- Repeating the same design principle in stage descriptions, cross-cutting requirements, confirmed decisions, and handoff sections.
- Mixing binding design, investigation evidence, detailed-design tasks, and development management in the document's latter half.
- Keeping an inherited chapter order and appending each review response, producing a patchwork document.
- Treating cross-cutting safety, logging, diagnostics, confidentiality, or outcome rules as repeated local notes in every stage.
- Turning detailed-design handoff into a long inventory of APIs, parameters, fields, fixed values, algorithms, or test items instead of naming the responsibilities to elaborate under the basic design.
- Deferring a fundamental responsibility, boundary, or behavior so that detailed design must invent the basic design.

## Completion criteria

A new reader understands the whole responsibility structure before its details; each responsibility and policy has one canonical location; cross-cutting concerns are coherent; rationale and handoff are distinct; and detailed-design authors can elaborate implementation rules without deciding the fundamental behavior or safety boundaries anew.
