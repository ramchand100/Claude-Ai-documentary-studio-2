# YouTube Documentary Creator Workspace — Pakistan

A personal AI-assisted production system for a Pakistani documentary YouTube channel covering economy, businesses, policies, industries, history, and important issues in simple language.

This is **not** software. It is a workspace: folders, templates, and Claude Code skills that take an episode from idea to published video, with you making every creative call.

## Pipeline

```
Idea → Research → Story Structure → Script → Fact Check → Visual Plan → Title/Thumbnail → Publish → Repurpose → Review
```

Each stage has a dedicated skill. Run them with `/topic-research`, `/research-assistant`, etc. (see `.claude/skills/`), or run the whole thing end-to-end with `/documentary-pipeline`.

## Episode ID convention

Every episode gets an ID the moment it's picked from the topic database: `EP###_slug-name`, e.g. `EP014_karachi-electric-crisis`.

Use this exact ID as the filename prefix (or subfolder name) in every folder the episode touches: `/Ideas`, `/Research`, `/Scripts`, `/Visual Plans`, `/Published Videos`. This is what makes an episode traceable end to end — grep the ID and you find everything about it.

IDs are sequential and never reused, even if an episode is dropped.

## Folder map

| Folder | Contents |
|---|---|
| `/Ideas` | The topic database (all scored ideas, not just chosen ones) |
| `/Research` | Deep research notes per episode |
| `/Companies` | Standing knowledge base on companies referenced across episodes |
| `/Economy` | Standing knowledge base — macro data, sectors, trends |
| `/Policies` | Standing knowledge base — laws, regulations, government schemes |
| `/Industries` | Standing knowledge base — sector-level context |
| `/Scripts` | Drafted and final scripts per episode |
| `/Visual Plans` | B-roll, chart, map, and animation plans per episode |
| `/Published Videos` | Final metadata: description, thumbnail brief, repurposed content, performance log |
| `/Templates` | Reusable blank templates for every stage |
| `/Source Database` | `SOURCE_TIERS.md` (source credibility ranking) and a running source log |

`/Companies`, `/Economy`, `/Policies`, `/Industries` are **standing knowledge**, not per-episode — an episode's research pulls from and adds to these, so the channel's institutional knowledge compounds over time instead of resetting every video.

## Standing reference files (root)

- `CHANNEL_STYLE_GUIDE.md` — voice, tone, audience, storytelling and language rules, what to avoid. Every script must follow this.
- `GLOSSARY.md` — approved bilingual (Urdu/English) terminology, kept consistent across episodes.
- `SENSITIVITY_CHECKLIST.md` — pre-publish check for military, religious, ethnic/provincial, and legal-risk content. Run before any episode ships.

## Weekly workflow

Cadence is weekly. Length is **not fixed** — a company origin story might run 12 minutes, a policy deep-dive might need 25. The Documentary Structure and Script Writing skills size the outline to what the topic actually needs; don't force a runtime.

A typical week:

**Day 1 — Pick & Research**
- If the topic database (`/Ideas/topic-database.md`) is running low, run `/topic-research` to refill it.
- Pick this week's episode, assign it the next `EP###` ID.
- Run `/research-assistant` on it. Output lands in `/Research/EP###_slug.md`, and updates the relevant standing files in `/Companies`, `/Economy`, `/Policies`, `/Industries`.

**Day 2 — Structure & Script**
- Run `/documentary-structure` to pick the right narrative shape for this topic (not a fixed template).
- Run `/script-writing` to draft. Output lands in `/Scripts/EP###_slug.md`.

**Day 3 — Verify**
- Run `/fact-checking` against the script. Fix anything flagged before moving on.
- Run through `SENSITIVITY_CHECKLIST.md` manually — this is a judgment call, not something to fully automate.

**Day 4 — Visual Plan**
- Run `/visual-planning` on the checked script. Output lands in `/Visual Plans/EP###_slug.md`. Hand this to editing.

**Day 5 — Edit & Package**
- You edit (outside this workspace).
- Run `/title-thumbnail` for titles, hook variants, and thumbnail concepts.
- Fill `video-description` template using the fact-check table and research notes.

**Day 6 — Publish & Repurpose**
- Publish.
- Run `/content-repurposing` for Shorts, carousel, thread, and newsletter versions.
- Log the episode in `/Published Videos/EP###_slug/`.

**Ongoing — Review**
- Weekly or monthly, run `/performance-review` to compare how episodes actually performed against what the Topic Research skill predicted, and feed that back into scoring.

Prefer one command over the six manual steps above? `/documentary-pipeline EP###` walks the same episode through every stage in order and tells you what's next.
