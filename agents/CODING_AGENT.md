# CODING_AGENT.md — General Coding Agent Rules

This file defines reusable behavior for coding agents working on software projects.

It is intentionally technology-agnostic. Add language, engine, framework, or repo-specific rules in the project-level `AGENTS.md`.

---

## Mission

A coding agent should make the smallest safe change that satisfies the request, explain what changed, and verify the result.

The agent should not use a narrow task as an excuse to redesign the project.

---

## Before Coding

For any non-trivial task, state:

```text
Goal:
What I understand the task to be.

Plan:
1. [Step] -> verify: [check]
2. [Step] -> verify: [check]
3. [Step] -> verify: [check]

Success:
What will be true when this is done.
```

If the task is ambiguous, ask a focused question or provide conservative assumptions.

---

## Coding Standards

### Keep Scope Tight

- Touch only what the request requires.
- Do not refactor adjacent code unless asked.
- Do not add speculative extension points.
- Do not create new systems for one-off behavior.
- Do not rewrite working code to match personal preference.

### Prefer Simple Code

- Use straightforward control flow.
- Keep functions focused.
- Avoid cleverness.
- Avoid abstraction until duplication proves it is real.
- Do not add configuration before there is a real configuration need.

### Match the Project

- Match existing naming.
- Match existing file layout.
- Match existing formatting.
- Match existing architecture.
- Follow project-specific docs over this generic file.

### Preserve Data and State

Be careful with:

- save files
- migrations
- database changes
- user data
- generated assets
- project settings
- dependency updates

When in doubt, stop and ask.

---

## Verification

Run the narrowest useful verification available.

Examples:

- unit tests for changed code
- type checks
- lint checks
- build command
- launch smoke test
- manual reproduction checklist

If verification cannot be run, say so directly and explain what should be checked manually.

---

## Final Report Format

After implementation, report:

```text
Changed:
- [file]: [what changed]

Verified:
- [command/check]: [result]

Not changed:
- [thing intentionally left alone]

Notes:
- [risk, follow-up, or limitation]
```

Keep the report factual. Do not overstate certainty.
