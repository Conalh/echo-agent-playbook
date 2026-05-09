# Documentation Prompts

Reusable prompts for writing and maintaining project docs.

---

## Create Project Memory

```text
Create or update PROJECT_MEMORY.md.

Goal:
Provide a compact current-state handoff for future agents.

Include:
- current project loop/state
- implemented systems
- recent changes
- risky areas
- deferred ideas
- do-not-touch list
- next clean pickup

Rules:
- Do not invent implementation details.
- Mark unknowns as unknown.
- Separate implemented from planned.
- Keep it useful for an implementation agent.
```

---

## Create Next Steps

```text
Create or update NEXT_STEPS.md.

Goal:
Give the next agent a precise, safe pickup point.

Include:
- where we left off
- immediate recommended task
- success criteria
- focused checklist
- do-not-touch list
- suggested copy-paste prompt

Rules:
- Prefer stability/readability tasks before expansion if the project is fragile.
- Do not turn the next step into a roadmap.
```

---

## Generalize Project-Specific Rules

```text
Generalize this project-specific instruction into a reusable standard.

Rules:
- Remove project names.
- Remove lore/mechanics.
- Keep the underlying workflow rule.
- Use placeholders where examples are needed.
- Keep it usable across future projects.

Output:
- rewritten generic rule
- note what was removed
```

---

## Sync Docs After Implementation

```text
Sync documentation after the recent implementation.

Focus:
- README if user-facing behavior changed
- PROJECT_MEMORY if current implementation state changed
- NEXT_STEPS if the pickup point changed
- CHANGELOG if the change is notable
- visual/design hook docs if presentation hooks changed

Rules:
- Do not add future ideas unless marked planned/deferred.
- Keep the docs concise.
- Report exactly which docs changed.
```
