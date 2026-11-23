# Design system

## Establish a shared visual language

- Reuse the project's existing design system, component library, and tokens as the first choice.
- When a project has no system, introduce a small, documented set of centralized tokens suited to its actual UI. Avoid building an elaborate token taxonomy before there is a need.
- Keep canonical values in one place and reference them from components and styles. Avoid parallel definitions for the same role.

## Token categories

Centralize values that recur or express a meaningful design decision, such as:

- Color roles: page and surface backgrounds, text, borders, interactive states, and semantic feedback.
- Typography: font families, sizes, weights, line heights, and hierarchy.
- Spacing: a consistent scale for gaps, padding, and layout rhythm.
- Shape and depth: border widths, radii, and shadows where used.
- Layout: content widths, navigation dimensions, and responsive breakpoints when these are shared project decisions.

Prefer role-based names such as `--color-text-muted` over names tied only to a specific screen. Preserve established naming when it is already clear and consistent.

## Use tokens consistently

- Use an existing token when its role fits. If a recurring design need has no token, add a suitable token in the canonical location and reuse it.
- Do not add a token for every isolated value. A one-off value is appropriate when it is intrinsic to an asset, required for a precise interaction, or justified by the design.
- Keep light, dark, and other themes coherent through semantic roles rather than scattering mode-specific overrides.
- Check contrast and state distinctions when defining color combinations.

The files in `examples/` show illustrative CSS and SCSS token structures. They are starting points, not required naming or values.
