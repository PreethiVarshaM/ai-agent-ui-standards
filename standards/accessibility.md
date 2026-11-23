# Accessibility

Build accessibility into the structure and interaction rather than adding it only as a final polish step. Follow applicable project and legal requirements; this document is a baseline, not a substitute for a conformance audit.

## Semantics and names

- Use native semantic elements for headings, landmarks, lists, buttons, links, forms, and tables.
- Give controls accessible names that describe their purpose. Associate form labels and help or error text with their controls.
- Use heading levels in a logical hierarchy. Provide useful alternative text for informative images and empty alternative text for decorative images.
- Use ARIA only when native HTML cannot express the needed role, state, or relationship; keep ARIA properties accurate as state changes.

## Keyboard and focus

- Ensure all functionality works with a keyboard, with a logical focus order and no keyboard traps.
- Preserve a visible focus indicator. Do not remove browser focus styling without providing an equivalent or better treatment.
- Use buttons for actions and links for navigation. For custom widgets, implement the expected keyboard behavior and communicate the pattern clearly.
- When opening dialogs or overlays, manage initial focus, containment where appropriate, dismissal, and focus return according to the interaction pattern.

## Perception and feedback

- Check text and important UI contrast against their backgrounds. Do not use color as the only way to communicate meaning.
- Ensure content remains usable when text is zoomed or enlarged and when users prefer reduced motion.
- Make validation, loading, and action feedback perceivable without relying only on transient visual changes.
- Avoid flashing content and unexpected focus or context changes.

## Check the result

Use the project's accessibility checks when available, and manually inspect keyboard operation and key interaction states for the changed flow. Automated tools do not detect every accessibility issue.
