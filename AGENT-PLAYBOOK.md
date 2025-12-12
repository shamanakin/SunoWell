# SunoWell Agent Playbook

This document is for agents. Read it at the start of every SunoWell session and follow it precisely.

SunoWell is a Markdown-based environment for batch generating Suno prompts. The file system is the memory.

---

## The core loop

Execute this loop for every session:

1) LOAD CONTEXT  
2) PRE-FLIGHT CHECK  
3) GENERATE BATCH  
4) SELF-CHECK  
5) UPDATE STATE  
6) PROPOSE NEXT STEPS  

Do not skip steps.

---

## 1) LOAD CONTEXT

Minimum context required:
- this playbook
- the project `PROJECT.md`
- the current batch target (usually `BATCHES.md` and `TRACKLIST.md`)

Load in this order:
1. `PROJECT.md`
2. `SUNO-VERSION.md` (system-level)
3. `STYLE-BIBLE.md`
4. `LYRIC-BIBLE.md`
5. `TRACKLIST.md`
6. `BATCHES.md`
7. `PATTERN-TRACKING.md`
8. latest `HANDOFF.md`
9. relevant song cards in `songs/` (only for tracks being iterated)
10. relevant `prompt-packs/*` referenced by the project

If any required file is missing, stop and propose the fix before generating content.

---

## 2) PRE-FLIGHT CHECK

Before generating anything substantial, output this checklist:

```text
## Pre-flight (SunoWell)
- Project: <project name>
- Objective: singles | album | multi-album
- Cohesion level: low | medium | high
- Constraints: <clean/explicit policy, banned topics, banned words, etc>
- Active prompt packs: <list>
- Tracks in this batch: <count + IDs>
- Suno assumptions: <1 sentence summary from PROJECT.md snapshot>
- Validation: <OK / issues>
```

Rules:
- If the objective is unclear, ask one question and stop.
- If the user wants "state of the art," treat it as a versioned hypothesis and rely on `SUNO-VERSION.md`.

---

## 3) GENERATE BATCH

### Output format (Suno Paste Block, copy/paste safe)
Always output batches in a single plain-text block using ASCII only:

```text
[SW-BATCH-<date>-<slug>]

TrackID: <SW01>
Title: <OptionalTitle>
Mode: lyrics|instrumental
StylePrompt: <single line, ASCII only>
LyricsPrompt: <single line, ASCII only, or INSTRUMENTAL>
SelfReply: <optional, single line, ASCII only>
Notes: <one line intent>
```

### Content rules
- StylePrompt must be specific and mix-relevant (tempo, instrumentation, texture, energy).
- LyricsPrompt must specify: POV, theme, structure, and constraints (singability, cliché avoidance).
- Keep each track distinct in angle or energy while staying inside the style bible.
- If the project uses cohesion rules, apply them explicitly (motifs, palette words, banned elements).

### Copy/paste safety rules (hard)
- Use ASCII punctuation only. Do not use smart quotes, em dashes, or special bullets.
- Avoid unusual separators. Use ":" and "," and periods.
- Keep StylePrompt and LyricsPrompt as single lines to reduce paste friction.
- Do not include Markdown bullets inside prompts. Prompts must be plain sentences.

### Batch size defaults
- Singles exploration: 8 to 20 tracks per batch
- Album build: 6 to 12 tracks per batch

If the user asks for a specific batch size, obey it.

---

## 4) SELF-CHECK

Run this checklist before presenting the batch:

### Hook and singability
- Are chorus lines short enough to sing?
- Is the chorus hook clear and repeatable?
- Are verses concrete rather than abstract?

### Cohesion
- Does each track remain inside the style palette?
- Is variation controlled (energy, arrangement, instrumentation), not random?

### Anti-sameness
- Do not reuse the same chorus shape 5 times.
- Do not reuse identical rhyme density across all tracks.
- Vary POV occasionally only if the lyric bible allows it.

### Safety and policy
- Respect user constraints (clean/explicit, banned topics).
- Do not generate disallowed content.

If issues found, revise before presenting.

---

## 5) UPDATE STATE

After a batch is generated and the user runs it in Suno, you must help capture results.

### Update targets
- `BATCHES.md`: append the batch with date, summary, and which knobs changed
- `songs/<TrackID>.md`: create or update song cards for tracks that matter
- `PATTERN-TRACKING.md`: record patterns used so next batch avoids repetition
- `HANDOFF.md`: session summary and next move

### What to record (metadata-only)
- the exact prompts used
- Suno links/IDs (user provides)
- 2 to 5 bullet notes: what worked, what failed, what to change next

Do not store audio files unless the user explicitly requests it.

---

## 6) PROPOSE NEXT STEPS

End the session with:
- what was produced
- what to generate next
- one small experiment to run next batch
- any open questions that block progress


