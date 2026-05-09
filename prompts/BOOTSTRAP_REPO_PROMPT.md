# Bootstrap Repo Prompts

Copy-paste prompts for starting or documenting a repo.

## Empty Documentation Repo

```text
Bootstrap this repository as a project-agnostic documentation repo.

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
- Do not add project-specific content.
- Keep docs concise.

Verify:
- list final tree
- confirm no source-code files were created
- confirm no project-specific content was added
```

## Empty Code Project

```text
Bootstrap this repository for [TECH_STACK].

Goal:
Create the smallest working project skeleton that runs locally.

Rules:
- Keep structure minimal.
- Do not add optional libraries.
- Do not add demo features beyond a launch check.
- Add README.md with setup and run instructions.
- Add AGENTS.md with project-specific rules.
- Add CHANGELOG.md with [Unreleased].

Verify:
- run the project if possible
- list commands used
- report missing dependencies or manual setup
```

## Add Agent Docs to Existing Project

```text
Add AI-agent documentation to this project.

Create if missing:
- AGENTS.md
- PROJECT_MEMORY.md
- NEXT_STEPS.md
- CHANGELOG.md

Rules:
- Do not change source code.
- Inspect the repo first.
- Do not invent implementation details.
- Mark unknowns as unknown.
- Separate implemented, planned, and deferred work.

Report:
- files created or changed
- what each file is for
- areas needing human confirmation
```
