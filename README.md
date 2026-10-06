# AI Software Engineering Playbook

An opinionated, framework-agnostic example repository for building software with AI coding agents.

The goal is not to produce a longer prompt. The goal is to give the agent a small engineering system it can read, follow, test, and update.

## What this repository demonstrates

```text
Product idea
    ↓
PRD → User flows → UI/UX design → Database schema → TRD
    ↓
Implementation plan → Agent skills → Code
    ↓
Lint → Typecheck → Unit tests → Playwright → Fixes → Retest
```

## Repository map

```text
.
├── AGENTS.md
├── docs/
│   ├── PRD.md
│   ├── TRD.md
│   ├── USER_FLOWS.md
│   ├── UI_UX_DESIGN.md
│   ├── DATABASE_SCHEMA.md
│   └── IMPLEMENTATION_PLAN.md
├── skills/
│   ├── design/SKILL.md
│   └── testing/SKILL.md
├── examples/prompts/feature-prompt.md
└── tests/e2e/README.md
```

## How to use it

1. Replace the example product in `docs/PRD.md` with your product.
2. Make the architecture decisions explicit in `docs/TRD.md`.
3. Describe success and failure paths in `docs/USER_FLOWS.md`.
4. Define the visual language and interaction states in `docs/UI_UX_DESIGN.md`.
5. Keep the data model and implementation phases current.
6. Ask the coding agent to read `AGENTS.md` before changing code.
7. Require browser verification for user-facing changes.

## Design principles

- Documentation is versioned beside code.
- Requirements, architecture, design, and execution are separate concerns.
- Agents should implement one incomplete phase at a time.
- Generation and review are different activities.
- A feature is not complete until its affected user flow is tested.
- The agent may suggest changes, but a human owns product and architectural decisions.

## Example product

The documents describe a small product called **Fieldnote**: a cross-platform app for creating entries, attaching images, and receiving optional AI-generated summaries. It is deliberately generic so the structure can be reused for a web, mobile, or API project.

## License

MIT. Use the structure, adapt the documents, and make the decisions explicit.
