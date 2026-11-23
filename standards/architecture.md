# UI architecture

## Inspect before changing

- Map the relevant route or screen, its parent layout, data flow, shared components, styles, tokens, and existing tests or checks before editing.
- Read project instructions and inspect neighboring implementations. Treat established conventions as intentional unless there is evidence otherwise.
- Identify the narrowest layer that should own the requested behavior: page composition, domain feature, shared UI, or application shell.

## Preserve useful boundaries

- Keep page composition, domain behavior, reusable presentation, and data access separated according to the project's existing architecture.
- Place a component where its reuse and ownership make sense. Do not move code into a shared layer solely because it could theoretically be reused.
- Keep state close to the components that need it. Lift or share state only when multiple consumers require coordinated behavior.
- Keep styling and tokens aligned with the project's established organization.

## Change incrementally

- Prefer a small, coherent change over a rewrite. Preserve existing routes, public component APIs, user workflows, and data contracts unless the request requires changing them.
- Avoid duplicate components, parallel design systems, and unnecessary dependencies. Extend existing abstractions when they remain clear and suitable.
- If a structural change is necessary, explain the need and keep migration scope explicit.

## Verify in context

- Inspect the affected UI alongside nearby screens and shared components.
- Check relevant states and responsive layouts, and use the project's available checks for the changed area.
- Report verification accurately, including any state or environment that could not be checked.
