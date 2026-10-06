# Product Requirements Document

## Product

**Fieldnote** is a cross-platform journal for capturing a daily entry, attaching an image, and receiving an optional AI-generated summary.

## Problem

People collect observations across notes, camera rolls, and chat messages. Fieldnote keeps an entry and its context together without turning a simple journal into a complex project-management tool.

## Users

- People who want a lightweight personal journal
- Researchers and makers recording field observations
- Users who want searchable history and short summaries

## Goals

- Create and save an entry in under one minute.
- Make past entries easy to find and compare.
- Make AI assistance optional, transparent, and easy to retry.
- Keep the first release useful without an AI subscription.

## Non-goals

- Social feeds or public profiles
- Medical, legal, or financial advice
- Fully autonomous decisions made by AI
- Offline conflict resolution in the first release

## Functional requirements

### Authentication

- A user can create an account with email and password.
- A user can sign in and sign out.
- Unauthenticated users cannot access private entries.

### Entries

- A user can create, edit, view, and delete their own entry.
- An entry contains a title, notes, optional image, and timestamps.
- Entries are listed newest first.
- The list supports keyword search.

### AI summary

- A user can request a summary for an existing entry.
- The UI shows that the summary is AI-generated.
- A failed request can be retried without duplicating the entry.
- The original notes remain unchanged.

## Success criteria

- 90% of new users can create their first entry without help.
- Entry creation succeeds in at least 99% of valid requests.
- Every release has automated coverage for authentication and entry creation.
- No private entry is returned for another user.

## Release 1 acceptance criteria

- Sign-up, sign-in, and sign-out work.
- Authenticated users can create and view entries.
- Invalid forms have actionable messages.
- The core flow works at desktop and mobile widths.
