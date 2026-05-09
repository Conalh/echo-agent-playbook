# Documentation Prompts

Prompts for writing and syncing project docs.

## Create Project Memory

```text
Create or update PROJECT_MEMORY.md.

Goal:
Provide a compact current-state handoff.

Include:
- current project state
- implemented systems
- recent changes
- risks
- deferred ideas
- do-not-touch list
- next clean pickup

Rules:
- Do not invent details.
- Mark unknowns.
- Separate implemented from planned.
- Keep it useful for an implementation agent.
```

## Create Next Steps

```text
Create or update NEXT_STEPS.md.

Goal:
Give the next agent a precise pickup point.

Include:
- where work stopped
- immediate task
- success criteria
- checklist
- do-not-touch list
- copy-paste prompt

Rules:
- Prefer stability/readability before expansion if the project is fragile.
- Do not turn next steps into a roadmap.
```

## Generalize Project-Specific Rules

```text
Generalize this project-specific instruction into a reusable standard.

Rules:
- Remove project names.
- Remove lore, mechanics, and private terms.
- Keep the workflow rule.
- Use placeholders where needed.

Output:
- rewritten generic rule
- what was removed
```

## Sync Docs After Implementation

```text
Sync documentation after the recent implementation.

Focus:
- README if user-facing behavior changed
- PROJECT_MEMORY if current state changed
- NEXT_STEPS if pickup changed
- CHANGELOG if the change is notable
- design docs if behavior or status changed

Rules:
- Do not add future ideas unless marked planned/deferred.
- Keep docs concise.
- Report exactly which docs changed.
```
