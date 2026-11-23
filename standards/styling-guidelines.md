# Styling guidelines

- Follow the styling approach already used in the affected area, whether that is CSS, Sass, CSS modules, utility classes, a component library, or another established method.
- Reuse existing tokens, utilities, mixins, and component variants before adding new rules.
- Avoid arbitrary one-off values when a suitable token or scale value exists. If a new recurring value is needed, add it to the canonical token source.
- Scope styles to the component or feature they serve. Avoid broad selectors and overrides that unintentionally affect other screens.
- Keep selectors and specificity straightforward. Do not use `!important` to mask a cascade issue without understanding and addressing its cause.
- Prefer layout systems such as flexbox or grid over fragile positional offsets for normal page structure.
- Use transitions and animation sparingly; respect reduced-motion preferences and avoid motion that obscures content or interaction.
- Ensure hover is not the only indication of interactivity. Define visible focus and meaningful disabled, selected, error, and other relevant states.
- Avoid introducing a second styling system or dependency for a localized change.
