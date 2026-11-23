# Example project discovery output

This fictional example shows the format and evidence level to aim for. Paths and commands below are illustrative; they do not describe a real repository.

## Discovery summary

**Project type:** Established web application.

### Observed

- `src/main.js` initializes the application through `src/app/create-app.js`.
- `src/app/routes.js` maps the dashboard and orders screens.
- `src/features/orders/` owns the orders screen and its order-specific behavior.
- `src/shared/ui/` contains the shared `Button` and `Card` components.
- `styles/tokens.css` defines color and spacing custom properties; feature styles reference those variables.
- `src/data/clients/orders.js` is the existing boundary for order requests.
- `package.json` defines `dev`, `build`, and `check` scripts. No accessibility-specific command is present.

### Inferences

- The application appears to use feature-owned screens with a small shared presentation layer.
- The token file is likely the canonical location for new shared visual values; confirm with the team before adding a new category.

### Unknowns

- Whether the team has a required browser support matrix.
- Whether keyboard and screen-reader checks are part of the team's manual review process.

### Recommended next step

Confirm the two unknowns if they affect the requested work, then record the observed paths and team answers in the project UI baseline. Reuse `Button`, `Card`, and the existing order client when changing the orders screen. No architecture change is indicated by this inspection.

## Example baseline entries

| Baseline field | Status | Value / evidence |
| --- | --- | --- |
| Route organization | Observed | `src/app/routes.js` |
| Feature UI ownership | Observed | Screens and behavior live under `src/features/<feature>/`. |
| Shared UI | Observed | `src/shared/ui/` |
| Design tokens | Observed | `styles/tokens.css` |
| API boundary | Observed | `src/data/clients/` |
| Verification | Observed | `npm run check`; `npm run build` |
| Browser support | Unknown | Ask the team when relevant. |
| Architecture decisions requiring discussion | Chosen | Preserve feature ownership and shared UI boundaries; ask before moving code between them. |
