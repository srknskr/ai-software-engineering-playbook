# Design Skill

## Purpose

Create interfaces that follow the product design specification and remain usable on real devices.

## Before coding

- Read `docs/UI_UX_DESIGN.md` and the affected user flow.
- Inspect existing components before creating a new one.
- Identify loading, empty, error, disabled, focus, and mobile states.

## While coding

- Prefer semantic HTML and accessible primitives.
- Reuse tokens and components instead of introducing one-off styles.
- Give each screen one clear primary action.
- Avoid turning every section into a card.
- Use motion only to explain a state change.

## Review checklist

- Keyboard navigation works.
- Focus is visible.
- Touch targets are large enough.
- Text remains readable at narrow widths.
- Errors explain how to recover.
- The visual hierarchy matches the product goal.
