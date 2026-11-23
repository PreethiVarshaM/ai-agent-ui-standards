# Project UI baseline

Copy this template into the project, complete it with the developer and AI agent, and link to it from the agent's instruction file. Keep canonical reusable guidance in this repository rather than duplicating it here.

For each field, record one of: **Observed** (include a file, command, or other evidence), **Chosen** (confirmed by the team), **Unknown**, or **Not applicable**. Do not let the agent silently fill gaps with guesses. Use [`../guides/project-discovery.md`](../guides/project-discovery.md) to gather the information.

## Project context

- Product or application:
- Main frontend entry points:
- Framework and rendering approach (if relevant):
- Supported browsers or device constraints:
- Project stage: existing / new / prototype / other:

## Existing UI system

- Shared component library and location:
- Design token source and naming conventions:
- Styling approach and conventions:
- Typography and icon sources:
- Existing layout, navigation, and page patterns:
- Theme or brand requirements:

## Architecture and data

- Route and feature organization:
- State and data-fetching conventions:
- API client or service boundary:
- Authentication and authorization conventions:
- Localization requirements:
- Important data, privacy, or security constraints affecting UI:

## Architecture baseline

- Current or chosen application structure:
- Where routes or screens belong:
- Where reusable UI belongs:
- Where domain-specific UI belongs:
- Where API and integration code belongs:
- State ownership and sharing approach:
- Architecture decisions that should not change without discussion:

## Verification

- Commands for linting, type checking, tests, or builds:
- How to run or inspect the application:
- Accessibility tools or manual checks used by the team:
- Browser, viewport, or device coverage expected:
- Environments or services required to verify a change:

## Project-specific decisions

Record only decisions that are specific to this project and not already covered by the shared standards. If a decision changes a shared standard, update the canonical standard instead.

## Discovery notes

- Inspected paths and commands:
- Confirmed observations:
- Open questions or assumptions to resolve:
- Decisions confirmed by the developer:
- Last reviewed:
