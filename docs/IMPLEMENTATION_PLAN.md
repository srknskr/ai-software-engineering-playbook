# Implementation Plan

Status markers: `[ ]` planned, `[~]` in progress, `[x]` complete.

## Phase 1 — Foundation

- [ ] Initialize web, mobile, and API packages
- [ ] Add TypeScript, formatting, lint, and typecheck
- [ ] Configure environment validation
- [ ] Add CI quality gates

## Phase 2 — Authentication

- [ ] Create user and session tables
- [ ] Implement sign-up and sign-in
- [ ] Add protected API middleware
- [ ] Test invalid credentials and sign-out

## Phase 3 — Entries

- [ ] Create entry migrations and service
- [ ] Build dashboard and entry editor
- [ ] Add image upload flow
- [ ] Add empty, loading, and error states
- [ ] Verify create/edit/delete in Playwright

## Phase 4 — AI summary

- [ ] Add provider adapter interface
- [ ] Add durable summary job
- [ ] Show progress, success, retry, and failure states
- [ ] Add cost and latency logging without prompt contents

## Phase 5 — Hardening

- [ ] Add ownership and upload security tests
- [ ] Test mobile viewport and keyboard navigation
- [ ] Run dependency and secret scans
- [ ] Document rollback procedure

## Delivery rule

An agent should select the next incomplete item, implement the smallest coherent slice, run the relevant checks, and update this file only after verification succeeds.
