---
name: topic-research
description: Discover and score Pakistani documentary topic ideas — economy, business, policy, industry, or history — and add them to the topic database. Use when the user wants new video ideas, wants to fill up the idea pipeline, or asks "what should I make next."
---

# Topic Research Skill

Generate documentary ideas for a Pakistani YouTube channel covering economy, businesses, policies, industries, history, and important issues — explained in simple language for ordinary viewers.

## Process

1. **Read `CHANNEL_STYLE_GUIDE.md`** first, to calibrate audience and tone before generating ideas.
2. **Generate candidate topics.** For each, work out:
   - **Title** — working title, not final (Title/Thumbnail skill refines later)
   - **Category** — Economy / Company / Policy / Industry / History / Social Issue
   - **Why it matters** — the concrete, personal reason an ordinary Pakistani should care (not "it's important" — say *how* it touches their life: their bill, their job, their prices, their taxes)
   - **Possible hook** — a specific opening moment, number, or question, not a generic teaser
   - **Expected audience interest** — who specifically this pulls in and why
   - **Research requirements** — what kind of sourcing this will need (see `Source Database/SOURCE_TIERS.md`) and whether that's realistic to get

3. **Score each idea 1-5 on each axis:**
   - **Curiosity** — does the title alone make someone want to click?
   - **Public Interest** — how many ordinary Pakistanis does this actually affect?
   - **Evergreen Value** — will this matter in 2 years, or is it news-cycle disposable?
   - **Storytelling Potential** — is there an actual arc (change, conflict, resolution), or just facts to list?
   - **Research Availability** — can this be sourced credibly (Tier 1-3), on a reasonable timeline?

   Sum for a total out of 25. Don't inflate scores — a mediocre idea scored honestly is more useful than a flattered one.

4. **Bias toward range, not repetition.** Don't propose five variations of the same theme. Mix categories (a company story, a policy explainer, an industry piece, a historical piece) so the channel doesn't calcify into one format — see the "don't make every documentary identical" principle in the workspace root.

5. **Check `Published Videos/*/performance-log.md`** (via the Performance Review skill's findings, if any exist yet) — if certain categories or hook styles have historically overperformed, weight new ideas accordingly, but don't let past performance be the only signal; evergreen public-interest topics deserve slots even if a past similar episode underperformed for unrelated reasons (bad thumbnail, bad timing).

6. **Append to `/Ideas/topic-database.md`**, newest at top, using the existing table format. Do not overwrite existing rows.

## Output

Rows added to the topic database table. Present the new ideas to the user directly too, ranked by total score, so they can pick without opening the file.

## Notes

- Ideas stay in the database even if never picked — this becomes a running record of what's been considered, useful to avoid re-proposing the same idea later.
- When the user picks an idea for production, that's the trigger to assign it the next `EP###` ID (check `/Published Videos`, `/Scripts`, and `/Research` for the highest existing ID) and hand off to the Research Assistant skill.
