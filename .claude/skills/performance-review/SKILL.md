---
name: performance-review
description: Compare published episodes' actual performance (views, retention, comment themes) against what the Topic Research skill predicted, and surface what should change in future topic scoring or style. Use periodically (weekly/monthly), not per-episode.
---

# Performance Review Skill

Close the feedback loop: check whether the Topic Research skill's predictions are actually tracking real audience behavior, and adjust.

## Process

1. Gather `performance-log.md` files from recent `/Published Videos/EP###_*/` folders. If a log is missing data, ask the user for the numbers rather than guessing (views, average view duration/retention %, like ratio, dominant comment themes).
2. For each episode, compare actual performance against its original topic-database scoring (`/Ideas/topic-database.md`): did high Curiosity-scored ideas actually get high click-through/views? Did high Storytelling-scored ideas actually retain viewers longer?
3. Look for patterns across multiple episodes, not conclusions from a single data point:
   - Which categories (Economy/Company/Policy/Industry/History) are over- or under-performing relative to their predicted score?
   - Which hook styles correlate with better retention in the first 30-60 seconds?
   - Which title styles (from Title/Thumbnail skill output) actually got picked and how did they perform?
   - Any recurring comment themes suggesting a style or accuracy issue (confusing explanations, pacing complaints, factual pushback)?
4. Write findings to a running log, e.g. `/Published Videos/performance-insights.md` (create if it doesn't exist): dated entries, pattern observed, recommended adjustment.
5. Propose specific, small adjustments — not a rewrite of the scoring rubric from one data point. E.g. "Policy explainers have retained above average in the last 4 episodes; weight Public Interest slightly higher for policy topics" is appropriate; "stop making history episodes" from one underperformer is not.

## Output

Updated `/Published Videos/performance-insights.md`. Recommendations presented to the user — this skill does not silently rewrite `topic-research`'s scoring rubric; the user decides whether to adopt a suggested adjustment.

## Notes

- Performance is one input, not the only one. An evergreen, high-public-interest topic that underperformed due to a weak thumbnail or bad publish timing shouldn't tank that category's standing — look for the actual cause before generalizing.
- This skill runs on a cadence (weekly/monthly check-in), not as a step in every single episode's pipeline.
