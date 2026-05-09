# Coding Guardrails

Rules that prevent common AI coding failures: guessing, overbuilding, broad refactors, and false success claims.

## 1. Think First

Before implementation, identify:

- goal
- assumptions
- affected files or systems
- simplest approach
- verification plan

If a simpler path exists, name it before building.

## 2. Prefer Simple Code

Use:

- clear functions
- direct data flow
- local fixes
- existing patterns
- readable control flow

Avoid:

- speculative architecture
- generic helpers for one use
- unused configuration
- cleverness
- defensive code for impossible states

Test:

```text
Would a maintainer call this overcomplicated?
```

If yes, simplify.

## 3. Keep Scope Surgical

Do not:

- refactor adjacent systems
- rename unrelated variables
- change file layout
- rewrite working code
- clean unrelated style
- delete unused code without approval

Mention worthy cleanup as follow-up.

## 4. Define Success

Generic example:

```text
Goal:
Add confirmation before deleting an item.

Success:
The confirmation opens, cancel leaves data unchanged, confirm deletes once, and unrelated actions still work.

Plan:
1. Add confirmation state -> verify prompt opens.
2. Wire confirm/cancel -> verify both paths.
3. Check adjacent actions -> verify no regression.
```

## 5. Match Architecture

Follow existing:

- naming
- file placement
- control flow
- data ownership
- test style

Do not introduce a new style casually.

## 6. Keep Ownership Clear

General rule:

```text
Core systems own state.
UI displays state and emits intent.
Parent systems coordinate children.
```

Avoid scattering one state across views, helpers, and globals unless the project already works that way.

## 7. Keep Rules Out of Presentation

Presentation code should not secretly own business rules.

If visual behavior affects logic, make the logic explicit.

## 8. Verify the Narrow Path

First verify the changed behavior.

Then verify likely regressions.

## 9. Report Boundaries

State what was not changed.

Example:

```text
Not changed:
- Did not alter authorization rules.
- Did not change the data model.
- Did not refactor adjacent screens.
```
