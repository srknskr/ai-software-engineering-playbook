# AGENTS.md

## Mission

Build Fieldnote as a reliable product, not as a collection of disconnected generated screens.

## Source of truth

Read these files before implementation:

- `docs/PRD.md` — product goals and requirements
- `docs/TRD.md` — architecture and technical constraints
- `docs/USER_FLOWS.md` — expected user journeys and failure paths
- `docs/UI_UX_DESIGN.md` — visual and interaction rules
- `docs/DATABASE_SCHEMA.md` — data model and invariants
- `docs/IMPLEMENTATION_PLAN.md` — current execution phase
- The relevant file under `skills/` — working method and quality gates

If two documents conflict, stop and report the conflict. Do not silently invent a new architecture.

## Working rules

1. Inspect the existing code before editing it.
2. Implement only the next incomplete phase unless the user expands scope.
3. Reuse existing patterns and components.
4. Keep validation, loading, empty, error, and mobile states explicit.
5. Never claim a flow works without running it.
6. Do not put secrets in source code, documentation, screenshots, or test fixtures.
7. Update the relevant documentation when an approved decision changes.

## Definition of done

Before reporting completion:

- Run formatting, linting, and type checks.
- Run unit and integration tests.
- Start the application in a production-like mode.
- Exercise the affected flow with Playwright at desktop and mobile widths.
- Fix discovered issues and repeat the checks.
- Summarize changed files, verification results, and any remaining risks.
