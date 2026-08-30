---
name: script-writing
description: Draft the narration script for an episode from its research and structure outline, in the channel's conversational Pakistani voice. Use after Documentary Structure has produced an outline.
---

# Script Writing Skill

Turn a research brief and structure outline into an actual narration script.

## Before writing

Read, every time (don't rely on memory from a previous session):
- `CHANNEL_STYLE_GUIDE.md` — voice, tone, and rules
- `GLOSSARY.md` — approved terminology
- The episode's research brief and documentary outline

## Style (from the Style Guide, restated for quick reference)

- Pakistani audience: conversational Urdu + simple English, mixed the way people actually speak
- Explaining to a friend, not lecturing — not academic, not robotic
- Strong first 30 seconds — open on the hook from the outline, never a definition
- Storytelling over listing facts — use the structure's arc
- Explain complex ideas simply, with one concrete example (person, company, household) carrying each abstract concept
- Use analogies from everyday Pakistani life
- Maintain curiosity — open loops, delayed payoffs
- Avoid unnecessary jargon; define what's unavoidable, once, in plain language

## Process

1. Draft section by section, following the outline's structure and section sizing — don't pad a section that the topic doesn't support, don't rush one that needs room.
2. Every factual claim in the narration should trace back to something in the research brief. Do not introduce new facts not present in the research — if something is needed and missing, flag it rather than inventing it.
3. Insert lightweight `[VISUAL NOTE: ...]` placeholders inline where a visual is clearly implied by the narration — full detail comes later from the Visual Planning skill, this is just a marker so nothing gets lost.
4. Check terminology against `GLOSSARY.md` as you go. If a new recurring term comes up that isn't in the glossary, propose a rendering and flag it for the user's approval rather than silently deciding.
5. At the end, compile a **"Claims requiring fact-check"** list — every number, date, quote, and causal claim stated as fact. This feeds directly into the Fact-Checking skill.
6. Self-check against the Style Guide's "Things to avoid" list before presenting the draft — academic tone, political endorsement, unverified claims stated as fact, clickbait mismatch.

## Output

`/Scripts/EP###_slug-name.md`, using `Templates/script-template.md`, status marked "Draft."

## Notes

- The AI drafts; the user makes final wording, angle, and opinion calls. Present the draft as a draft — flag places where a creative or editorial judgment call is needed rather than silently picking a stance on a contested point.
- Don't force every script into the same rhythm. A structure with six tight sections should read differently paced than one with three long sections — let the outline's shape carry through into the prose.
