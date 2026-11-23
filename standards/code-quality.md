# UI code quality

- Follow the repository's language, framework, naming, formatting, and file organization conventions.
- Keep UI logic readable and explicit. Extract helpers when they clarify domain behavior or remove meaningful duplication, not just to reduce line count.
- Use types and validation patterns already established by the project. Handle nullable, missing, and unexpected data deliberately.
- Avoid dead code, unexplained constants, duplicated logic, and unnecessary dependencies.
- Keep user-facing copy clear, consistent, and easy to localize when the project supports localization.
- Update relevant tests or examples when behavior changes, following the project's existing practices.
- Run relevant existing checks when available. Describe checks that passed and clearly identify checks that were not run; do not imply a visual review or test occurred if it did not.
- Review the final diff for unrelated changes, regressions, and consistency with nearby UI.
