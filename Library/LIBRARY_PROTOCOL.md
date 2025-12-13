# SunoWell Library Protocol

> The library organizes itself. Your prompts persist. Nothing gets deleted.

---

## Purpose

This library stores all batch-generated music prompts as `.txt` files, organized dynamically by genre, mood, project, or whatever structure emerges from use.

The agent manages the library. You don't have to.

---

## The One Rule

**Never delete prompt files.**

- Folders can be created, renamed, merged, or archived.
- Files can be moved between folders.
- Nothing gets deleted. Ever.

If a prompt is outdated or bad, archive it. Don't delete it.

---

## Output File Format

Every generated batch becomes one or more `.txt` files:

```
Library/
  <category>/
    YYYY-MM-DD_<slug>.txt
```

### File Contents (Copy/Paste Ready)

```text
[SUNOWELL BATCH: <date>-<slug>]

---

TrackID: SW01
Title: <Title>
Mode: lyrics | instrumental

StylePrompt:
<single line, ASCII only, comma-separated descriptors>

LyricsPrompt:
<single line or INSTRUMENTAL, ASCII only>

---

TrackID: SW02
...
```

### Critical Rules
- ASCII only. No smart quotes, em dashes, or special characters.
- StylePrompt and LyricsPrompt are single lines (no bullets or markdown).
- Each track separated by `---`.
- File is immediately copy/paste ready for Suno.

---

## Placement Decision Tree

When saving a new batch:

1. **User specifies a category/folder?** → Use it (create if needed).
2. **Batch has a clear genre anchor?** → Use or create genre folder (e.g., `electronic/`, `hip-hop/`, `ambient/`).
3. **Batch is project-specific?** → Use or create project folder (e.g., `album-signals/`, `project-therapy-beats/`).
4. **Unclear or exploratory?** → Place in `_unsorted/`.

---

## Folder Naming Conventions

- Lowercase, hyphens for spaces: `dark-pop`, `lo-fi-beats`, `cinematic-ambient`
- No special characters
- Be specific but not verbose: `electronic` not `electronic-music-general`

---

## Folder Lifecycle

### Creating
When the library needs a new category, create it with a `.gitkeep` or first file.

### Renaming
When a folder name no longer fits, rename it. Update any project references.

### Merging
If two folders overlap heavily:
1. Decide on the surviving name
2. Move all files to the survivor
3. Delete the empty folder

### Archiving
Move stale or experimental batches to `_archive/<original-folder>/`.

---

## Library Index

Maintain `_Index.md` at the library root:
- List all folders with 1-line descriptions
- Update when structure changes
- Include "Recent Additions" section

---

## Changelog

Track structural changes here (not file additions):

```
DATE       | ACTION   | DETAILS
-----------|----------|------------------------------------------
2025-12-13 | INIT     | Library initialized with core structure.
```

