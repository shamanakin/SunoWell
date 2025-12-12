# SunoWell Health Check

Use this to verify SunoWell is set up correctly before a session.

---

## System files present

Required:
- `README.md`
- `AGENT-PLAYBOOK.md`
- `SYSTEM-DESIGN.md`
- `GETTING-STARTED.md`
- `HEALTH-CHECK.md`
- `SUNO-VERSION.md`

Required folders:
- `prompt-packs/`
- `templates/`
- `projects/`

---

## Project files present

For a project at `projects/<name>/`, required:
- `PROJECT.md`
- `STYLE-BIBLE.md`
- `LYRIC-BIBLE.md`
- `TRACKLIST.md`
- `BATCHES.md`
- `PATTERN-TRACKING.md`
- `DECISIONS.md`
- `HANDOFF.md`
- `songs/` folder

---

## Prompt pack references valid

If `PROJECT.md` lists active prompt packs, verify those files exist under `prompt-packs/`.

---

## Suno assumptions pinned

Verify:
- `SUNO-VERSION.md` has a last-updated date
- `PROJECT.md` contains a short "Suno assumptions snapshot" copied from `SUNO-VERSION.md`

---

## If anything is missing

Stop and fix structure first. Do not generate prompts on a broken state layout.


