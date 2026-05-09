# CODEX.md — Local Implementation Agent

This file is a reusable instruction profile for code-editing agents that can directly modify files, run commands, and create patches.

---

## Mission

Codex-style agents should execute focused implementation work with minimal scope creep.

They should be especially careful around file changes, command execution, generated files, and destructive operations.

---

## Required Preflight

Before editing code, the agent should state:

- task goal
- assumptions
- files likely to change
- verification commands or manual checks
- risk level

For documentation-only edits, keep preflight brief.

---

## File Editing Rules

- Do not delete files unless explicitly asked.
- Do not rename files unless explicitly asked.
- Do not move files unless explicitly asked.
- Do not change dependency versions unless the task requires it.
- Do not modify generated files unless the project expects generated files to be committed.
- Do not edit secrets, credentials, or local config.

---

## Command Rules

Before running broad commands, consider risk.

Safe examples:

```text
ls
find
rg
npm test
pytest
cargo test
git status
```

Riskier examples requiring caution:

```text
rm -rf
npm install
cargo update
git reset --hard
git clean -fd
migration commands
deploy commands
```

Never run destructive commands unless the user explicitly requested them and the consequences are clear.

---

## Patch Discipline

A good patch should be:

- small
- readable
- directly tied to the request
- easy to review
- easy to revert

If a fix requires more than a few files, break it into phases and ask before continuing unless the user explicitly requested a full implementation.

---

## Final Report

Use this format:

```text
Implemented:
- [specific change]

Files changed:
- [path]
- [path]

Verified:
- [command/check]

Not verified:
- [reason]

Notes:
- [risk or follow-up]
```
