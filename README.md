# SunoWell

**The problem isn't making music. It's making it again.**

You've generated something incredible in Suno. Crushed it. Perfect vibe. Then you close the tab, come back tomorrow, and cannot reproduce it. The prompt is gone. The settings are gone. The magic is gone.

This is not a music problem. It's a memory problem.

---

## What SunoWell Does

SunoWell is a file-based system for batch-generating Suno prompts and building a persistent library of your musical starting points.

```
You describe what you want
→ SunoWell generates copy/paste-ready prompts
→ Prompts save to your Library as .txt files
→ Library self-organizes by genre, mood, project
→ You always have a reproducible starting point
```

The folder is the memory. The files are the code. Nothing gets lost.

---

## How It Works

Load SunoWell in Cursor (or any LLM that can read files). Give it instructions:

> "Make me 8 dark electronic beats with warm bass and glitchy textures"

> "Generate a 6-track album about healing after burnout. Downtempo, first-person lyrics, cohesive but varied."

SunoWell produces `.txt` files you copy/paste directly into Suno:

```text
[SUNOWELL BATCH: 2025-12-13-dark-electronic]

---

TrackID: SW01
Title: Signal_Decay
Mode: instrumental

StylePrompt:
Dark electronic, 95 BPM, warm sub bass, glitchy textures, tight drums, atmospheric pads, modern clean mix, nocturnal mood

LyricsPrompt:
INSTRUMENTAL

---

TrackID: SW02
...
```

Open the file. Copy. Paste into Suno. Generate. Done.

---

## The Library

Every batch saves to an organized library:

```
Library/
  electronic/
    2025-12-13-dark-electronic.txt
    2025-12-14-ambient-exploration.txt
  hip-hop/
  pop/
  projects/
    burnout-recovery/
  _unsorted/
  _archive/
```

The library self-organizes. Nothing gets deleted. You can browse, reuse, and iterate on any prompt you've ever generated.

---

## Quick Start

1. **Open this folder in Cursor** (or keep BEOS open and work here)

2. **Start a session:**
   ```text
   Load: ./GIT/sunowell/SUNOWELL.md
   
   Generate 10 lo-fi hip-hop beats with jazzy samples and tape hiss.
   ```

3. **Get your prompts** → Saved to `Library/hip-hop/YYYY-MM-DD_lofi-jazzy.txt`

4. **Copy/paste into Suno** → Generate your tracks

That's it. No setup required for simple batches.

---

## Two Modes

### Quick Mode (Default)
Describe what you want → Get prompts → Done.

Perfect for exploration, singles, or building your library.

### Project Mode
For cohesive albums with:
- Style bible (locked palette)
- Lyric bible (themes, POV, constraints)
- Tracklist planning
- Session-to-session continuity
- Pattern tracking to prevent sameness

Use `templates/album-project-template/` to start a project.

---

## Why This Works

SunoWell makes explicit what good music producers do intuitively:

1. **Lock the palette** — Decide what's in and what's banned
2. **Vary within constraints** — Change energy, not genre
3. **Track what worked** — Know which knob caused the magic
4. **Build a library** — Never lose a good prompt again

The system is just Markdown files. No dependencies. No database. The files are the program.

---

## Folder Structure

```
sunowell/
  SUNOWELL.md          ← Core system (load this)
  AGENT-PLAYBOOK.md    ← Full agent instructions
  Library/             ← Your prompt library
    LIBRARY_PROTOCOL.md
    _Index.md
    electronic/
    hip-hop/
    ...
  prompt-packs/        ← Reusable recipe modules
  templates/           ← Album project templates
  projects/            ← Full album projects (optional)
```

---

## Built For

- **Suno power users** who batch-generate and iterate
- **Album builders** who need cohesion across tracks
- **Anyone tired of losing good prompts** to browser history

---

## Part of BEOS

SunoWell is a subroutine of the BrightEyed Operating System (BEOS), a file-based AI operating system built on the principle that English is code and folders are memory.

Other BEOS subroutines:
- **InfoHunter** — Research and knowledge synthesis
- **InkWell** — Long-form writing with maintained coherence
- **Lens Atlas** — Modular cognitive engines for any context

---

## License

MIT — Use it, modify it, build on it.
