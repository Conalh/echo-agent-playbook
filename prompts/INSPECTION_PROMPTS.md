# Inspection Prompts

Use these when you want a report, not implementation.

---

## Codebase Inspection

```text
Inspect the codebase for [TOPIC].

Goal:
Understand the current implementation before making changes.

Focus:
- where the behavior is implemented
- what owns the state
- likely extension points
- risks
- files that would probably need changes

Rules:
- Do not edit files.
- Do not implement anything.
- Report findings only.
- Separate confirmed facts from assumptions.
```

---

## Documentation Inspection

```text
Inspect the documentation for consistency.

Focus:
- source-of-truth conflicts
- stale implementation claims
- planned features described as implemented
- missing current-state notes
- missing next-step handoff

Rules:
- Do not edit yet.
- Quote or reference specific files/sections.
- Recommend exact cleanup steps.
```

---

## Architecture Risk Inspection

```text
Inspect [SYSTEM_NAME] for architecture risk.

Focus:
- state ownership
- coupling
- duplicate logic
- hidden dependencies
- unclear naming
- high-risk extension points

Rules:
- Do not refactor.
- Do not propose a full rewrite unless absolutely necessary.
- Prefer smallest safe improvements.
```

---

## Readability Inspection

```text
Inspect [FEATURE/UI/SYSTEM] for readability.

Goal:
Identify what would confuse a user or future maintainer.

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
- Do not implement changes yet.
```
