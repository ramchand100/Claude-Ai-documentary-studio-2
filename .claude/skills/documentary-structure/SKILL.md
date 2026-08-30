---
name: documentary-structure
description: Analyze a researched topic and recommend the narrative structure that fits it best (not a fixed template) — company story, economic issue, policy explainer, historical piece, or a custom shape. Use after research is done, before scripting.
---

# Documentary Structure Skill

Pick the narrative shape that fits the topic. Never default to one fixed structure — the whole point of this skill is that a company story, a policy explainer, and a historical piece should not sound like the same template with the words swapped.

## Structure library (starting points, not a checklist to force-fit)

- **Company story:** Origin → Problem → Growth → Strategy → Challenges → Future
- **Economic issue:** Everyday problem → Why it happens → Data → Stakeholders → Impact → Solutions
- **Policy:** Why introduced → How it works → Winners → Losers → Future
- **Historical:** Beginning → Turning points → Consequences → Today
- **Custom:** If the topic doesn't fit any of the above cleanly, design a structure that fits it. A scandal/investigation topic might need: The Discovery → What Was Hidden → How It Unraveled → The Reckoning → What Changed. A comparison topic (e.g. two industries, two cities) might need parallel tracks. Don't force a mismatch.

## Process

1. Read the episode's research brief (`/Research/EP###_slug.md`).
2. Identify what kind of story this actually is — not just its category, but its *shape*. A company topic that's really about a founder's downfall is a different shape than a company topic that's about steady, unremarkable growth.
3. Pick the closest-fitting structure from the library, or design a custom one. State the reasoning — why this shape fits this topic — so the choice isn't a black box.
4. Break the structure into concrete sections **sized to what the topic needs**, not to a fixed section count or runtime. A section can be two minutes or seven; state an estimated total length as a range and let the content decide it, per `CHANNEL_STYLE_GUIDE.md`'s length policy (weekly cadence, variable length).
5. Define the **spine** — one sentence: the question this episode answers, or the change it tracks. Every section should serve the spine.
6. Define the **hook** — what the first 30 seconds actually opens on (a person, number, moment, or question — never a definition; see `CHANNEL_STYLE_GUIDE.md`).
7. Define the **ending** — what the viewer is left with, framed as why it matters to them, not a recap of facts covered.

## Output

Fill `Templates/documentary-outline.md` and save it as `/Research/EP###_slug-outline.md`, alongside the episode's research brief. Hand the completed outline to the Script Writing skill.

## Notes

- If recent episodes have all leaned on the same structure (check `/Scripts` for the last 3-4 episodes), actively consider whether that's because the topics genuinely called for it, or because the structure choice is defaulting out of habit. Variety is a channel health signal, not just a nice-to-have.
