# Regression Test Prompts

Prompts for checking that recent changes did not break the core loop.

---

## General Regression Smoke Test

```text
Run a regression/smoke test after the recent changes.

Goal:
Verify the current implemented loop before adding new features.

Focus:
- project launches cleanly
- main workflow still completes
- recent feature works
- adjacent systems still work
- settings/persistence still work if relevant
- fallback path still works if one exists
- no obvious runtime errors
- no data/math regression

Rules:
- Report failures first.
- Do not add features.
- Do not refactor.
- Fix only launch/runtime blockers if explicitly asked.
```

---

## Feature Regression Test

```text
Regression-test [FEATURE_NAME].

Focus:
- normal path
- edge path
- cancellation/close path
- repeated-use path
- adjacent feature interaction
- persistence/state reset if relevant

Report:
- passed checks
- failed checks
- not tested
- recommended fixes

Do not implement fixes unless asked.
```

---

## UI Regression Test

```text
Smoke-test the UI after recent layout/presentation changes.

Focus:
- panels open and close
- buttons still work
- input is not blocked accidentally
- important text is readable
- overlays layer correctly
- settings/pause/confirm dialogs still appear above the primary UI
- no major layout overlap at common window sizes

Do not redesign the UI during this test.
```

---

## Documentation Regression Test

```text
Check whether the documentation still matches the current project state.

Focus:
- README overview is accurate
- AGENTS instructions are still valid
- current-state docs match implemented features
- NEXT_STEPS points to the actual next task
- CHANGELOG includes notable recent changes
- planned/deferred work is not described as live

Do not edit yet. Report mismatches first.
```
