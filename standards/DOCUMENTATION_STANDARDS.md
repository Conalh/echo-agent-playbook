# Documentation Standards

Reusable rules for maintaining useful project documentation.

Good documentation should reduce confusion, not become a second source of confusion.

---

## Source of Truth

Every project should identify which document wins when docs disagree.

Example structure:

```text
README.md             Public overview and setup.
AGENTS.md             Agent instructions and coding rules.
PROJECT_MEMORY.md     Current implementation state.
NEXT_STEPS.md         Current handoff point.
CHANGELOG.md          Notable changes.
DESIGN_BIBLE.md       Canonical design rules, if needed.
```

If two documents disagree, update the stale one or explicitly mark the conflict.

---

## Implemented vs Planned

Always distinguish implemented behavior from planned ideas.

Use clear labels:

```text
Implemented
Planned
Deferred
Not implemented
Prototype only
```

Do not describe future ideas as if they are live.

Do not let aspirational design docs confuse implementation agents.

---

## Current State Docs

A current-state document should answer:

- What exists now?
- What changed recently?
- What is risky?
- What is deferred?
- What should the next agent do?
- What should the next agent avoid?

Keep it updated after meaningful implementation work.

---

## Handoff Docs

A handoff document should include:

- current goal
- exact next task
- constraints
- test checklist
- do-not-touch list
- suggested prompt for the next coding agent

Handoff docs are most useful when they are specific.

---

## Design Docs

Design docs should separate:

- design intent
- user-facing behavior
- system rules
- implementation status
- future ideas

A design doc can be expressive, but it should not lie about what exists.

---

## Changelog Docs

Use changelogs for notable changes, not every typo.

See `CHANGELOG_DISCIPLINE.md`.

---

## Writing Style

Prefer:

- short sections
- concrete examples
- exact terms
- stable vocabulary
- checklists when useful

Avoid:

- vague labels
- huge undifferentiated walls of text
- fake precision
- buried warnings
- project-specific assumptions in generic templates

---

## Documentation Review Checklist

Before considering docs healthy, check:

- Is the source of truth clear?
- Are implemented and planned features separated?
- Is the next step obvious?
- Are risky areas named?
- Are stale details removed or marked?
- Could a new agent start safely from these docs?
