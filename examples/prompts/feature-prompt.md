# Example Feature Prompt

```text
Read AGENTS.md and the relevant files under docs/ and skills/.

Implement the next incomplete item in docs/IMPLEMENTATION_PLAN.md.
For this task, do not introduce a new architectural pattern.

Before changing code:
1. Explain which requirement and user flow are affected.
2. Identify the existing components and services to reuse.
3. State the validation and failure states you will cover.

After implementation:
1. Run formatting, lint, typecheck, and automated tests.
2. Start the application in production-like mode.
3. Exercise the affected flow with Playwright on desktop and mobile widths.
4. Fix discovered issues and retest.
5. Update IMPLEMENTATION_PLAN.md only after verification succeeds.
6. Report changed files, commands, results, and remaining risks.
```
