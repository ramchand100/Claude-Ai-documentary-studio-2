---
name: visual-planning
description: Generate a section-by-section visual plan for a fact-checked script — B-roll, images, maps, charts, animations, archive footage, and editing notes — to make editing faster. Use after fact-checking is complete.
---

# Visual Planning Skill

Turn a fact-checked script into an editing-ready visual plan.

## Process

For **every section** of the script:

1. **B-roll ideas** — what generic or specific footage supports the narration here
2. **Images required** — specific photos needed (people, places, documents, products)
3. **Maps** — where geography matters, specify region/city-level detail needed
4. **Charts** — for any statistic or trend in the narration, specify chart type (line/bar/comparison) and pull the underlying data reference from the research brief or `/Economy` and `/Industries` files
5. **Animations** — where a process or abstract concept needs a simple animated explainer rather than static footage
6. **Archive footage suggestions** — historical topics especially; note where rights/fair-use needs checking
7. **Editing notes** — pacing cues, suggested transitions, on-screen text/lower-thirds

## Process notes

- Replace the script's inline `[VISUAL NOTE: ...]` placeholders with fully specified plan entries — nothing should be left as a vague placeholder in the final plan.
- Match visual density to section pacing: a fast-moving hook section needs quick cuts; a data-heavy section needs a chart that stays on screen long enough to read.
- Flag anything needing licensed footage, paid stock, or a custom-commissioned graphic, so the user can budget time/money for it before the edit.

## Output

`/Visual Plans/EP###_slug-name.md`, using `Templates/visual-plan.md`. This is the file that goes directly to editing.

## Notes

- This skill doesn't touch narration wording — if a visual idea reveals a script problem (e.g. the narration references a chart that doesn't actually exist in the data), flag it back rather than inventing data to fit.
