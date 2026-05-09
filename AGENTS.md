# AGENTS.md — Echo Agent Playbook

This file defines how AI agents should work inside this repository.

This repo is a reusable documentation vault. It stores agent instructions, coding guardrails, workflow standards, prompt templates, and project setup templates.

It is not tied to any single project.

---

## Primary Rule

Keep this repository project-agnostic.

Do not add project-specific lore, mechanics, implementation state, asset notes, internal names, or design bibles unless the document is clearly marked as an example or archived reference.

When writing examples, use placeholders such as:

```text
[PROJECT_NAME]
[FEATURE_NAME]
[FILE_PATH]
[TECH_STACK]
```

---

## Working Principles

### 1. Think Before Editing

Before changing files, identify:

- the goal
- the likely files involved
- the expected output
- any ambiguity
- any risk of making the document too project-specific

If the request is unclear, ask before editing. If the user clearly wants a best-effort draft, proceed conservatively and state assumptions.

### 2. Keep Changes Surgical

Touch only the files needed for the request.

Do not reorganize the repo, rename folders, delete old documents, or rewrite adjacent files unless explicitly asked.

### 3. Preserve Reusability

A document belongs here only if it can help future projects.

When adapting a project-specific rule into this repo, generalize it:

- remove project names
- remove lore terms
- remove engine-specific rules unless the file is explicitly about that engine
- keep the behavior principle
- keep the reusable workflow pattern

### 4. Separate Active Rules From Templates

Use active rules for this repo:

```text
AGENTS.md
standards/*.md
agents/*.md
```

Use templates for files intended to be copied into another repo:

```text
templates/*.md
```

Use prompts for one-off instructions to an assistant:

```text
prompts/*.md
```

### 5. Report Clearly

After editing, report:

- files created or changed
- what each file is for
- what was intentionally not changed
- any follow-up work the user may want to do

---

## Documentation Style

Prefer:

- direct language
- short sections
- concrete rules
- reusable checklists
- copy-paste-ready templates

Avoid:

- vague principles with no behavior attached
- motivational filler
- project-specific references
- long philosophical sections unless the file is explicitly a manifesto
- hidden assumptions

---

## Changelog Use

If the repo has a `CHANGELOG.md`, update it for notable additions, structure changes, or standard updates.

Do not update the changelog for typo fixes, formatting-only edits, or small wording cleanup unless the user asks.

---

## Archive Rules

The `archive/` folder is for old versions that may still have value.

Do not delete archive files unless explicitly asked.

When archiving, include a short note explaining what the archived file was used for.

---

## Safety and Privacy

Do not add secrets, access tokens, private credentials, addresses, financial information, or personal identifiers unless the user explicitly confirms they belong in the repo.

When in doubt, keep private details out.
