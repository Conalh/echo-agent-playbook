# Refactor Prompts

Refactors are risky. Use these prompts to keep them contained.

---

## Small Refactor

```text
Refactor [TARGET] to [GOAL].

Reason:
[Why this refactor is needed now.]

Scope:
- [file]
- [file]

Rules:
- Preserve behavior.
- Do not add features.
- Do not rename public APIs unless required.
- Keep the diff reviewable.
- Stop if the refactor wants to expand beyond the listed scope.

Verify:
- existing tests/checks still pass
- affected workflow still behaves the same
- no unrelated files changed
```

---

## Extract Helper

```text
Extract the repeated logic in [FILES/FUNCTIONS] into a small helper.

Rules:
- Only extract the repeated logic that already exists.
- Do not generalize beyond current usage.
- Keep names concrete.
- Preserve behavior.

Verify:
- before/after behavior is the same
- call sites remain easy to read
```

---

## Cleanup After Feature Stabilizes

```text
Clean up [FEATURE_NAME] after implementation.

Goal:
Improve readability without changing behavior.

Allowed:
- remove obvious duplication
- improve names where local and safe
- move helper code to the existing appropriate location
- update comments/docs that are now stale

Not allowed:
- new features
- architecture rewrite
- broad renaming
- changes to unrelated systems

Verify:
- behavior unchanged
- tests/checks pass
- diff stays focused
```

---

## Refactor Stop Rule

Use this when an agent starts finding too much.

```text
Stop after identifying the refactor plan.

Do not edit yet.

Report:
- why the refactor is needed
- files involved
- risk level
- smallest safe first phase
- verification plan
```
