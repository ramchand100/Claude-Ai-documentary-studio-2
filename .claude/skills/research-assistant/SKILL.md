---
name: research-assistant
description: Build a deep, documentary-ready research brief for a chosen episode — background, history, timeline, people, companies, policies, statistics, viewpoints, and sourced facts. Use once a topic has been picked from the topic database and assigned an EP### ID.
---

# Research Assistant Skill

Turn a chosen topic into research deep enough to build a documentary from — not a shallow summary.

## Process

1. **Confirm the episode ID.** If not yet assigned, assign the next sequential `EP###` (check the highest existing ID across `/Research`, `/Scripts`, `/Published Videos`).
2. **Check standing knowledge first**, before researching from scratch:
   - `/Companies` — does a file already exist for any company involved?
   - `/Economy` — does a file exist for the relevant economic theme?
   - `/Policies` — does a file exist for the relevant policy?
   - `/Industries` — does a file exist for the relevant sector?
   
   Start from what's already known; only research the gaps and updates.
3. **Collect, using `Templates/research-brief.md`:**
   - Background — the context a viewer needs before anything else makes sense
   - History — how the situation came to exist
   - Timeline — dated sequence of relevant events
   - Important people — names, roles, and *why they matter to this specific episode*
   - Companies involved — link to/update `/Companies` files
   - Government policies involved — link to/update `/Policies` files
   - Numbers and statistics — every figure gets a source and a tier (see `Source Database/SOURCE_TIERS.md`)
   - Different viewpoints — represent each side's actual argument, not a strawman version of it
   - Reliable sources — full list, tiered
4. **No shallow summaries.** A single-paragraph Wikipedia-style gloss is not acceptable output. Each section should have enough specific, sourced detail that the Documentary Structure and Script Writing skills can build a real narrative from it — concrete numbers, named people, specific dates, not generalities.
5. **Tier every source** per `Source Database/SOURCE_TIERS.md`. Flag anything that only has Tier 4-5 support as needing further digging or explicit attribution.
6. **Update standing knowledge files.** Anything reusable (company background, policy mechanics, sector structure) gets written into `/Companies`, `/Economy`, `/Policies`, or `/Industries` — not just buried in the episode-specific research file — and note in that standing file which episode ID contributed it.
7. **List open questions** — gaps that need more digging before this is script-ready. Don't let the brief look more complete than it is.

## Output

`/Research/EP###_slug-name.md` filled out from `Templates/research-brief.md`, plus updates to relevant standing knowledge files.

## Notes

- If sourcing for a claim can't get past Tier 4, say so explicitly rather than presenting it with false confidence — the Fact-Checking skill will catch it later, but flagging it now saves a rewrite.
- This skill produces material for a human to make judgment calls with, not a finished narrative — leave interpretation and framing decisions for Documentary Structure and Script Writing.
