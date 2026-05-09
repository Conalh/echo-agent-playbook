# Regression Test Prompts

Prompts for checking that recent changes did not break the core path.

## General Smoke Test

```text
Run a regression smoke test after the recent changes.

Goal:
Verify the implemented loop before adding features.

Focus:
- project launches cleanly
- main workflow completes
- recent feature works
- adjacent systems still work
- settings/persistence still work if relevant
- fallback path still works if one exists
- no obvious runtime errors
- no data regression

Rules:
- Report failures first.
- Do not add features.
- Do not refactor.
- Fix launch/runtime blockers only if asked.
```

## Feature Regression

```text
Regression-test [FEATURE_NAME].

Focus:
- normal path
- edge path
- cancel/close path
- repeated-use path
- adjacent interactions
- persistence or reset, if relevant

Report:
- passed checks
- failed checks
- not tested
- recommended fixes

Do not implement fixes unless asked.
```

## UI Regression

```text
Smoke-test the UI after recent layout or presentation changes.

Focus:
- panels open and close
- buttons work
- input is not blocked
- important text is readable
- overlays layer correctly
- settings and confirmation dialogs appear above base UI
- no major layout overlap at common sizes

Do not redesign the UI during this test.
```

## Documentation Regression

```text
Check whether documentation matches current project state.

Focus:
- README overview is accurate
- AGENTS instructions are valid
- current-state docs match implemented features
- NEXT_STEPS points to the next real task
- CHANGELOG includes notable recent changes
- planned/deferred work is not described as live

Do not edit. Report mismatches first.
```
