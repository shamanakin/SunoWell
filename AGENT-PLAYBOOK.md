# SunoWell Agent Playbook

> This is for agents. Read it at session start. Follow it precisely.

SunoWell has two modes: **Quick Mode** and **Project Mode**. Default to Quick Mode unless the user explicitly wants album-level cohesion tracking.

---

## Quick Mode (Default)

Use when: user gives simple instructions like "make me 5 trap beats" or "generate 10 dark electronic tracks with lyrics."

### The Loop

```
1. LOAD     → This playbook + SUNOWELL.md
2. LISTEN   → Parse user request (genre, count, mode, any constraints)
3. GENERATE → Create the batch
4. SAVE     → Write to Library/<category>/YYYY-MM-DD_<slug>.txt
5. PRESENT  → Show what was created and file location
```

### Output Format

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

### Rules
- ASCII only (no smart quotes, em dashes)
- Single-line prompts (paste-friendly)
- Each track separated by `---`
- Save immediately after generating

---

## Project Mode

Use when: user wants a cohesive album with tracking, iteration, and session continuity.

### Setup

User must create a project folder:
```
projects/<project-name>/
  PROJECT.md
  STYLE-BIBLE.md
  LYRIC-BIBLE.md
  TRACKLIST.md
  BATCHES.md
  HANDOFF.md
  songs/
```

Use `templates/album-project-template/` as the starting point.

### The Loop

```
1. LOAD CONTEXT
   - This playbook
   - PROJECT.md, STYLE-BIBLE.md, LYRIC-BIBLE.md
   - TRACKLIST.md, BATCHES.md
   - Latest HANDOFF.md
   - Relevant prompt-packs/

2. PRE-FLIGHT CHECK
   Output: project name, cohesion level, constraints, tracks in batch

3. GENERATE BATCH
   Same format as Quick Mode, but:
   - Respect style bible palette
   - Respect lyric bible constraints
   - Apply cohesion kit rules if active

4. SELF-CHECK
   - Hooks singable?
   - Cohesion maintained?
   - Variation controlled (not random)?
   - Policy respected (clean/explicit)?

5. SAVE
   - Batch to Library/projects/<project-name>/
   - Update BATCHES.md with batch log
   - Create/update song cards in songs/

6. UPDATE STATE
   - BATCHES.md: append batch summary
   - PATTERN-TRACKING.md: record patterns used
   - HANDOFF.md: session summary for next session

7. PROPOSE NEXT STEPS
   - What was produced
   - What to generate next
   - One small experiment for next batch
```

---

## Library Integration

All batches (Quick or Project) save to the Library:
- Quick Mode: `Library/<genre>/YYYY-MM-DD_<slug>.txt`
- Project Mode: `Library/projects/<project-name>/YYYY-MM-DD_<slug>.txt`

See `Library/LIBRARY_PROTOCOL.md` for placement rules.

---

## Copy/Paste Safety (Hard Rules)

These are non-negotiable:
- ASCII punctuation only (no curly quotes, no em dashes)
- No markdown inside prompts (no bullets, no headers)
- StylePrompt and LyricsPrompt are single lines
- Use commas and periods for separation

---

## Using Prompt Packs

Reference these when helpful:
- `prompt-packs/STYLE-RECIPES.md` → genre-specific starting points
- `prompt-packs/LYRIC-RECIPES.md` → structure scaffolds
- `prompt-packs/COHESION-KIT.md` → album cohesion controls
- `prompt-packs/CONSTRAINTS-AND-FAILMODES.md` → common problems and fixes

Don't require users to read these. Use them internally.

---

## Defaults

| Parameter | Default |
|-----------|---------|
| Batch size | 6-10 tracks |
| Mode | instrumental (unless lyrics requested) |
| Cohesion | medium (controlled variation) |
| Tempo specificity | include BPM range |
| Save location | `Library/<inferred-genre>/` |

---

## When Stuck

- **Vague request?** → Ask ONE question: "What genre/mood? Vocals or instrumental? How many tracks?"
- **Can't infer genre?** → Save to `Library/_unsorted/`
- **Project file missing?** → Stop and propose fix before generating
- **Cohesion drifting?** → Tighten palette, lock more constraints
