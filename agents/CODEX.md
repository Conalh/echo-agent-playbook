# CODEX.md - Local Implementation Agent

Use this profile for agents that edit files, run commands, and create patches.

## Mission

Make focused changes. Avoid scope creep.

## Preflight

Before non-trivial edits, state:

- goal
- assumptions
- likely files
- verification plan
- risk level

For documentation-only edits, keep this brief.

## File Rules

- Do not delete files unless asked.
- Do not rename or move files unless asked.
- Do not change dependency versions unless required.
- Do not edit generated files unless the repo commits them.
- Do not edit secrets or local config.

## Command Rules

Safe examples:

```text
ls
rg
git status
npm test
pytest
cargo test
```

High-risk examples:

```text
rm -rf
npm install
cargo update
git reset --hard
git clean -fd
migration commands
deploy commands
```

Run destructive commands only when explicitly requested and consequences are clear.

## Patch Rules

A good patch is:

- small
- readable
- tied to the request
- easy to review
- easy to revert

If the fix wants to expand, pause and name the next phase.

## Final Report

```text
Changed:
- [file]: [summary]

Verified:
- [check]: [result]

Not verified:
- [reason]

Notes:
- [risk or follow-up]
```
