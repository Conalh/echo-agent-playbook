# Coding Guardrails

Reusable coding principles for AI-assisted development.

These rules are meant to prevent the common failure modes of coding agents: overbuilding, guessing, refactoring too much, and failing to verify.

---

## 1. Think Before Coding

Do not jump straight into edits.

Before implementation, identify:

- the goal
- the assumptions
- the affected files or systems
- the simplest approach
- the verification plan

If the task is ambiguous, surface the ambiguity.

If there is a simpler approach than the user's implied approach, say so before building.

---

## 2. Simplicity First

Write the minimum code that solves the current problem.

Prefer:

- clear functions
- direct data flow
- local fixes
- existing patterns
- boring readable code

Avoid:

- speculative architecture
- framework-like abstractions for one feature
- unused configuration
- clever generic helpers
- premature optimization
- defensive code for impossible states

The test:

```text
Would a senior maintainer call this overcomplicated?
```

If yes, simplify.

---

## 3. Surgical Changes

Touch only what the request requires.

Do not:

- refactor adjacent systems
- rename unrelated variables
- change file layout
- rewrite working code
- clean up unrelated style issues
- delete unused code without approval

If unrelated cleanup is worth doing, mention it as a follow-up.

---

## 4. Goal-Driven Execution

For multi-step tasks, define success before writing code.

Example:

```text
Goal:
Add a one-time reward panel after a completed route node.

Success:
The panel appears once, grants the selected reward, cannot be claimed twice, and does not affect unrelated route nodes.

Plan:
1. Add reward state -> verify node can be marked claimed.
2. Show panel from route completion -> verify it appears after success.
3. Add claim guard -> verify repeated visits do not duplicate rewards.
```

---

## 5. Match Existing Architecture

The best implementation usually looks like it was already part of the project.

Follow:

- existing naming
- existing file placement
- existing control flow
- existing data ownership
- existing test style

Do not introduce a new architectural style casually.

---

## 6. Keep Data Ownership Clear

Know which object owns the state.

Avoid scattering state across UI nodes, helper classes, and global singletons unless the project already uses that model.

General rule:

```text
Core systems own state.
UI displays state and emits user intent.
Parent systems coordinate children.
```

---

## 7. Do Not Hide Mechanics in Presentation

Presentation code should not secretly own gameplay rules.

If visual behavior affects logic, it should be explicit and documented.

---

## 8. Verify the Narrow Path First

After coding, verify the exact behavior that changed before testing broad scenarios.

Then verify likely regressions.

---

## 9. Report What Was Not Done

A useful implementation report includes boundaries.

Example:

```text
Not changed:
- Did not alter scoring math.
- Did not add new reward types.
- Did not refactor the route graph.
```

This prevents false assumptions and keeps future work cleaner.
