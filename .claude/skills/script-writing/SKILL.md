---
name: script-writing
description: Draft the narration script for an episode from its research and structure outline, in the channel's conversational Pakistani voice. Use after Documentary Structure has produced an outline.
---

# Script Writing Skill

Turn a research brief and structure outline into an actual narration script.

## Before writing

Read, every time (don't rely on memory from a previous session):
- `CHANNEL_STYLE_GUIDE.md` — voice, tone, and rules
- `GLOSSARY.md` — approved terminology
- The episode's research brief and documentary outline

## Style (from the Style Guide, restated for quick reference)

- Pakistani audience: conversational Urdu + simple English, mixed the way people actually speak
- Explaining to a friend, not lecturing — not academic, not robotic
- Strong first 30 seconds — open on the hook from the outline, never a definition
- Storytelling over listing facts — use the structure's arc
- Explain complex ideas simply, with one concrete example (person, company, household) carrying each abstract concept
- Use analogies from everyday Pakistani life
- Maintain curiosity — open loops, delayed payoffs
- Avoid unnecessary jargon; define what's unavoidable, once, in plain language
- **Neutral on every topic, not just the visibly charged ones.** State facts and let the viewer draw conclusions — this applies uniformly, whether the topic is a nuclear-crisis history, a tariff policy, or something that doesn't look sensitive at all. The narration itself never takes a stance beyond what the sourced facts support; angle and opinion are the user's editorial call to add afterward, not something the draft bakes in by default.

## Section bodies are narration only

**No bracketed cues of any kind inside a section's text — no `[VISUAL NOTE: ...]`, no inline editorial asides, nothing but what gets spoken.** Two things used to live inline in past scripts and no longer do:
- **Visual cues** — don't insert them at all. The Visual Planning skill now reads the pure narration on its own and originates every visual idea itself; it no longer expects pre-seeded hints in the script.
- **Editorial/creative-judgment flags** (e.g. "confirm this framing reads as balanced," a note about a naming inconsistency, a sensitivity call worth a second look) — these still matter, but they go in the **Notes** section at the top of the script file, not inline in the section where they came up. Reference the section name if it helps the user find the spot ("Section 3 — the government-justification paragraph...").

## Every section transition needs a verbal bridge

**Never end one section and open the next with a bare fact or date and no connecting language.** Now that visual cues no longer live in the script, there's nothing left to paper over a rough seam — the narration itself has to carry the listener from one section to the next. A transition is not acceptable if it would confuse someone hearing it read aloud with no visual cut to signal a scene change.

A working bridge is usually one of:
- A connecting phrase ("kuch hafton baad," "lekin," "aur phir") that signals what kind of jump is happening (forward in time, a contrast, a consequence).
- A cause-effect link — the previous section's ending state becomes this section's premise.
- An explicit callback — the previous section promises something ("we'll see this number again"), and the next section delivers on it near its start, not buried three paragraphs in.
- **Explicit time-order signposting whenever a section doesn't pick up chronologically where the last one left off** — if the next section jumps backward or sideways in time from where the narration just was, say so ("Kuch mahine pehle, is dauraan..." / "meanwhile, back in..."). A silent jump to an earlier date right after the previous section ended on a later one is genuinely disorienting, not just stylistically abrupt — catch this while drafting, not after.

After drafting, reread just the last sentence of each section against the first sentence of the next, back to back, with the section headers removed — if it doesn't read as continuous spoken narration, add a bridge before moving on.

## Check runtime before presenting, not after

**Don't let the length mismatch surface for the first time in Visual Planning — catch it here, while it's still cheap to fix.** Once fact-checking has run, expanding the script means redoing that work too.

1. Count narration words per section (same method Visual Planning uses: word count ÷ 140 words/minute, a conservative clear-explainer pace).
2. Sum for a total estimated runtime and compare it against the outline's target length range.
3. If there's a meaningful gap, say so plainly in the script's **Notes** section rather than silently presenting a draft that's obviously short or long — and decide whether to expand/trim now, before the draft goes further, or explicitly accept the shorter/longer runtime (both are legitimate outcomes per the channel's topic-driven length policy).

## Reread for how it sounds spoken, not how it reads on paper

This is audio a host will actually say out loud — a sentence that looks fine as text can still be awkward to speak. Before presenting the draft, reread the whole thing (silently is fine, but read it as if speaking it) specifically checking for:
- Tongue-twisters or clusters of hard-to-say words back to back
- Awkward seams in the Urdu/English code-switching — a clause that would make a speaker stumble over which language they're in
- Sentences that are grammatically fine but don't have a natural spoken rhythm (too many clauses stacked before a breath, an unnatural word order)

