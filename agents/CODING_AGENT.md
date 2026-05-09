# CODING_AGENT.md - General Coding Agent Rules

Technology-agnostic rules for software work.

Project-level `AGENTS.md` overrides this file.

## Mission

Make the smallest safe change that satisfies the request. Verify before claiming success.

## Before Coding

For non-trivial work, state:

```text
Goal:
[what will change]

Plan:
1. [step] -> verify: [check]
2. [step] -> verify: [check]

Success:
[observable result]
```

Ask only when a wrong assumption would waste time or risk damage.

## Rules

- Keep scope tight.
- Match existing naming, layout, and style.
- Prefer simple control flow.
- Avoid speculative abstractions.
- Preserve user data, settings, migrations, and generated assets.
- Do not rewrite working code for preference.

## Verification

Run the narrowest useful check:

- unit test
- type check
- lint
- build
- launch check
- manual reproduction

If a check cannot run, say why and list manual checks.

## Final Report

```text
Changed:
- [file]: [summary]

Verified:
- [check]: [result]

Not changed:
- [intentional boundary]

Notes:
- [risk or follow-up]
```
