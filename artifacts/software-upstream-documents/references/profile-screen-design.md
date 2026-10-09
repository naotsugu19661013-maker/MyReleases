# Screen design profile

## Responsibility

- **Purpose:** establish user-visible screens, information hierarchy, navigation, interaction, states, feedback, accessibility, and responsive or platform behavior required to realize approved user requirements.
- **Primary readers:** users or representatives, product owners, UX/UI designers, developers, testers, accessibility reviewers, and approvers.
- **Must decide:** screen inventory and roles, entry and exit paths, layout regions and information priority, controls and user actions, navigation, normal/empty/loading/error/disabled states, validation and feedback, keyboard and assistive-technology behavior, focus order, display adaptation, and traceability to user requirements.
- **Must not decide:** internal class design, business rules not owned by the UI, server algorithms, implementation task schedule, or visual styling choices unsupported by product requirements or design standards.

## Recommended reading order

1. Purpose, users, platforms, scope, requirements basis, and applicable UI/accessibility standards.
2. Interaction principles, terminology, and global navigation model.
3. Screen inventory and transition overview.
4. Each screen's purpose, entry conditions, information hierarchy, controls, actions, and exit behavior.
5. Shared states, validation, feedback, dialogs, notifications, and failure recovery.
6. Keyboard, focus, screen reader, contrast, scaling, responsive, and platform adaptation requirements.
7. Content rules, permissions or role variants, unresolved matters, and references.

## Chapter model

Purpose/scope, users/platforms, standards, screen inventory, navigation, screen specifications, state/feedback behavior, and accessibility are mandatory. Responsive behavior, roles/permissions, localization, content rules, prototypes, telemetry, and migration from an existing UI are conditional.

Separate business requirements into requirements definition, non-visual system behavior into basic design, reusable visual tokens into the governing design system, and control implementation details into detailed design.

## Common failures

- Providing only static happy-path screenshots with no state, navigation, keyboard, or error behavior.
- Describing screens independently without first showing the inventory and transition model.
- Repeating global interaction and accessibility rules under every screen.
- Letting placeholder copy or mockup artifacts become accidental requirements.
- Using visual polish to hide missing functional decisions or acceptance behavior.

## Completion criteria

A reviewer can traverse every intended user path and state; an implementer can build the visible behavior without inventing navigation or accessibility policy; and a tester can derive observable checks while business and internal implementation rules remain owned elsewhere.
