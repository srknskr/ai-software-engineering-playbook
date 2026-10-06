# End-to-End Test Notes

This directory is reserved for Playwright tests that exercise complete user journeys.

Suggested first tests:

- `auth.spec.ts`: sign-up, sign-in, sign-out, invalid credentials
- `entries.spec.ts`: create, refresh, edit, delete
- `entry-failure-states.spec.ts`: rejected upload, API failure, retry
- `responsive.spec.ts`: create an entry at desktop and mobile widths

Tests should use stable accessible roles and labels rather than CSS implementation details.
