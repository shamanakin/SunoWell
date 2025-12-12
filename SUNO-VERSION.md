# Suno version assumptions (living file)

This file prevents "state of the art" prompting from silently rotting.

When Suno changes behavior, update this file and copy a short snapshot into each active project `PROJECT.md`.

---

## Status

- Last updated: 2025-12-12
- Applies to: latest Suno web app as of this date (treat as heuristic, not certainty)

---

## Prompting posture

Rules of thumb that are robust even as models change:
- Be specific about arrangement and texture, not only genre labels
- Keep tempo and energy clear
- Prefer a tight palette over a long list of descriptors
- Control variation explicitly (what changes track-to-track, what must stay fixed)

---

## Lyrics prompting posture

Lyrics prompts should specify:
- POV (first/second/third)
- theme (one sentence)
- structure (verse/chorus/bridge line counts)
- singability constraints (line length, avoid tongue twisters)
- banned clichés and banned phrases (project-specific)

---

## Common failure modes (and how to mitigate)

These show up across generative music systems:
- Drift from the intended palette  
  Mitigation: tighten tempo range, instrumentation, and banned elements in `STYLE-BIBLE.md`.

- Chorus is not hooky  
  Mitigation: force a 4-line chorus with a repeatable anchor phrase and shorter lines.

- Lyrics feel generic  
  Mitigation: require concrete images, forbid abstract filler, specify 2 to 3 anchor nouns per track.

- Too much sameness across tracks  
  Mitigation: use `PATTERN-TRACKING.md` and rotate chorus shapes and rhyme density.

---

## Project snapshot template (copy into PROJECT.md)

```text
Suno assumptions snapshot (from SUNO-VERSION.md, <date>):
- Style prompts: tight palette, explicit arrangement, explicit energy
- Lyrics prompts: POV + structure + singability constraints
- Iteration: change one knob per batch and record results
```


