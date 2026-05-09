# Implementation Prompts

Reusable prompts for focused coding work.

---

## Small Feature Implementation

```text
Implement [FEATURE_NAME].

Goal:
[One-sentence description of the desired behavior.]

Scope:
- [file/system likely involved]
- [file/system likely involved]

Rules:
- Keep the change minimal.
- Do not refactor unrelated code.
- Match existing naming and style.
- Do not add new architecture unless required.
- Update docs/changelog only if this is a notable change.

Verify:
- [specific check]
- [specific check]

Report:
- files changed
- what changed
- checks run
- what was intentionally not changed
```

---

## Bug Fix

```text
Fix [BUG_DESCRIPTION].

Observed behavior:
[What currently happens.]

Expected behavior:
[What should happen.]

Reproduction:
1. [step]
2. [step]
3. [step]

Rules:
- Find the smallest fix.
- Do not rewrite adjacent systems.
- Add or update a focused test if the project has tests.
- Do not hide failed verification.

Verify:
- reproduce the bug before the fix if possible
- confirm the reproduction path now passes
- check likely adjacent regression
```

---

## UI Behavior Change

```text
Implement this UI behavior change: [CHANGE].

Goal:
[What should be true from the user's perspective.]

Rules:
- Do not change unrelated layout.
- Do not rename existing nodes/components unless required.
- Keep data ownership in the parent/system layer.
- UI should display state and emit intent, not secretly own core logic.

Verify:
- [manual UI check]
- [state check]
- [regression check]
```

---

## Add a New Document

```text
Create a new markdown document: [FILE_NAME].

Purpose:
[What this document should help with.]

Rules:
- Keep it project-agnostic unless told otherwise.
- Use clear headings.
- Include copy-paste examples if useful.
- Do not duplicate existing docs.

Verify:
- file exists in the correct folder
- README or index links it if appropriate
```
