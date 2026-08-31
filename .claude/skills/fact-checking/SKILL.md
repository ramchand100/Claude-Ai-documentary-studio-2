---
name: fact-checking
description: Extract every factual claim from a drafted script and verify it — statistics, dates, company information, government policies, historical facts — producing a sourced confidence table. Use after a script draft exists, before visual planning.
---

# Fact-Checking Skill

Verify a script before it moves forward. This is a distinct pass from research — research gathers, this checks.

## Tools

Same as the Research Assistant skill: when a claim needs checking against a primary document that's a PDF or sits behind a bot-block, try the Tavily connector's extraction tool (`mcp__Tavily__tavily_extract`) before accepting a weaker secondary source. A claim upgraded from "search-summary" to "directly read the primary document" is exactly the kind of thing that moves a Low/Medium confidence rating to High.

## Process

1. **Extract every claim** stated as fact in the script: statistics, dates, company information, government policy details, historical facts, quotes, and causal statements ("X caused Y").
2. **For each claim, check:**
   - Does it match what's in the episode's research brief and the standing knowledge files (`/Companies`, `/Economy`, `/Policies`, `/Industries`)?
   - What source backs it, and what tier is that source (`Source Database/SOURCE_TIERS.md`)?
   - Is it current, or has it been superseded by a newer figure/event?
3. **Build the claims table** (`Templates/fact-check-report.md`): claim, source, tier, confidence (High/Medium/Low), needs verification (Yes/No), resolution.
   - **High confidence** = Tier 1-2 source, or Tier 3 corroborated by a second independent source.
   - **Medium confidence** = single Tier 3 source, or Tier 4 with clear attribution in the script.
   - **Low confidence** = Tier 4-5 only, or contradictory sources found.
4. **Flag sensitivity candidates** for the user's manual pass through `SENSITIVITY_CHECKLIST.md` — claims about named living people, companies, military/security topics, religious or ethnic/provincial content, or anything currently in litigation. Don't attempt to resolve these yourself; flag and hand off.
5. **Resolve or escalate:**
   - High/Medium confidence claims: mark verified, move on.
   - Low confidence claims: either find a better source, rewrite the script line to attribute it explicitly ("according to X..." / "reportedly..."), or recommend cutting it. Don't silently leave a low-confidence claim stated as flat fact.
6. Update the script file directly with any wording fixes needed (attribution added, a figure corrected), and note the change.

## Output

Fact-check report saved (e.g. `/Research/EP###_slug-factcheck.md` or appended to the research file — keep it alongside the episode's research for traceability), using `Templates/fact-check-report.md`. Script updated in place if fixes were needed, status moved toward "Fact-Checked."

## Notes

- This skill does not replace the user running `SENSITIVITY_CHECKLIST.md` — it feeds that process by surfacing the candidates, but final sensitivity judgment calls are the user's.
- Never mark a claim "Verified" on a single Tier 4-5 source. If that's genuinely the best available sourcing, the claim needs attribution language in the script, not a Verified stamp.
