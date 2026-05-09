# Changelog Discipline

A changelog records notable movement without making future readers inspect every commit.

## Format

Use `[Unreleased]` until the project has versions.

```md
# Changelog

## [Unreleased]

### Added
- New files or features.

### Changed
- Behavior, structure, or workflow changes.

### Fixed
- Corrected broken behavior or wrong docs.

### Removed
- Deleted files, features, or workflows.

### Notes
- Context or caveats.
```

## Add Entries For

- new features
- new systems
- new documents
- changed workflows
- important fixes
- major documentation syncs
- changes future agents need to know

## Skip Entries For

- typo fixes
- formatting-only edits
- comment-only edits
- small wording cuts
- uncommitted experiments

## Good Entries

```md
### Added
- Added `PROJECT_MEMORY.md` template for current-state handoffs.

### Changed
- Reorganized agent instructions into `agents/`, `standards/`, and `prompts/`.

### Fixed
- Corrected README folder map.
```

## Bad Entries

```md
- updated stuff
- fixed things
- changed docs
```

## Agent Rule

After notable work, report changelog status:

```text
CHANGELOG.md updated under [Unreleased] -> Changed.
```

Or:

```text
CHANGELOG.md not updated because this was inspection-only.
```
