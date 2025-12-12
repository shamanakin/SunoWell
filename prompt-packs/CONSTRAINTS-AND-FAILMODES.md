# Constraints and Failmodes (SunoWell prompt pack)

This file is a checklist for preventing common prompt failures and "why did it do that" moments.

---

## Constraint categories (project-level)

Capture constraints in `PROJECT.md`, `STYLE-BIBLE.md`, and `LYRIC-BIBLE.md`.

### Content constraints
- clean vs explicit policy
- banned topics
- banned slurs and hate content
- real-person references (usually avoid)

### Sonic constraints
- tempo band
- primary instrumentation
- banned instrumentation
- mix target (lofi vs modern, wide vs intimate)

### Lyric constraints
- POV
- motif words or phrases
- banned clichés
- rhyme density target (low/medium/high)
- chorus shape rule (4 lines, repeat anchor phrase, etc)

---

## Failure modes and mitigations

### Drift (wrong genre or vibe)
Symptoms:
- instrumentation changes drastically
- tempo feels wrong
- mood flips from track to track

Mitigations:
- tighten tempo band and energy language
- reduce genre labels to 1 to 2 max
- specify 2 to 3 must-have instruments
- add a ban list (no trap hats, no acoustic guitar, etc)

### Overstuffed style prompt
Symptoms:
- muddy output
- inconsistent arrangement

Mitigations:
- remove half the adjectives
- keep only palette, arrangement, mix target

### Chorus is not a hook
Symptoms:
- chorus feels like another verse
- no anchor phrase

Mitigations:
- force a 4-line chorus
- require a repeated anchor phrase
- shorten chorus lines

### Lyrics are generic
Symptoms:
- vague abstractions
- "we will rise" style filler

Mitigations:
- require concrete nouns and actions
- forbid generic motivational phrases
- add 2 to 3 anchor images per track

### Album sounds same in a boring way
Symptoms:
- same chorus shape
- same rhyme density
- same emotional temperature

Mitigations:
- use `PATTERN-TRACKING.md`
- rotate chorus shape across tracks
- vary energy, arrangement density, and vocal intensity within approved range

---

## Rule of one knob

When iterating, change one thing per batch:
- tempo band
- instrumentation emphasis
- chorus shape
- motif phrase
- lyric POV (only if allowed)

Record the change in `BATCHES.md`.


