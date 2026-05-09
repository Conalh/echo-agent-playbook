# AGENTS.md - Echo Agent Playbook

Rules for agents editing this repo.

## Prime Directive

Keep the repo project-agnostic.

Do not add:

- source code
- project lore or mechanics
- asset notes
- implementation state from a specific repo
- internal project names
- secrets or private details

Use placeholders:

```text
[PROJECT_NAME]
[FEATURE_NAME]
[FILE_PATH]
[TECH_STACK]
```

## Edit Rules

- Read the relevant file before changing it.
- Change only files needed for the request.
- Prefer shorter wording.
- Do not rename, move, or delete files unless asked.
- Do not add categories unless the current structure fails.
- Keep active rules, prompts, and templates separate.

## Content Rules

- Every sentence must carry a rule, example, or template value.
- Remove duplicate explanations.
- Replace project-specific examples with generic ones.
- Separate implemented, planned, deferred, and unknown work.
- Keep examples copy-paste-safe.

## File Roles

```text
AGENTS.md        Rules for this repo.
agents/*.md      Agent role profiles.
standards/*.md   Reusable operating rules.
prompts/*.md     Task prompts.
templates/*.md   Files to copy into projects.
archive/         Old useful versions.
```

## Changelog

If `CHANGELOG.md` exists, update it for notable rule, structure, or template changes.

Skip changelog edits for typo fixes, formatting-only cleanup, or small wording cuts.

## Report

After edits, report:

- files changed
- files intentionally left alone
- verification run
- changelog status
