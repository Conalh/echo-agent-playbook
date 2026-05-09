# Echo Agent Playbook

Project-agnostic rules, prompts, and templates for AI-assisted work.

Use this repo to align agents quickly without importing project lore, source code, or stale chat history.

## Use This For

- agent role instructions
- coding and documentation standards
- verification, Git, and changelog rules
- copy-paste prompts
- starter project docs

## Keep Out

- source code
- project lore, mechanics, or asset notes
- secrets, credentials, or personal data
- generated media
- chat dumps with no reusable rule

## Folders

```text
agents/      Agent role profiles.
standards/   Reusable rules for work, docs, Git, and verification.
prompts/     Copy-paste task prompts.
templates/   Starter Markdown files for new projects.
archive/     Old useful versions.
```

## Start Here

New coding agent:

1. `AGENTS.md`
2. `standards/AGENT_OPERATING_RULES.md`
3. `standards/CODING_GUARDRAILS.md`
4. `standards/DOCUMENTATION_STANDARDS.md`
5. `standards/VERIFICATION_AND_SMOKE_TESTS.md`

New project:

1. `templates/PROJECT_README_TEMPLATE.md`
2. `templates/PROJECT_AGENTS_TEMPLATE.md`
3. `templates/PROJECT_MEMORY_TEMPLATE.md`
4. `templates/NEXT_STEPS_TEMPLATE.md`
5. `templates/CHANGELOG_TEMPLATE.md`

Prompting an agent:

1. `prompts/BOOTSTRAP_REPO_PROMPT.md`
2. `prompts/IMPLEMENTATION_PROMPTS.md`
3. `prompts/INSPECTION_PROMPTS.md`
4. `prompts/REGRESSION_TEST_PROMPTS.md`

## Minimal Copy Set

For most projects, copy:

```text
AGENTS.md
PROJECT_MEMORY.md
NEXT_STEPS.md
CHANGELOG.md
```

Add standards only when the project needs stronger agent constraints.

## Maintenance

- Keep examples generic.
- Use placeholders such as `[PROJECT_NAME]`.
- Move project-specific rules into project repos.
- Archive old useful versions instead of deleting them.
- Update `CHANGELOG.md` for notable rule or structure changes.
