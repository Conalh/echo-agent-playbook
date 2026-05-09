# Bootstrap Repo Prompts

Copy-paste prompts for getting a new repo started with an AI coding assistant.

---

## Empty Documentation Repo

```text
Bootstrap this repository as a project-agnostic documentation repo.

Goal:
Create a clean markdown structure for reusable agent instructions, coding standards, prompt templates, and project setup templates.

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
- Do not infer a tech stack.
- Do not add project-specific lore, mechanics, or implementation notes.
- Keep all docs generic and reusable.
- Use concise markdown.

Verify:
- list final file tree
- confirm no code files were created
- confirm no project-specific content was added
```

---

## Empty Code Project

```text
Bootstrap this repository for [TECH_STACK].

Goal:
Create the smallest working project skeleton that can run locally.

Rules:
- Keep the structure minimal.
- Do not add optional libraries.
- Do not add demo features beyond a basic launch/smoke-test screen.
- Add README.md with setup and run instructions.
- Add AGENTS.md with project-specific coding rules.
- Add CHANGELOG.md with an [Unreleased] section.

Verify:
- run the project if possible
- list commands used
- report any missing dependencies or manual setup
```

---

## Add Agent Docs to Existing Project

```text
Add AI-agent documentation to this existing project.

Create:
- AGENTS.md
- PROJECT_MEMORY.md
- NEXT_STEPS.md
- CHANGELOG.md if missing

Rules:
- Do not change source code.
- Do not invent implementation details.
- Inspect the repo structure first.
- Keep unknowns marked as unknown.
- Use implemented/planned/deferred labels where relevant.

Verify:
- list created files
- summarize what each file contains
- identify any areas needing human confirmation
```
