# Agent adapter example

Use this as source text for the instruction file supported by your AI coding agent. Update the relative paths to match where this repository is stored in your project.

```md
## UI engineering baseline

Before UI work in an unfamiliar or new project, follow `path/to/ai-agent-ui-standards/guides/project-discovery.md`.
Follow `path/to/ai-agent-ui-standards/AGENTS.md` and the applicable documents in `path/to/ai-agent-ui-standards/standards/`.
Use `path/to/project-ui-baseline.md` for confirmed project-specific architecture and UI conventions.

Preserve the existing architecture in established projects. For new projects, separate observed facts, assumptions, and recommendations; agree on the initial architecture baseline before scaffolding. Do not make broad structural changes unless requested.
```

An adapter should stay short and point to the canonical files. If the agent cannot access linked or vendored files, put the necessary concise instructions directly in its supported instruction file and keep that copy synchronized with the standards.
