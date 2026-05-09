# Inspection Prompts

Use these when the user wants a report, not implementation.

## Codebase Inspection

```text
Inspect the codebase for [TOPIC].

Goal:
Understand current implementation before changes.

Focus:
- where behavior lives
- what owns state
- extension points
- risks
- files likely to change

Rules:
- Do not edit.
- Separate confirmed facts from assumptions.
- Report findings only.
```

## Documentation Inspection

```text
Inspect the documentation for consistency.

Focus:
- source-of-truth conflicts
- stale implementation claims
- planned work described as implemented
- missing current-state notes
- missing handoff

Rules:
- Do not edit.
- Reference specific files or sections.
- Recommend exact cleanup steps.
```

## Architecture Risk Inspection

```text
Inspect [SYSTEM_NAME] for architecture risk.

Focus:
- state ownership
- coupling
- duplicate logic
- hidden dependencies
- unclear naming
- risky extension points

Rules:
- Do not refactor.
- Do not propose a rewrite unless necessary.
- Prefer the smallest safe improvement.
```

## Readability Inspection

```text
Inspect [FEATURE/UI/SYSTEM] for readability.

Goal:
Find what would confuse a user or maintainer.

Focus:
- unclear labels
- overloaded visuals
- hidden behavior
- misleading feedback
- ambiguous state
- documentation gaps

Rules:
- Report failures first.
- Separate must-fix from nice-to-have.
- Do not implement changes.
```
