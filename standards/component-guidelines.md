# Component guidelines

## Design components around responsibility

- Give each component a clear purpose and keep it focused. Split a component when its responsibilities, state, or markup become difficult to understand or change independently.
- Prefer composition and existing primitives over a large component with many unrelated flags.
- Reuse an existing component when its behavior and visual role match. Extend it carefully when that is clearer than adding a duplicate.
- Create shared components for stable patterns with real reuse or clear shared ownership, not speculative reuse.

## Keep APIs understandable

- Use names that describe the component's role and props that make supported states explicit.
- Keep defaults predictable and avoid hidden global behavior.
- Preserve established public APIs unless the request requires an intentional change; consider existing call sites before changing a shared component.
- Keep domain-specific behavior with its owning feature rather than leaking it into a generic primitive.

## Handle state and content

- Represent loading, error, empty, success, disabled, and selected states when relevant to the component's role.
- Avoid inaccessible custom controls when a semantic native element provides the needed behavior.
- Support realistic content lengths, localization growth, and optional content without breaking layout.
- Keep component styles and state variants consistent with project tokens and patterns.

## Organize files

Follow the project's existing organization. A component's implementation, styles, tests, and documentation may be colocated when that convention is used. See `../examples/component-structure.example.md` for one possible structure.
