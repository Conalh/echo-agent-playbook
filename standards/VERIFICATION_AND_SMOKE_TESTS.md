# Verification and Smoke Tests

Verification proves the changed path before success is claimed.

## Levels

### 1. Static Check

Use for structure or syntax.

Examples:

- lint
- type check
- format check
- import check
- file tree inspection

### 2. Unit Check

Use for isolated behavior.

Examples:

- unit tests
- small script tests
- component tests

### 3. Integration Check

Use when systems interact.

Examples:

- start app
- complete workflow
- verify state change
- verify UI opens or closes

### 4. Regression Smoke Test

Use after broad or risky changes.

Smoke tests check the core loop, not every edge case.

## Smoke Test Template

```md
# Smoke Test - [DATE / FEATURE]

Goal:
Verify the implemented loop before adding new behavior.

Focus:
- app launches cleanly
- main workflow still works
- recent feature still works
- adjacent systems still work
- settings or persistence still work, if relevant
- no obvious runtime errors

Report failures first.
Do not add features during this pass.
```

## Regression Prompt

```text
Run a regression smoke test after the recent [FEATURE/SYSTEM] changes.

Goal:
Verify the implemented loop before adding new behavior.

Focus:
- [critical path]
- [recent feature]
- [adjacent feature]
- [settings/persistence]
- [fallback path]

Report failures first.
Do not implement features.
```

## Report Format

```text
Verified:
- [check]: passed

Failed:
- [check]: [failure]

Not verified:
- [check]: [why]
```

Do not hide failed checks under a success summary.

## If Checks Cannot Run

Say so directly and list manual checks.
