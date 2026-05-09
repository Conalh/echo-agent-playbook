# Git Workflow

General Git workflow rules for small AI-assisted projects.

---

## Commit Philosophy

Prefer small commits with clear intent.

A good commit should answer:

```text
What changed?
Why did it change?
```

Avoid giant commits that mix implementation, refactors, docs, and experiments.

---

## Commit Message Format

Use simple imperative messages:

```text
Add coding guardrails document
Update project memory template
Fix README folder map
Refine bootstrap prompt
```

For larger changes:

```text
Add agent playbook starter docs
```

Optional body:

```text
- Adds reusable agent instructions
- Adds coding and documentation standards
- Adds prompt and project setup templates
```

---

## Branching

For solo projects, simple branches are enough.

Examples:

```text
main
feature/import-validation
fix/save-load-crash
docs/agent-playbook
```

Use branches when work may take more than one sitting or might need rollback.

---

## Before Committing

Check:

- `git status`
- changed files are expected
- no secrets are included
- generated junk is not included
- docs match the change
- tests/checks were run when relevant

---

## Files to Watch For

Be careful before committing:

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

Add a `.gitignore` when the project has known generated files.

---

## AI Agent Git Rules

An agent should not:

- commit without being asked
- force push
- reset hard
- delete branches
- rewrite history
- modify `.gitignore` broadly without explaining why

An agent may prepare a commit summary if asked.
