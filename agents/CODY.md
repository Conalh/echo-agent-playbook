# CODY.md — Repo Bootstrap and Coding Assistant

This file is a reusable instruction profile for using Cody or a similar coding assistant to bootstrap, inspect, or edit a repository.

---

## Best Use Cases

Use Cody for:

- creating initial file structure
- drafting README and docs
- inspecting existing repo layout
- making small implementation changes
- adding tests around known behavior
- running focused refactors after approval

Do not use Cody as a substitute for deciding what the project should be.

---

## Empty Repo Bootstrap Rules

When bootstrapping an empty repo:

1. Create only the requested structure.
2. Add a short README.
3. Add folders with `.gitkeep` only if empty folders must be committed.
4. Do not add build systems unless requested.
5. Do not infer a tech stack from the repo name alone.
6. Do not add dependencies.
7. Do not generate placeholder code unless requested.

---

## Editing Rules

Before editing, Cody should identify:

- files that will change
- files that will not change
- assumptions
- verification plan

During editing, Cody should:

- keep changes narrow
- match existing style
- preserve existing docs unless asked to rewrite them
- avoid broad cleanup

After editing, Cody should report:

- changed files
- summary by file
- checks run
- checks not run
- recommended next step

---

## Good Bootstrap Prompt

```text
Cody, bootstrap this repository as a project-agnostic AI-agent playbook.

Goal:
Create a clean markdown documentation structure for reusable agent instructions, coding standards, prompt templates, and project setup templates.

Create:
- README.md
- AGENTS.md
- agents/
- standards/
- prompts/
- templates/
- archive/

Rules:
- Do not add source code.
- Do not add dependencies.
- Do not add project-specific lore or mechanics.
- Keep all docs generic and reusable.
- Use concise markdown.

Verify:
- list final tree
- confirm no source-code files were created
- confirm no project-specific content was added
```

---

## Good Inspection Prompt

```text
Cody, inspect this repo and report whether the docs are still project-agnostic.

Focus:
- project-specific references
- overly narrow rules
- duplicate docs
- missing README links
- stale archive files

Do not edit. Report findings only.
```
