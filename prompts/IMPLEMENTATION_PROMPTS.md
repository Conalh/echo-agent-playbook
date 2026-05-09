# Implementation Prompts

Prompts for focused coding work.

## Small Feature

```text
Implement [FEATURE_NAME].

Goal:
[desired behavior]

Scope:
- [file/system]
- [file/system]

Rules:
- Keep the change minimal.
- Do not refactor unrelated code.
- Match existing naming and style.
- Add architecture only if required.
- Update docs/changelog only for notable changes.

Verify:
- [specific check]
- [specific check]

Report:
- files changed
- checks run
- what was intentionally not changed
```

## Bug Fix

```text
Fix [BUG_DESCRIPTION].

Observed:
[current behavior]

Expected:
[desired behavior]

Reproduction:
1. [step]
2. [step]
3. [step]

Rules:
- Find the smallest fix.
- Do not rewrite adjacent systems.
- Add a focused test if the project has tests.
- Do not hide failed verification.

Verify:
- reproduce the bug if possible
- confirm the path now passes
- check likely adjacent regression
```

## UI Behavior

```text
Implement this UI behavior change: [CHANGE].

Goal:
[user-visible result]

Rules:
- Do not change unrelated layout.
- Do not rename components unless required.
- Keep core state in the parent/system layer.
- UI displays state and emits intent.

Verify:
- [manual UI check]
- [state check]
- [regression check]
```

## Add Document

```text
Create [FILE_NAME].

Purpose:
[what this document helps with]

Rules:
- Keep it project-agnostic unless told otherwise.
- Use clear headings.
- Include examples only if useful.
- Do not duplicate existing docs.

Verify:
- file exists in the correct folder
- README or index links it if appropriate
```
