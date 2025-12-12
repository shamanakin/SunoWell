# Lyric Recipes (SunoWell prompt pack)

This file contains lyric construction scaffolds for fast, repeatable prompting.

Rule: lyrics prompts must specify POV, theme, structure, and singability constraints.

---

## Lyric prompt format

```text
POV: first | second | third
Theme: <one sentence>
Tone: <2 to 4 adjectives>
Structure: <line counts>
HookRule: <where the hook lives and how it repeats>
LanguageConstraints: <what to avoid, what to include>
```

---

## Recipe: Clean pop structure (verse/chorus/bridge)

LyricsPrompt:
Write lyrics in first person. Theme: <fill>. Tone: <fill>. Structure: Verse 1 (8 lines), Chorus (4 lines), Verse 2 (8), Chorus (4), Bridge (4), Final Chorus (4). HookRule: the chorus contains a short repeatable anchor phrase. LanguageConstraints: keep lines singable, avoid clichés, use concrete images.

---

## Recipe: Story verse with tight chorus

LyricsPrompt:
Write lyrics in first person as a short story. Theme: <fill>. Tone: grounded, vivid, slightly tense. Structure: Verse (12 lines) with clear scene details, Chorus (4 lines) with one anchor phrase repeated, Verse (12), Chorus (4), Outro (4). LanguageConstraints: no abstract filler, use specific nouns and actions.

---

## Recipe: Mantra chorus (high cohesion tool)

Use this when you want album-level cohesion via repeated phrasing.

LyricsPrompt:
Write lyrics in first person. Theme: <fill>. Tone: <fill>. Structure: Verse (8), Chorus (4), Verse (8), Chorus (4), Bridge (4), Chorus (4). HookRule: the chorus repeats the same first and last line each time. LanguageConstraints: short lines, strong vowel sounds, minimal rhyme.

---

## Recipe: Instrumental with title concept

Use this when you want an instrumental track but still want conceptual cohesion.

LyricsPrompt:
INSTRUMENTAL. No vocals. Title concept: <fill>. Mood: <fill>. Keep arrangement consistent with the StylePrompt.

---

## Recipe: Call and response chorus (reply-friendly)

LyricsPrompt:
Write lyrics in second person. Theme: <fill>. Tone: urgent but clear. Structure: Verse (8), Chorus (4) written as call and response lines, Verse (8), Chorus (4), Bridge (4), Chorus (4). HookRule: the first chorus line is the core hook and repeats. LanguageConstraints: keep lines punchy and singable.


