# Getting Started with SunoWell

You can be generating music prompts in under 2 minutes.

---

## Quick Mode (Most Users Start Here)

### Step 1: Open in Cursor

Open `GIT/sunowell/` in Cursor (or work within BEOS).

### Step 2: Start a Session

Paste this into Cursor chat:

```text
Load: ./GIT/sunowell/SUNOWELL.md

Generate 8 dark electronic tracks with warm bass, glitchy textures, and nocturnal vibes. Instrumentals only.
```

### Step 3: Get Your Prompts

SunoWell creates a `.txt` file in your Library:
```
Library/electronic/2025-12-13_dark-electronic-glitchy.txt
```

### Step 4: Copy/Paste into Suno

Open the file. Each track is separated by `---`. Copy a StylePrompt, paste into Suno, generate.

Done.

---

## Adding Lyrics

Just ask:

```text
Load: ./GIT/sunowell/SUNOWELL.md

Generate 6 indie pop songs about leaving a toxic job. First-person lyrics, upbeat but bittersweet. Structure: verse-chorus-verse-chorus-bridge-chorus.
```

SunoWell will include both StylePrompt and LyricsPrompt for each track.

---

## Project Mode (For Albums)

When you want cohesive albums with session-to-session tracking:

### Step 1: Create a Project

Copy `templates/album-project-template/` to `projects/<your-album>/`

### Step 2: Fill the Bibles

Edit these files:
- `PROJECT.md` — What you're making
- `STYLE-BIBLE.md` — Sound palette and banned elements
- `LYRIC-BIBLE.md` — Themes, POV, language constraints
- `TRACKLIST.md` — Arc and intent per track

### Step 3: Start a Session

```text
Load: ./GIT/sunowell/AGENT-PLAYBOOK.md

Project: ./GIT/sunowell/projects/<your-album>/

Generate the first batch of 6 tracks. High cohesion, vary energy only.
```

### Step 4: Iterate

After running prompts in Suno:
1. Note which tracks worked
2. Return to Cursor
3. Ask for the next batch based on results

SunoWell tracks patterns, batches, and continuity in your project folder.

---

## Example Requests

**Simple:**
> "Make me 10 lo-fi hip-hop beats"

**Specific:**
> "Generate 8 ambient tracks, 60-70 BPM, evolving synth pads, no percussion, spacious and meditative"

**With Lyrics:**
> "Create 5 dark pop songs about digital addiction. Defiant tone, punchy hooks, modern radio mix."

**Full Album:**
> "I'm making a 10-track concept album about AI consciousness. Cinematic electronic, alternating between tense and hopeful tracks. First-person narrator who is an AI becoming aware."

---

## Folder Reference

```
sunowell/
  SUNOWELL.md       ← Load this for Quick Mode
  AGENT-PLAYBOOK.md ← Full reference for agents
  Library/          ← Your generated prompts live here
  prompt-packs/     ← Recipe modules (optional reference)
  templates/        ← Project templates
  projects/         ← Your album projects
```

---

## Tips

- **Be specific about texture and arrangement**, not just genre labels
- **Include tempo/BPM** for more consistent results
- **Lock more constraints** if cohesion is drifting
- **Check `prompt-packs/STYLE-RECIPES.md`** for genre starting points
- **Everything saves to the Library** — browse it anytime
