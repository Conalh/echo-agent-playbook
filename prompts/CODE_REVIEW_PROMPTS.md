# Code Review Prompts

Prompts for reviewing code changes with an AI assistant.

---

## Focused Diff Review

```text
Review this diff for correctness and scope control.

Focus:
- bugs
- unintended behavior changes
- overbroad edits
- state ownership issues
- missing verification
- docs/changelog mismatch

Rules:
- Do not rewrite the patch.
- Prioritize issues by severity.
- Ignore style preferences unless they affect maintainability.
```

---

## Pre-Merge Review

```text
Review the current branch before merge.

Focus:
- changed files are expected
- feature works as requested
- no unrelated refactors slipped in
- tests/checks were run
- docs/changelog are updated if needed
- no secrets or generated junk are included

Report:
- blockers
- warnings
- optional cleanup
- suggested commit message
```

---

## Safety Review

```text
Review this change for safety risks.

Focus:
- data loss
- save/load changes
- migrations
- file deletion
- destructive commands
- security/privacy issues
- dependency changes

Rules:
- Report blockers first.
- Be conservative.
- Recommend rollback or isolation if needed.
```

---

## Documentation Review

```text
Review these docs for clarity and truthfulness.

Focus:
- implemented vs planned distinction
- stale claims
- unclear source of truth
- missing next steps
- project-specific content inside generic docs

Rules:
- Give exact suggested edits.
- Do not rewrite the whole document unless asked.
```
