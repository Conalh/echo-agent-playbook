# Changelog Discipline

A changelog records notable changes so future maintainers can understand project movement without reading every commit.

---

## Recommended Format

Use an `[Unreleased]` section until the project has formal versions.

```md
# Changelog

All notable changes to this project will be documented here.

## [Unreleased]

### Added
- New features or new documents.

### Changed
- Behavior changes, structure changes, major wording changes.

### Fixed
- Bug fixes or corrected broken behavior.

### Removed
- Deleted features or files.

### Notes
- Context, documentation syncs, known caveats.
```

---

## What Belongs in the Changelog

Add entries for:

- new features
- new systems
- new documents
- changed workflows
- important bug fixes
- major documentation syncs
- significant UI/presentation changes
- changes that future agents need to know happened

---

## What Does Not Need a Changelog Entry

Usually skip entries for:

- typo fixes
- formatting-only edits
- comment-only edits
- small wording cleanup
- trivial file organization
- experiments that are not committed or preserved

---

## Good Entry Examples

```md
### Added
- Added `PROJECT_MEMORY.md` template for current-state handoffs.
- Added regression-test prompt templates for coding agents.

### Changed
- Reorganized agent instructions into `agents/`, `standards/`, and `prompts/`.

### Fixed
- Corrected README folder map to match the actual repo structure.
```

---

## Bad Entry Examples

```md
- updated stuff
- fixed things
- changed docs
```

A changelog entry should say what changed.

---

## Agent Rule

After notable implementation work, the agent should say whether the changelog was updated.

Example:

```text
CHANGELOG.md was updated under [Unreleased] -> Added.
```

Or:

```text
CHANGELOG.md was not updated because this was an inspection-only task.
```
