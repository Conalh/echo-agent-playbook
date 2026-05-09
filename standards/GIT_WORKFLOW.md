# Git Workflow

Rules for small AI-assisted projects.

## Commits

Prefer small commits with one clear intent.

A commit should answer:

```text
What changed?
Why did it change?
```

Use imperative messages:

```text
Add coding guardrails
Update project memory template
Fix README folder map
Refine bootstrap prompt
```

For larger commits, add a short body:

```text
- Adds reusable agent instructions
- Adds documentation standards
- Adds prompt templates
```

## Branches

Use simple names:

```text
main
docs/agent-playbook
feature/import-validation
fix/startup-crash
```

Use a branch when work spans sessions or needs rollback.

## Before Committing

Check:

- `git status`
- changed files are expected
- no secrets are included
- generated junk is excluded
- docs match the change
- relevant checks ran

## Watch Files

Be careful with:

```text
.env
*.key
*.pem
.DS_Store
node_modules/
dist/
build/
.cache/
local settings files
large generated media
```

## Agent Rules

An agent should not:

- commit without being asked
- force push
- reset hard
- delete branches
- rewrite history
- broaden `.gitignore` without reason

An agent may prepare a commit summary when asked.
