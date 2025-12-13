# SunoWell System Design

SunoWell is a Markdown-based system for generating music prompts for Suno with persistence, organization, and iteration discipline.

---

## Design Philosophy

### 1) English as Code
The system logic is expressed as Markdown files. The files are the program. No dependencies, no database, no tooling required.

### 2) Files as Memory
Agents do not "remember." They read state and update it. The Library is the memory. Generated prompts persist as `.txt` files organized by category.

### 3) Recursive Loop
Power comes from repeating:
```
load context → generate → save to library → repeat
```

### 4) Controlled Variation
Good music batches are not random. They vary within a palette. SunoWell encodes the palette (constraints) and the knobs that vary (energy, arrangement, texture).

### 5) Zero Friction Output
Every generated prompt is immediately copy/paste ready for Suno. ASCII only, single-line prompts, no formatting to strip out.

---

## Architecture Overview

### Layer 1: Core System
- `SUNOWELL.md` — Primary activation file (load this)
- `AGENT-PLAYBOOK.md` — Full behavioral specification for agents

### Layer 2: Library (Persistent Memory)
- `Library/` — All generated prompts save here
- `Library/LIBRARY_PROTOCOL.md` — Dynamic organization rules
- `Library/_Index.md` — Browseable index of all content
- Subfolders by genre, mood, or project

### Layer 3: Prompt Packs (Reusable Modules)
- `prompt-packs/STYLE-RECIPES.md` — Genre-specific starting points
- `prompt-packs/LYRIC-RECIPES.md` — Lyric structure scaffolds
- `prompt-packs/COHESION-KIT.md` — Album cohesion controls
- `prompt-packs/CONSTRAINTS-AND-FAILMODES.md` — Common problems and fixes

### Layer 4: Project State (Optional)
- `projects/<name>/` — Full album projects with tracking
- Includes: PROJECT.md, STYLE-BIBLE.md, LYRIC-BIBLE.md, TRACKLIST.md, BATCHES.md, songs/

---

## Data Flow

### Quick Mode
```
User Intent
    ↓
SUNOWELL.md (parse request)
    ↓
Generate Batch
    ↓
Save to Library/<category>/YYYY-MM-DD_<slug>.txt
    ↓
Present to User
```

### Project Mode
```
User Intent + Project State
    ↓
AGENT-PLAYBOOK.md (load bibles, constraints)
    ↓
Generate Batch (respecting palette)
    ↓
Save to Library/projects/<name>/
    ↓
Update Project State (BATCHES.md, HANDOFF.md)
    ↓
Present + Propose Next Steps
```

---

## Why This Solves Real Suno Workflow Problems

### Problem: Prompt Loss
You get a great track. Close the tab. Can't find the prompt.

**Fix:** Every prompt saves to the Library. Browse it anytime.

### Problem: Album Incoherence
Each track drifts to a different genre.

**Fix:** Style bible locks the palette. Cohesion kit controls variation.

### Problem: Iteration Amnesia
You forget which knob caused the improvement.

**Fix:** Batch logs and pattern tracking make experiments explicit.

### Problem: "Best Practice" Rots
Suno changes. What worked last month might not work now.

**Fix:** `SUNO-VERSION.md` stores versioned assumptions. Projects pin a snapshot.

### Problem: Friction
Markdown formatting, special characters, multi-line prompts break when pasted.

**Fix:** ASCII only, single-line prompts, zero formatting to clean up.

---

## Core Files Reference

| File | Purpose |
|------|---------|
| `SUNOWELL.md` | Primary system file — load this |
| `AGENT-PLAYBOOK.md` | Full agent behavioral spec |
| `Library/LIBRARY_PROTOCOL.md` | How the library organizes itself |
| `Library/_Index.md` | Browseable index |
| `prompt-packs/*.md` | Reusable recipe modules |
| `templates/` | Project templates |
| `projects/` | Full album projects |
| `SUNO-VERSION.md` | Versioned Suno assumptions |
