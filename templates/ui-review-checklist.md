# UI review checklist

Use this checklist for changes to a screen, component, or frontend flow. Mark items that do not apply as N/A.

## Project fit

- [ ] I inspected the affected screen, nearby UI, project instructions, shared components, tokens, and styling conventions.
- [ ] The change reuses or appropriately extends existing components and patterns.
- [ ] The change is limited to the requested behavior and preserves unrelated functionality.

## Visual system

- [ ] Colors, type, spacing, borders, radii, and shadows follow existing tokens or justified project patterns.
- [ ] Layout and component states are consistent with adjacent screens.
- [ ] No avoidable duplicate component, token, dependency, or styling system was introduced.

## Accessibility and responsive behavior

- [ ] Semantic elements, labels, names, and heading structure are appropriate.
- [ ] Keyboard operation and visible focus work for the changed interactions.
- [ ] Status, error, and validation feedback can be perceived without color alone.
- [ ] Narrow and wide layouts handle content without clipping or unintended scrolling.
- [ ] Motion and contrast remain usable for the changed content.

## States and integration

- [ ] Relevant loading, error, empty, pending, disabled, and success states are handled.
- [ ] API or authentication behavior follows existing boundaries and does not expose sensitive details.
- [ ] Long, missing, or unexpected content does not break the UI.

## Verification

- [ ] Relevant existing checks were run, or the reason they could not be run is recorded.
- [ ] The changed UI was inspected in context where an appropriate environment was available.
- [ ] The final diff contains no unrelated changes, and any limitations are stated accurately.
