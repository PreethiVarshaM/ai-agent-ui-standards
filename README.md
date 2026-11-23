# AI Agent UI Standards

A reusable, framework-agnostic UI engineering baseline for AI coding agents and the developers who work with them. Use it to build consistent, accessible, maintainable, and scalable frontend applications.

The standards are the source of truth. Agent-specific instruction files are adapters that point to them; they should not fork or redefine the guidance.

## Use this resource

1. Copy or vendor this repository into your project, or link to it from your agent instructions.
2. Add the contents of [`AGENTS.md`](AGENTS.md) to the instruction path your agent reads. Keep the canonical standards available in the repository.
3. Read the project UI baseline template in [`templates/project-ui-baseline.md`](templates/project-ui-baseline.md), fill it in with project-specific conventions, and place it where your team maintains project instructions.
4. Ask the agent to inspect the existing UI before changing it, then implement the requested change against these standards.
5. Review the result with [`templates/ui-review-checklist.md`](templates/ui-review-checklist.md).

This resource does not require a particular framework, CSS method, component library, build tool, or AI agent. Existing project conventions take precedence when they are deliberate and compatible with the requested work.

## Standards

- [Architecture](standards/architecture.md): inspect first, preserve boundaries, and make the smallest coherent change.
- [Design system](standards/design-system.md): centralize and reuse design decisions.
- [Component guidelines](standards/component-guidelines.md): build focused, reusable components with clear APIs.
- [Styling guidelines](standards/styling-guidelines.md): follow project styling conventions and avoid arbitrary values.
- [Accessibility](standards/accessibility.md): support semantic, keyboard, and assistive-technology use.
- [Responsive design](standards/responsive-design.md): adapt content and interactions to available space and input modes.
- [Code quality](standards/code-quality.md): keep UI code understandable, consistent, and maintainable.
- [Optional UI integration](standards/ui-integration.md): coordinate frontend work with APIs, authentication, and service boundaries.

## Examples and templates

- [SCSS design tokens](examples/design-tokens.example.scss)
- [CSS design tokens](examples/design-tokens.example.css)
- [Component structure](examples/component-structure.example.md)
- [UI review checklist](templates/ui-review-checklist.md)
- [Project UI baseline](templates/project-ui-baseline.md)

Examples illustrate possible implementations. Adapt their syntax and values to the project's stack; they are not framework requirements.

## Agent adapters

Use the smallest adapter the agent needs. Keep project-specific choices in the project baseline and keep the detailed, reusable guidance in `standards/`.

| Agent | Adapter location | Suggested setup |
| --- | --- | --- |
| Claude Code | `CLAUDE.md` or project instructions | Add a short pointer to `AGENTS.md` and the relevant standards. |
| Cursor | `.cursor/rules/` | Add a rule that references `AGENTS.md` and the relevant standards. |
| GitHub Copilot | `.github/copilot-instructions.md` | Add a pointer to `AGENTS.md` and applicable standards. |
| Windsurf | Workspace rules or `AGENTS.md` | Reference the canonical standards from workspace instructions. |
| OpenAI Codex | `AGENTS.md` | Use the included `AGENTS.md` directly. |
| Other agents | Their project instruction mechanism | Point to `README.md`, `AGENTS.md`, and relevant standards. |

These are integration suggestions, not guarantees about each product's current instruction discovery behavior. Check the agent's documentation and avoid maintaining multiple conflicting copies of the standards.

## Contributing

Propose changes to the canonical standards first. Keep guidance actionable, framework-neutral, and compatible with incremental work in existing applications. Update examples or templates when a standards change affects them.

## License

This project is licensed under the [MIT License](LICENSE).
