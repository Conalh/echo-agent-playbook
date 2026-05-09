# Implemented vs Planned

A reusable standard for keeping project documentation honest.

---

## The Problem

AI-assisted projects often accumulate documents that describe future ideas in the same tone as live features.

That creates confusion.

Future agents may read a planned system as implemented and build on a false assumption.

---

## Required Labels

Use these labels consistently:

```text
Implemented      Exists and works in the current project.
Partial          Exists, but only part of the intended behavior is live.
Prototype        Exists in a test scene, lab, branch, or isolated demo.
Planned          Intended future work, not live.
Deferred         Intentionally postponed.
Removed          Previously existed, now gone.
Unknown          Status needs verification.
```

---

## Good Example

```md
## CSV Export

Status: Partial.

Implemented:
- Exports the current table.
- Preserves active filters.
- Downloads a CSV file.

Deferred:
- Scheduled exports.
- Custom column presets.
- Export history.
```

---

## Bad Example

```md
## CSV Export

The export system supports scheduled exports, custom columns, history, and filtered downloads.
```

If only filtered downloads exist, this is misleading.

---

## Agent Rule

When writing or updating docs, an agent should ask:

```text
Would a new contributor know what is real right now?
```

If not, split the section into `Implemented` and `Planned`.

---

## Design Docs Are Allowed to Dream

Design documents can contain future ideas.

They just need labels.

A good design doc can say:

```md
This is the emotional target.
Current implementation only covers the first-pass version.
The deeper version is deferred.
```

That preserves ambition without confusing implementation.