Fix what you find. This is a separate pass from the transition check above — that one is about section-to-section flow, this one is about sentence-level speakability.

## Every percentage becomes a 100-rupee illustration

**Never state a raw percentage in the narration without translating it.** A number like "57.5%" or "82%" means nothing felt to a listener on first hearing. Convert it into a concrete count out of 100 rupees — "har 100 rupaye mein se, 58 rupaye..." — every time a percentage would otherwise be spoken.

**If more than one percentage-based split happens in the same episode, they must track ONE continuous 100 rupees — never restart at a fresh 100 for a subset of the first split.** This caused a real, shipped error once: a script split 100 rupees into 42/58, then later said "look at that same 100 rupees again" to describe a formula that actually only applied to the 58 — implying a second, unrelated 100 rupees existed. The fix is to always subdivide the *actual remaining amount*, explicitly reusing it: "un 100 rupayon mein se provinces ko 58 milte hain — ab inhi 58 rupayon mein se, [X] rupaye..." Before presenting a draft with more than one percentage split, trace the rupee amounts through by hand and confirm every subdivision is of a real, previously-stated amount, not a fresh 100.

**When a percentage has been converted to a rupee amount already, don't reintroduce it as a raw percentage later in the same script** (e.g. a callback in the ending) — reuse the same rupee figures instead, so the audience isn't asked to re-translate the same fact twice.

Rupee amounts derived this way (e.g. 58 × 82% ≈ 48) are simple arithmetic on an already-verified percentage, not a new independently-sourced claim — flag them as derived in the **Claims requiring fact-check** list, the same way EP001 flagged its dollar-to-rupee conversions.

## Give every section a narrative reason to keep watching

Two related habits, both aimed at the same problem — a script that's factually solid but reads as a flat timeline instead of a story:
- **At least one open loop beyond the opening hook.** A section ending should sometimes set up something the next section pays off ("...ek sharat thi jo baad mein bohot maayne rakhegi"), not just conclude its own fact and move on. Not every section needs this, but an episode with zero open loops after the hook will feel like a list of facts in order.
- **A genuinely surprising fact gets a setup sentence, not a subordinate clause.** If something breaks the reader's assumption (e.g. a federal official criticizing a policy the federal government owns), give it its own short lead-in ("aur yahan ek dilchasp baat hai...") before the reveal, rather than folding it into a longer sentence where it can slide past unnoticed.

## Every abstract concept gets one concrete anchor, run consistently

Per the Style Guide's "one concrete example" rule — but specifically: pick **one** person/company/household analogy per episode and run it through multiple sections (introduced early, called back at the ending), rather than several different one-off comparisons scattered through the draft. When the research doesn't have a real sourced example, an explicitly illustrative analogy (never presented as a real case, never inventing a specific fact or statistic) satisfies this rule.

## Process

1. Draft section by section, following the outline's structure and section sizing — don't pad a section that the topic doesn't support, don't rush one that needs room.
2. Every factual claim in the narration should trace back to something in the research brief. Do not introduce new facts not present in the research — if something is needed and missing, flag it rather than inventing it.
3. Check terminology against `GLOSSARY.md` as you go. If a new recurring term comes up that isn't in the glossary, propose a rendering and flag it for the user's approval rather than silently deciding.
4. Any editorial or creative-judgment flag goes into the **Notes** section at the top of the script — not inline, not scattered through the sections. Collect these as you draft rather than only at the end. Copy the outline's **spine** (one sentence) into Notes too, so the draft is checkable against its own throughline without opening the outline file separately.
5. Run the runtime check, the read-aloud check, and the percentage/100-rupee continuity check (above) before presenting the draft.
6. At the end, compile a **"Claims requiring fact-check"** list — every number, date, quote, and causal claim stated as fact. This feeds directly into the Fact-Checking skill.
7. Self-check against the Style Guide's "Things to avoid" list before presenting the draft — academic tone, political endorsement, unverified claims stated as fact, clickbait mismatch, and a stance or opinion creeping into the narration on any topic, sensitive-looking or not.

## Output

`/Scripts/EP###_slug-name.md`, using `Templates/script-template.md`, status marked "Draft."

## Notes

- The AI drafts; the user makes final wording, angle, and opinion calls. Present the draft as a draft — flag places where a creative or editorial judgment call is needed rather than silently picking a stance on a contested point. These flags live in the script's own **Notes** section (see above), not inline.
- Don't force every script into the same rhythm. A structure with six tight sections should read differently paced than one with three long sections — let the outline's shape carry through into the prose.
