# Refactor Prompts

Refactors need tight boundaries.

## Small Refactor

```text
Refactor [TARGET] to [GOAL].

Reason:
[why this is needed now]

Scope:
- [file]
- [file]

Rules:
- Preserve behavior.
- Do not add features.
- Do not rename public APIs unless required.
- Keep the diff reviewable.
- Stop if scope expands beyond the listed files.

Verify:
- existing checks still pass
- affected workflow behaves the same
- no unrelated files changed
```

## Extract Helper

```text
Extract repeated logic in [FILES/FUNCTIONS] into a small helper.

Rules:
- Extract only logic that already repeats.
- Do not generalize beyond current usage.
- Keep names concrete.
- Preserve behavior.

Verify:
- before/after behavior is the same
- call sites remain readable
```

## Cleanup After Feature Stabilizes

```text
Clean up [FEATURE_NAME].

Goal:
Improve readability without changing behavior.

Allowed:
- remove obvious duplication
- improve local names
- move helpers to existing appropriate locations
- update stale comments/docs

Not allowed:
- new features
- architecture rewrite
- broad renaming
- unrelated changes

Verify:
- behavior unchanged
- checks pass
- diff stays focused
```

## Stop Rule

```text
Stop after identifying the refactor plan.

Do not edit.

Report:
- why the refactor is needed
- files involved
- risk level
- smallest safe first phase
- verification plan
```
