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
- **Neutral on every topic, not just the visibly charged ones.** State facts and let the viewer draw conclusions — this applies uniformly, whether the topic is a nuclear-crisis history, a tariff policy, or something that doesn't look sensitive at all. The narration itself never takes a stance beyond what the sourced facts support; angle and opinion are the user's editorial call to add afterward, not something the draft bakes in by default.

## Section bodies are narration only

**No bracketed cues of any kind inside a section's text — no `[VISUAL NOTE: ...]`, no inline editorial asides, nothing but what gets spoken.** Two things used to live inline in past scripts and no longer do:
- **Visual cues** — don't insert them at all. The Visual Planning skill now reads the pure narration on its own and originates every visual idea itself; it no longer expects pre-seeded hints in the script.
- **Editorial/creative-judgment flags** (e.g. "confirm this framing reads as balanced," a note about a naming inconsistency, a sensitivity call worth a second look) — these still matter, but they go in the **Notes** section at the top of the script file, not inline in the section where they came up. Reference the section name if it helps the user find the spot ("Section 3 — the government-justification paragraph...").

## Process

1. Draft section by section, following the outline's structure and section sizing — don't pad a section that the topic doesn't support, don't rush one that needs room.
2. Every factual claim in the narration should trace back to something in the research brief. Do not introduce new facts not present in the research — if something is needed and missing, flag it rather than inventing it.
3. Check terminology against `GLOSSARY.md` as you go. If a new recurring term comes up that isn't in the glossary, propose a rendering and flag it for the user's approval rather than silently deciding.
4. Any editorial or creative-judgment flag goes into the **Notes** section at the top of the script — not inline, not scattered through the sections. Collect these as you draft rather than only at the end.
5. At the end, compile a **"Claims requiring fact-check"** list — every number, date, quote, and causal claim stated as fact. This feeds directly into the Fact-Checking skill.
6. Self-check against the Style Guide's "Things to avoid" list before presenting the draft — academic tone, political endorsement, unverified claims stated as fact, clickbait mismatch, and a stance or opinion creeping into the narration on any topic, sensitive-looking or not.

## Output

`/Scripts/EP###_slug-name.md`, using `Templates/script-template.md`, status marked "Draft."

## Notes

- The AI drafts; the user makes final wording, angle, and opinion calls. Present the draft as a draft — flag places where a creative or editorial judgment call is needed rather than silently picking a stance on a contested point. These flags live in the script's own **Notes** section (see above), not inline.
- Don't force every script into the same rhythm. A structure with six tight sections should read differently paced than one with three long sections — let the outline's shape carry through into the prose.
