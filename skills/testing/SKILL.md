# Testing Skill

## Purpose

Verify behavior from the user's perspective instead of treating compilation as proof of correctness.

## Test layers

1. Unit tests for deterministic domain rules.
2. API tests for validation, authorization, and persistence.
3. Playwright tests for complete user journeys.

## Browser workflow

- Start the app in production-like mode.
- Test the happy path.
- Test one validation failure.
- Test one network or provider failure.
- Refresh after a successful write and verify persistence.
- Repeat the critical flow at a mobile viewport.

## Evidence

Record the command, result, and any known limitation. Do not report a green test when the command was skipped or failed to start.
