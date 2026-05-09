# Documentation Standards

Docs should reduce uncertainty. They should not become a second source of it.

## Source of Truth

Define which file wins when docs disagree.

Common structure:

```text
README.md          Public overview and setup.
AGENTS.md          Agent rules.
PROJECT_MEMORY.md  Current implementation state.
NEXT_STEPS.md      Active handoff.
CHANGELOG.md       Notable changes.
DESIGN.md          Product or design rules, if needed.
```

If files conflict, update the stale file or mark the conflict.

## Implemented vs Planned

Use stable labels:

```text
Implemented
Partial
Prototype
Planned
Deferred
Removed
Unknown
```

Never describe future work as live behavior.

## Current-State Docs

A current-state doc should answer:

- what exists now
- what changed recently
- what is risky
- what is deferred
- what to do next
- what to avoid

## Handoff Docs

A handoff doc should include:

- current goal
- exact next task
- constraints
- test checklist
- do-not-touch list
- suggested prompt

## Design Docs

Design docs should separate:

- user-facing behavior
- system rules
- implementation status
- future ideas

Ambition is fine. Mislabeling is not.

## Changelog Docs

Use changelogs for notable changes, not every edit.

See `CHANGELOG_DISCIPLINE.md`.

## Style

Prefer:

- short sections
- exact terms
- stable labels
- checklists when useful

Avoid:

- vague headings
- long walls of text
- buried warnings
- project-specific assumptions in generic templates

## Review Checklist

- Is the source of truth clear?
- Are implemented and planned items separated?
- Is the next step obvious?
- Are risky areas named?
- Are stale details removed or marked?
- Could a new agent start safely?
