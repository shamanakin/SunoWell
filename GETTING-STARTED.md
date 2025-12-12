# SunoWell Getting Started

This is a short walkthrough for your first SunoWell session.

---

## 1) Create a project

Copy:
`templates/album-project-template/` → `projects/<your-project>/`

If you want singles exploration, you can still use the album template. Just keep `TRACKLIST.md` looser and run smaller batches.

---

## 2) Fill the bibles

Open and fill:
- `PROJECT.md`
- `STYLE-BIBLE.md`
- `LYRIC-BIBLE.md`
- `TRACKLIST.md`

Keep it simple. Specific constraints beat long prose.

---

## 3) Start a Cursor session

Paste into Cursor chat:

```text
Load and follow: ./GIT/sunowell/AGENT-PLAYBOOK.md

Project Location: ./GIT/sunowell/projects/<your-project>/

Generate a batch of 10 tracks.
High cohesion. Controlled variation by energy and arrangement.
Output copy/paste blocks for Suno: StylePrompt + LyricsPrompt per track.
```

---

## 4) Run the batch in Suno

For each track:
1) Paste the StylePrompt
2) Paste the LyricsPrompt
3) Generate
4) Keep the Suno link/ID

---

## 5) Capture results

Return to Cursor and paste:
- Suno links/IDs
- quick notes: which tracks were keepers, which failed, why

Then ask:
"Update state in the project and propose the next batch based on results."

---

## 6) Iterate

You should run a small experiment each batch:
- change one knob
- keep everything else stable

Examples:
- tighten tempo band
- swap the chorus shape
- add a recurring motif phrase
- remove a conflicting texture


