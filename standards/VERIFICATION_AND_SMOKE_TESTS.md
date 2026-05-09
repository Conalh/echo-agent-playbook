# Verification and Smoke Tests

Reusable standards for checking AI-assisted changes.

---

## Verification Levels

### 1. Static Check

Use when checking structure or syntax.

Examples:

- lint
- type check
- format check
- import check
- file tree inspection

### 2. Unit Check

Use when behavior has isolated tests.

Examples:

- unit tests
- small script tests
- component tests

### 3. Integration Check

Use when systems interact.

Examples:

- start app
- complete a workflow
- verify a UI panel opens
- verify state changes across screens

### 4. Regression Smoke Test

Use after several systems changed or when the app has become fragile.

A smoke test checks the core loop without trying to test every edge case.

---

## Smoke Test Template

```md
# Smoke Test — [DATE / FEATURE]

Goal:
Verify the current implemented loop before adding new mechanics.

Focus:
- app launches cleanly
- main workflow still works
- recent feature still works
- adjacent systems were not broken
- settings/persistence still work if relevant
- no obvious runtime errors
- rollback path still works if one exists

Report failures first.
Do not add new features during this pass.
```

---

## Regression Prompt Pattern

```text
Run a live regression/smoke test after the recent [FEATURE/SYSTEM] changes.

Goal:
Verify the implemented loop before adding mechanics.

Focus:
- [critical path]
- [recent feature]
- [adjacent feature]
- [settings/persistence]
- [fallback/rollback]
- [no math/data regression]

Report failures first.
Do not add mechanics.
```

---

## Agent Verification Report

Use:

```text
Verified:
- [check]: passed
- [check]: passed

Failed:
- [check]: [failure]

Not verified:
- [check]: [why]
```

Do not hide failed checks under a general success summary.

---

## When Verification Cannot Be Run

Say so directly.

Example:

```text
I could not run the app in this environment. Manual checks needed:
- Launch the app.
- Open Settings.
- Complete one normal workflow.
- Confirm the changed panel appears once.
```
