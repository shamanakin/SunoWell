# SunoWell for Cursor
## A file-based music lab for Suno. Prompts are the code. The folder is the memory.

If you have ever made a great Suno track and then failed to reproduce the vibe, you do not have a music problem. You have a memory problem.

SunoWell is a Markdown-based system (InkWell-style) that lets you:
- batch-generate Suno style prompts and lyric prompts
- build cohesive albums on purpose (with controlled variation)
- track experiments so you do not repeat the same dead ends
- keep prompting state across sessions with zero tooling

This is built for Cursor. You can still use it anywhere that can read files and follow instructions.

---

## What you get

- `AGENT-PLAYBOOK.md`: the runtime loop the agent follows
- `prompt-packs/`: reusable recipe modules (style, lyrics, cohesion, failmodes)
- `templates/`: album project template + song card template
- `projects/`: your albums and batches live here
- `SUNO-VERSION.md`: versioned assumptions so "best practice" does not rot silently

---

## Quickstart (5 minutes)

1) Open `GIT/sunowell/` in Cursor (or keep BEOS open and work inside this folder).
2) Copy the template:
   - Duplicate `templates/album-project-template/` into `projects/<your-album-name>/`
3) Fill in:
   - `PROJECT.md`
   - `STYLE-BIBLE.md`
   - `LYRIC-BIBLE.md`
   - `TRACKLIST.md`
4) Start a session by pasting this into Cursor chat:

```text
You are operating inside SunoWell for Cursor.
Load and follow: ./GIT/sunowell/AGENT-PLAYBOOK.md

Project Location: ./GIT/sunowell/projects/<your-album-name>/

This session I want:
1) Generate a batch of 8 tracks (style + lyrics prompts) for the next run.
2) Keep cohesion high, but vary energy and arrangement per track.
3) Output the batch in a copy/paste block format for Suno.
```

---

## The loop (why this works)

SunoWell makes the agent do what humans do when they are good at a craft:

1) Load constraints (style bible, lyric bible, tracklist)
2) Generate candidates
3) Evaluate what happened (notes + IDs/links)
4) Iterate intentionally

No magic. Just an explicit memory loop.

---

## Example: copy/paste batch output (3 tracks)

Use this as the format SunoWell will emit. You copy/paste each StylePrompt and LyricsPrompt into Suno.

```text
[SW-BATCH-EXAMPLE-001]

TrackID: SW01
Title: Signal_Repair
StylePrompt:
  Alt-electronic, mid-tempo, crisp drums, warm bass, airy synths, subtle glitch texture, modern mix, melodic, uplifting but tense.
LyricsPrompt:
  Write lyrics in first person. Theme: rebuilding focus after distraction. Structure: Verse 1 (8 lines), Chorus (4 lines hook), Verse 2 (8), Chorus (4), Bridge (4), Final Chorus (4). Use concrete images. Keep lines singable.

TrackID: SW02
Title: Window_Of_Tolerance
StylePrompt:
  Downtempo, cinematic electronic, soft percussion, pulsing sub, sparse piano motifs, intimate, nocturnal, high clarity.
LyricsPrompt:
  Write lyrics as a calm inner monologue. Theme: staying present without numbing. Structure: Verse (10 lines), Chorus (4), Verse (10), Chorus (4), Outro (4). Avoid clichés. Keep it direct.

TrackID: SW03
Title: The_Algorithm_Is_Not_My_God
StylePrompt:
  Dark pop, tight rhythm, punchy drums, hypnotic synth riff, confident vocal space, modern radio mix, controlled aggression.
LyricsPrompt:
  Write lyrics with a defiant tone. Theme: refusing to outsource identity. Structure: Verse (8), Chorus (4), Verse (8), Chorus (4), Bridge (4), Chorus (4). Put the hook in the chorus. Keep rhyme light and natural.
```

---

## Folder map

```text
sunowell/
  README.md
  AGENT-PLAYBOOK.md
  SYSTEM-DESIGN.md
  GETTING-STARTED.md
  HEALTH-CHECK.md
  SUNO-VERSION.md
  prompt-packs/
  templates/
  projects/
```

---

## Cohesion controls (albums that actually stay coherent)

SunoWell uses three layers:
- `STYLE-BIBLE.md`: the sound palette and banned elements
- `LYRIC-BIBLE.md`: POV, themes, language constraints, motifs
- `prompt-packs/COHESION-KIT.md`: controlled-variation knobs that keep it dynamic without drifting

---

## Versioning

Suno changes. Prompting best practice changes with it.

SunoWell keeps a single truth file (`SUNO-VERSION.md`) and each project pins a short "assumptions snapshot" inside `PROJECT.md` so old projects remain reproducible.

---

## License

If you publish this as a repo, MIT is a good default so people can drop it into any workspace.


