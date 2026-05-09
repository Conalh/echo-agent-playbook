# Implemented vs Planned

Keep docs honest about what exists.

## Problem

AI-assisted projects often describe future ideas in the same tone as live features.

Future agents then build on false assumptions.

## Labels

Use:

```text
Implemented  Exists and works now.
Partial      Exists, but not fully.
Prototype    Exists only in an isolated demo, branch, or test.
Planned      Intended future work.
Deferred     Intentionally postponed.
Removed      Previously existed, now gone.
Unknown      Needs verification.
```

## Good Example

```md
## CSV Export

Status: Partial.

Implemented:
- Exports the current table.
- Preserves visible filters.
- Downloads a CSV file.

Deferred:
- Scheduled exports.
- Custom column presets.
- Export history.
```

## Bad Example

```md
## CSV Export

The export system supports scheduled exports, custom columns, history, and filtered downloads.
```

If only filtered downloads exist, this is false.

## Agent Rule

Ask:

```text
Would a new contributor know what is real now?
```

If not, split the section into implemented and planned work.

## Design Docs

Design docs may include future ideas.

They still need status labels.
