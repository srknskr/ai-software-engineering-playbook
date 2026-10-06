# UI/UX Design Specification

## Visual direction

Fieldnote should feel calm, practical, and editorial. It should not look like a generic AI dashboard.

## Tokens

```text
Color
- Ink: #102033
- Paper: #F7F5F0
- Accent: #C58B2A
- Muted text: #647184
- Error: #B42318

Typography
- Display: expressive serif or humanist sans
- Body: readable system sans
- Code: monospace

Layout
- 8px spacing base
- 16px mobile side padding
- 32px desktop side padding
- 12px default radius
- 44px minimum touch target
```

## Components

- `Button`: primary, secondary, destructive, loading, disabled
- `TextField`: label, hint, error, focused, disabled
- `EntryCard`: title, date, image state, summary state
- `EmptyState`: explanation plus one clear next action
- `Toast`: success and recoverable error only
- `Dialog`: title, consequence, cancel, confirm

## Responsive rules

- The entry editor is one column on mobile and two columns on wide screens.
- Never hide the save action only behind hover.
- Navigation remains keyboard accessible at every breakpoint.
- Content must remain usable at 320px viewport width.

## Accessibility

- Use semantic headings in order.
- Every form control has a visible label or an accessible name.
- Focus indicators are visible against both light and dark surfaces.
- Errors are associated with their fields and announced when appropriate.
- Do not communicate state with color alone.

## Quality questions

- Does the page have one obvious primary action?
- Can a first-time user recover from every failure state?
- Are repeated cards helping scanability, or are they hiding hierarchy?
- Is motion explaining a state change rather than decorating the page?
