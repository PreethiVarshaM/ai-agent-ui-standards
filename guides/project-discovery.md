# Project discovery and architecture setup

Use this workflow before making UI changes in an unfamiliar project and before proposing structure for a new one. It is framework-neutral. Discovery should produce an evidence-based map and a short, reviewable configuration, not a speculative redesign.

## Start by classifying the project

Identify the situation:

- **Established:** application code, conventions, and UI already exist.
- **New with constraints:** product or technical requirements exist, but implementation is not established.
- **Empty or unclear:** little code or insufficient information exists to make a sound recommendation.

State which case applies and why. If evidence is mixed, explain the uncertainty.

## Existing project: inspect before recommending

Read project instruction files and inspect only the files relevant to understanding the application. Use repository contents and available scripts as evidence; do not assume a framework from a dependency name alone.

Build a compact map of:

1. **Application shape:** entry points, routes/screens, layouts, packages or apps in a monorepo.
2. **UI structure:** feature boundaries, shared components, design system or component library, and ownership conventions.
3. **Styling:** CSS/Sass/utilities/library, token sources, theming, and responsive conventions.
4. **Behavior and data:** state ownership, data-fetching paths, API boundaries, authentication patterns relevant to UI.
5. **Quality workflow:** scripts for development, builds, type checks, linting, tests, accessibility checks, and visual inspection.
6. **Agent configuration:** existing instructions, local rules, and project-specific baselines.

Use a brief report:

```text
Project type: established / new with constraints / empty or unclear
Observed architecture: [short map with evidence paths]
Existing UI system: [components, tokens, styling]
Data and state conventions: [observed patterns]
Available verification: [actual scripts and commands]
Unknowns: [only items that affect the next decision or requested change]
Recommended next step: [smallest useful action]
```

Separate **observed** facts from **inferences** and **recommendations**. Cite paths or commands for important claims. If a detail cannot be verified, mark it unknown. Do not scan secrets or dump environment files while discovering configuration.

For an established application, treat the current architecture as the baseline. Recommend change only when the requested work cannot fit it, a concrete problem is evidenced, or the developer asks for redesign. Explain the smallest viable adjustment and its migration impact before proceeding.

## New project: guide decisions in context

Do not select a default stack just because it is familiar. First gather the requirements that could change the recommendation. Ask a small, prioritized set of questions; continue with clear assumptions only when the developer prefers speed and the assumptions are low impact.

Useful prompts include:

- What is the product and who uses it? What are the first one to three screens or workflows?
- Is this a browser app, mobile app, desktop app, or a combination? Are there required platforms or accessibility targets?
- Is a language, framework, hosting environment, backend, design system, or component library already required?
- Is this a prototype, internal tool, content site, or long-lived product? What team will maintain it?
- Does it need authentication, user-specific data, localization, offline use, or real-time updates?
- What commands and environments can be used to build, check, and review it?

Then present a compact proposal with alternatives only where a real tradeoff exists. Include the reason each choice fits the stated constraints, what it makes easier or harder, and which decisions remain open. Avoid premature choices such as elaborate folder taxonomies or global state libraries before the use case needs them.

## Establish the initial architecture baseline

Agree on only the decisions needed to start safely:

- Runtime, framework, and rendering approach, if required by the product.
- Route or screen organization and the boundary between app shell, features, and shared UI.
- Component library and design-token approach; if none exists, define a small initial token set.
- Styling method consistent with team skills and platform constraints.
- Data and API boundary, including where request state and errors are handled.
- State ownership approach for local, shared, and server data.
- Accessibility, responsive, localization, and security needs that affect structure.
- Build, lint, type-check, test, and visual review commands that are actually available.

Record each as **Chosen**, **Required**, or **Open** in the project UI baseline. Distinguish hard requirements from preferences. Prefer reversible choices and a simple initial structure. Do not create files, install dependencies, or scaffold until the developer has accepted the proposal when the request was only to explore or plan.

## Configure and verify

After agreement:

1. Place the completed project baseline and a short agent adapter in the project's instruction locations.
2. Create only the agreed architecture and configuration. Reuse existing tooling if already present.
3. Run the available setup and quality commands from the project's own configuration; do not invent command names.
4. Inspect the resulting entry point and one representative screen or component to confirm the files match the intended boundaries.
5. Update the baseline with actual paths, scripts, and any decisions changed during implementation.

If setup fails or a dependency is unavailable, report the blocker and options. Do not quietly replace an agreed technology choice or claim the project is configured before verification.
