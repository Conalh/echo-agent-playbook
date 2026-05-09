# Echo Agent Playbook

Reusable AI-agent workflows, coding standards, guardrails, prompts, and documentation patterns for future projects.

This repository is intentionally project-agnostic. It is not a game repo, app repo, lore bible, or source-code archive. It is a small operating manual for getting AI collaborators aligned quickly.

## What Belongs Here

- Agent role instructions
- Coding guardrails
- Documentation standards
- Changelog discipline
- Git workflow notes
- Reusable implementation prompts
- Reusable inspection and regression prompts
- Project setup templates
- Old versions worth keeping for reference

## What Does Not Belong Here

- Project-specific lore
- Project-specific mechanics
- Source code
- Asset files
- Private keys or secrets
- Temporary chat dumps with no reusable value
- Generated images or media assets

## Folder Map

```text
agents/      Role instructions for AI collaborators.
standards/   Reusable coding, docs, Git, and verification rules.
prompts/     Copy-paste task prompts for common workflows.
templates/   Starter markdown files for new projects.
archive/     Older versions kept for reference.
```

## Recommended Reading Order

For a new coding agent:

1. `AGENTS.md`
2. `standards/AGENT_OPERATING_RULES.md`
3. `standards/CODING_GUARDRAILS.md`
4. `standards/DOCUMENTATION_STANDARDS.md`
5. `standards/VERIFICATION_AND_SMOKE_TESTS.md`

For setting up a new project:

1. `templates/PROJECT_README_TEMPLATE.md`
2. `templates/PROJECT_AGENTS_TEMPLATE.md`
3. `templates/PROJECT_MEMORY_TEMPLATE.md`
4. `templates/NEXT_STEPS_TEMPLATE.md`
5. `templates/CHANGELOG_TEMPLATE.md`

For prompting a coding assistant:

1. `prompts/BOOTSTRAP_REPO_PROMPT.md`
2. `prompts/IMPLEMENTATION_PROMPTS.md`
3. `prompts/INSPECTION_PROMPTS.md`
4. `prompts/REGRESSION_TEST_PROMPTS.md`

## Core Principle

The goal is not to make agents sound impressive. The goal is to make them useful, careful, honest, and consistent.

Good agent behavior is usually simple:

- understand the task before acting
- keep scope tight
- avoid speculative architecture
- explain tradeoffs clearly
- verify the result
- document what changed

## Using This Repo

Copy only the files that fit the project. Do not drag the entire playbook into every repo by default.

For most projects, start with:

```text
AGENTS.md
PROJECT_MEMORY.md
NEXT_STEPS.md
CHANGELOG.md
```

Then add project-specific design or technical documents as needed.

## Maintenance Rules

- Keep examples generic unless the file is explicitly personal.
- Keep project-specific docs out of this repo.
- If a rule becomes too specific, move it into a project repo.
- If a rule keeps helping across projects, keep it here.
- Archive older versions instead of deleting them when they may be useful later.
