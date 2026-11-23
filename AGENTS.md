# UI engineering instructions

Use this file as an adapter to the canonical UI standards in `standards/`. The standards are the source of truth; do not create a conflicting parallel set of rules in agent-specific instructions.

## Before changing UI

1. Inspect the repository structure, existing screens, shared components, design tokens, styling approach, and relevant project instructions.
2. Identify the conventions and components already used by the affected area. If context is missing, inspect nearby examples before introducing a new pattern.
3. Make the smallest coherent change that satisfies the request. Preserve unrelated behavior and avoid broad rewrites.

## While implementing

- Reuse or extend existing components and tokens before adding new ones.
- Keep visual decisions consistent with the established design system. Do not introduce arbitrary colors, typography, spacing, borders, or shadows when a token or existing pattern applies.
- Use semantic, accessible markup and support keyboard interaction, visible focus, and appropriate labels.
- Check responsive behavior, including narrow viewports and content growth.
- Account for loading, error, empty, and success states when relevant to the changed flow.
- Follow the project's framework, file organization, styling, naming, and testing conventions. Do not add dependencies or restructure unrelated code without a clear need.

## Before completing

- Compare the change with adjacent screens and components for consistency.
- Review the relevant standards and [`templates/ui-review-checklist.md`](templates/ui-review-checklist.md).
- Run the project checks that are relevant and available, and report what was or was not verified. Do not claim visual validation unless the UI was actually inspected.
- Summarize the change and any material limitations.

## Canonical guidance

Read the applicable documents under `standards/`: architecture, design system, component, styling, accessibility, responsive design, and code quality. Read `ui-integration.md` when the work crosses API, authentication, or frontend-backend boundaries. Examples in `examples/` are illustrative, not mandatory syntax.
