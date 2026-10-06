# Technical Requirements Document

## Architecture

Use a modular monolith for the first release:

```text
Web / Mobile clients
        ↓ HTTPS
REST API
        ↓
Application services
        ↓
PostgreSQL + object storage
        ↓
Background worker → AI provider
```

The repository may be implemented with different frameworks. The boundaries and contracts matter more than the framework choice.

## Decisions

| Area | Decision |
| --- | --- |
| Web | React-based application with TypeScript |
| Mobile | React Native client sharing API contracts |
| API | REST, JSON, versioned under `/api/v1` |
| Database | PostgreSQL |
| ORM | A typed ORM with explicit migrations |
| Auth | Short-lived access token plus rotating refresh token |
| Storage | Private object storage with signed upload URLs |
| Jobs | Durable queue for AI summaries and notifications |
| AI | Provider adapter behind an application service |
| Deployment | CI builds immutable artifacts; production runs a tagged release |
| Testing | Unit, API integration, and Playwright end-to-end tests |
| Observability | Structured logs, request IDs, health checks, error reporting |

## API conventions

- Return a stable JSON envelope for errors.
- Use nouns for resources and HTTP methods for actions.
- Validate input at the API boundary.
- Authorize every resource by authenticated user ID.
- Use idempotency keys for retriable commands that create side effects.
- Never return provider API keys or internal stack traces.

## Security requirements

- Hash passwords with a modern password hashing algorithm.
- Store refresh tokens hashed and rotate them after use.
- Enforce ownership checks in the service layer, not only in the UI.
- Validate upload MIME type, size, and image dimensions.
- Keep AI prompts and provider responses out of ordinary application logs.
- Use least-privilege credentials for database, storage, and deployment.

## Quality gates

Every pull request must pass formatting, lint, typecheck, unit tests, API tests, and the affected Playwright flow before merge.
