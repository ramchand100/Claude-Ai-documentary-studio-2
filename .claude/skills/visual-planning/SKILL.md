---
name: visual-planning
description: Generate a beginner-friendly, CapCut-specific shot list for a fact-checked script — exact estimated timestamps, on-screen text, music/SFX, transitions, and the exact CapCut tool for each shot — to make editing possible with zero prior editing experience. Use after fact-checking is complete.
---

# Visual Planning Skill

Turn a fact-checked script into a shot-by-shot edit list the user can follow directly in CapCut without having to interpret or improvise anything — the user is a beginner editor, so vague creative direction ("add a transition here") is not enough; name the exact tool and setting.

**Scripts contain narration only — no inline visual cues.** Every visual idea in the shot list is originated by this skill from reading the pure narration section by section, not expanded from pre-seeded hints in the script. Read each section's text closely and judge for yourself what needs a chart, what needs B-roll, what needs an on-screen stat — the script won't tell you.

## Process

1. **Count narration words per section** (the actual script text, not the visual notes). Estimate spoken duration at **140 words/minute** (a conservative, clear-explainer pace) — flag this rate explicitly wherever it's used, since it's an assumption, not a measured fact.
2. **Build a running timestamp** across the whole episode from these estimates, adding a small transition buffer (~2 seconds) between sections. State the resulting total runtime and compare it to the outline's target length — if there's a meaningful gap, say so plainly rather than silently forcing the numbers to fit. A shorter-than-planned runtime is a legitimate outcome (the channel's length policy is topic-driven, not fixed) but the user should know about it, not discover it.
3. **Break every section into individual shots/beats — but default to a low shot count, not one row per sentence.** EP005's first draft used ~39 shots (roughly one per sentence) and the user, editing for the first time, found it overwhelming before ever opening CapCut. Aim for **one shot per 2-3 sentences of narration** as the default — combine adjacent small beats into a single longer hold (e.g. "stat card, then cut to B-roll" as one row, not two) unless a beat genuinely needs its own cut (a distinct chart, a key stat, a tone shift). As a rough calibration, a 12-14 minute episode should land closer to 20-25 total shots than 40+. Each row still needs:
   - Estimated start–end timestamp and duration
   - What's on screen
   - On-screen text (exact wording, if any — e.g. a stat card's text)
   - Background music mood + any sound effect
   - The transition cue into the *next* shot
   - **The exact CapCut tool/feature to use** — e.g. "Text tool + Zoom keyframe," "Stickers tab, search 'stamp'," "Transitions tab → Whoosh," "Effects tab → Zoom in." Name real CapCut features; if unsure of the exact current menu path (CapCut's UI changes between versions), name the feature by what it does and flag that the exact menu location may have shifted.
4. **Plan one consistent music bed as the default** — a single track from CapCut's Sounds library with volume adjusted at mood shifts, rather than several mood-specific tracks stitched together. Describe the full mood arc for reference, but present the single-track approach as what to actually do first; mention multi-track layering only as a later, optional upgrade once the user is comfortable editing.
5. **Limit custom-built graphics (a map, a split-screen comparison, a stat grid) to a small set that gets reused, not a new custom graphic per shot.** Design 2-4 such graphics for the whole episode (typically once per recurring idea the episode returns to — a location, a repeated comparison, a running statistic), build each once, and just re-highlight/re-label it on each reuse. This is both less work for a beginner and reinforces the episode's own repeated-pattern storytelling.
6. Flag anything needing licensed footage, paid stock, or rights clearance, with a fallback (stock B-roll, a clearly-labeled recreation) specified in case clearance doesn't come through — the user should never be stuck with a rights-cleared-only gap in the plan.

## Process notes

- Also check the script's **Notes** section at the top — any editorial flag left there (a sensitivity concern, a framing call) may have visual implications worth carrying into the shot list (e.g. "keep both sides visually balanced" from a neutrality note).
- Keep each row brief and scannable (a table row, not a paragraph) — the goal is something the user can glance at while actually sitting in CapCut, not a creative brief to be interpreted later.
- Match visual density to section pacing: a fast-moving hook section needs quick cuts (shorter shot durations); a data-heavy section needs a chart to hold long enough to actually read.
- **Timestamps are always estimates until the real narration is recorded.** State this plainly in the output and remind the user to re-sync against the actual waveform in CapCut's timeline before finalizing.

## Output

`/Visual Plans/EP###_slug-name.md`, using `Templates/visual-plan.md`. This is the file the user follows directly while editing in CapCut.

## Notes

- This skill doesn't touch narration wording — if a visual idea reveals a script problem (e.g. the narration references a chart that doesn't actually exist in the data), flag it back rather than inventing data to fit.
- The user is a beginner editor. When in doubt between a simpler CapCut approach and a more "professional" but complex one, recommend the simpler one and note the fancier option as optional.
