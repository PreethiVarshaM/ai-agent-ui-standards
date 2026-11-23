# Optional: frontend integration

Use this guidance when a UI change crosses an API, authentication, authorization, or service boundary. Follow the project's established architecture and security requirements; this document does not prescribe a backend stack.

## API contracts and data

- Inspect existing client services, request types, response shapes, and error conventions before changing integration code.
- Keep transport concerns at the project's established data-access boundary. Components should consume the project's existing hooks, services, or equivalent abstraction where available.
- Treat server data as untrusted and handle absent, stale, malformed, or partial values safely.
- Coordinate contract changes explicitly with the owning API. Avoid silently guessing field names, enum values, or success semantics.
- Keep secrets and privileged credentials out of client code. Only expose data intended for the client.

## User-visible request states

- Represent initial loading, refresh or pending work, empty results, recoverable errors, and successful completion as appropriate.
- Keep the user's input and context when a recoverable operation fails where practical. Offer a clear retry or next step when one exists.
- Prevent duplicate submissions where that could create duplicate effects, and show progress for operations that take time.
- Handle cancellation, stale responses, and concurrent updates according to the project's data-fetching conventions.
- Do not expose raw stack traces, internal service details, tokens, or sensitive response data in UI errors.

## Authentication and authorization

- Use the project's established session and identity mechanisms; do not invent a parallel token store or auth flow.
- Treat authentication (who the user is) and authorization (what the user can do) as distinct. The server remains authoritative for access decisions.
- Handle expired sessions and sign-in redirects without losing user context when the application supports safe return flows.
- Do not treat hiding a control in the UI as a security boundary. Enforce permissions at the service boundary as well.
- Avoid logging credentials, personal data, or sensitive payloads.

## Boundaries and verification

- Keep domain and transport types separate when the existing architecture does so; map API responses at the established boundary.
- Do not couple reusable visual primitives to a specific endpoint or backend response shape.
- Verify success and failure behavior using the project's established mocks, fixtures, or development environment when available.
- Document assumptions when a dependency contract or service behavior cannot be verified.
