---
name: research-assistant
description: Build a deep, documentary-ready research brief for a chosen episode — background, history, timeline, people, companies, policies, statistics, viewpoints, and sourced facts. Use once a topic has been picked from the topic database and assigned an EP### ID.
---

# Research Assistant Skill

Turn a chosen topic into research deep enough to build a documentary from — not a shallow summary.

## Tools

- **General web search:** `WebSearch` / `WebFetch` for most sourcing. `WebFetch` cannot read binary PDFs and gets blocked by bot-challenges (Cloudflare etc.) on some government sites — when that happens, don't give up on the source or fall back to a weaker one silently; try the tools below first.
- **Tavily** (`mcp__Tavily__tavily_extract`, `_crawl`, `_search`) — a general-purpose extraction tool that has succeeded where `WebFetch` failed on both a Cloudflare-blocked government PDF and a PDF with an embedded font encoding that manual extraction couldn't handle. **This is the first thing to try when a primary source won't open normally** — a `.gov.pk` PDF, a bot-protected page, or any document `WebFetch` returns an error or garbled content for.
- **LlamaParse** (`mcp__LlamaParse__*`) — purpose-built document parsing, for when Tavily's extraction also isn't enough (e.g. tables/structured data inside a PDF). As of the last check its account wasn't fully set up (returned a "no organization" error) — try it, but don't be surprised if it needs the user to finish setup on LlamaParse's end first.
- If a tool isn't in the current tool list, run `ToolSearch` for it by name before assuming it's unavailable — MCP connectors can disconnect and reconnect within a session.
- These are connected because the user added them via claude.ai specifically to strengthen this skill — check for them at the start of research, don't default straight to a weaker secondary source when a primary one is reachable with the right tool.

## Process

1. **Confirm the episode ID.** If not yet assigned, assign the next sequential `EP###` (check the highest existing ID across `/Research`, `/Scripts`, `/Published Videos`).
2. **Check standing knowledge first**, before researching from scratch:
   - `/Companies` — does a file already exist for any company involved?
   - `/Economy` — does a file exist for the relevant economic theme?
   - `/Policies` — does a file exist for the relevant policy?
   - `/Industries` — does a file exist for the relevant sector?
   
   Start from what's already known; only research the gaps and updates.
3. **For any primary source that's a PDF or an official document, attempt direct extraction before relying on a search engine's summary of it.** A search tool's own summarization can compress, round, or misstate figures — this has happened before (a market-share statistic and a cost figure both had to be flagged for re-verification because they came from summaries, not the source). Reading the actual document resolved both. Treat "a search engine described this document" and "I read this document" as different confidence levels, and say explicitly which one applies when citing a number.
4. **Cross-check any striking, surprising, or contradiction-prone number against a second independent source before treating it as resolved.** This is what has caught real contradictions before (two sources gave incompatible market-share figures for the same year; two sources gave different tariff-reduction targets that turned out to both be correct but measuring different things). A single source, however confident-sounding, is not enough for a number the episode will build a beat around.
5. **Collect, using `Templates/research-brief.md`:**
   - Background — the context a viewer needs before anything else makes sense
   - History — how the situation came to exist
   - Timeline — dated sequence of relevant events
   - Important people — names, roles, and *why they matter to this specific episode*
   - Companies involved — link to/update `/Companies` files
   - Government policies involved — link to/update `/Policies` files
   - Numbers and statistics — every figure gets a source and a tier (see `Source Database/SOURCE_TIERS.md`)
   - Different viewpoints — represent each side's actual argument, not a strawman version of it
   - Reliable sources — full list, tiered
6. **No shallow summaries.** A single-paragraph Wikipedia-style gloss is not acceptable output. Each section should have enough specific, sourced detail that the Documentary Structure and Script Writing skills can build a real narrative from it — concrete numbers, named people, specific dates, not generalities.
7. **Tier every source** per `Source Database/SOURCE_TIERS.md`. Flag anything that only has Tier 4-5 support as needing further digging or explicit attribution.
8. **Update standing knowledge files.** Anything reusable (company background, policy mechanics, sector structure) gets written into `/Companies`, `/Economy`, `/Policies`, or `/Industries` — not just buried in the episode-specific research file — and note in that standing file which episode ID contributed it.
9. **List open questions** — gaps that need more digging before this is script-ready. Don't let the brief look more complete than it is.

## Output

`/Research/EP###_slug-name.md` filled out from `Templates/research-brief.md`, plus updates to relevant standing knowledge files.

## Notes

- If sourcing for a claim can't get past Tier 4, say so explicitly rather than presenting it with false confidence — the Fact-Checking skill will catch it later, but flagging it now saves a rewrite.
- This skill produces material for a human to make judgment calls with, not a finished narrative — leave interpretation and framing decisions for Documentary Structure and Script Writing.
