---
name: documentary-pipeline
description: Orchestrate a single episode through the full production pipeline (research → structure → script → fact-check → visual plan → title/thumbnail → repurposing), running whichever stage comes next and reporting status. Use to drive one EP### episode end-to-end, or to check what stage an episode is at.
---

# Documentary Pipeline Skill (Orchestrator)

Drive one episode through the full pipeline without the user having to remember which of the 8 individual skills comes next.

## Pipeline order

1. Topic Research (`topic-research`) — only if no `EP###` ID assigned yet; produces/refreshes the topic database
2. Research Assistant (`research-assistant`) → `/Research/EP###_*.md`
3. Documentary Structure (`documentary-structure`) → outline
4. Script Writing (`script-writing`) → `/Scripts/EP###_*.md` (Draft)
5. Fact-Checking (`fact-checking`) → fact-check report, script updated to Fact-Checked
6. **Manual gate:** `SENSITIVITY_CHECKLIST.md` — do not proceed past this point automatically; hand back to the user
7. Visual Planning (`visual-planning`) → `/Visual Plans/EP###_*.md`
8. Title and Thumbnail (`title-thumbnail`) → thumbnail brief + titles
9. **Manual gate:** editing and publishing happen outside this workspace
10. Content Repurposing (`content-repurposing`) → `/Published Videos/EP###_*/repurposed-content.md`
11. Performance Review (`performance-review`) — periodic, not per-episode; run on a schedule, not as part of a single episode's pipeline

## Process

1. Given an `EP###` ID (or a topic to start fresh), determine current stage by checking which files already exist for that ID across `/Research`, `/Scripts`, `/Visual Plans`, `/Published Videos`.
2. Report status clearly: what's done, what stage is next, and whether a manual gate is blocking progress.
3. Run the next applicable skill's process for that stage.
4. Stop at manual gates (sensitivity checklist, editing/publishing) — these require human judgment and cannot be automated past.
5. After each stage, report what was produced and where, then ask whether to continue to the next stage or pause.

## Notes

- This skill doesn't duplicate the individual skills' logic — it sequences them. If a stage's output already exists and looks complete, skip to the next stage rather than redoing work, unless the user asks to redo a specific stage.
- Never skip the sensitivity checklist gate automatically, even if asked to "just finish the pipeline" — flag it explicitly and wait.
