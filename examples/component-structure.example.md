# Example component structure

This is one possible organization, shown without a framework requirement. Keep the structure your project already uses unless there is a clear reason to change it.

```text
features/
  account-settings/
    AccountSettingsPage.*       # Route-level composition
    AccountForm.*               # Feature-owned form behavior
    account-settings.css        # Feature-scoped styling, if colocated by convention
    account-settings.test.*     # Tests, if colocated by convention

shared/
  Button.*                      # Shared primitive with a stable API
  FormField.*                   # Shared accessible field composition
```

## Ownership cues

- Keep route composition with the route or feature that owns it.
- Keep business rules and API-specific behavior in the feature or the project's established service layer.
- Promote a visual component to shared UI when it has clear reuse or shared ownership, not because it might someday be reused.
- Keep a generic primitive independent of endpoint-specific data and domain decisions.
- Follow existing naming, export, test, and style-file conventions.
