# Case Study — PRD Critic

> **Publishing tip:** this reads best as a Notion page, a Read.cv post, or a GitHub README. Keep it under 2 pages — hiring managers skim. Every filled-in section should have at least one concrete artifact (screenshot, quote, number). Delete any section where you don't have one.

---

## One-line pitch

> _"An AI PRD critic that scores drafts against an 8-criterion rubric and surfaces the 2–3 priority fixes a senior PM would call out."_

## Why I built this

<!-- 2–3 sentences on what prompted it. Honesty plays better than manufactured gravitas.
Example: "I wanted a sharper signal than friends could give me on PRD drafts for interview prep. Generic LLMs flinched. I set out to make one that didn't." -->

…

## Users & the job

<!-- Who is this for and what job are they hiring it for? Pull from 01-project-brief.md. -->

…

## The product decision that matters most

<!-- Pick ONE decision you made and walk through it. Examples:
- Why I built a critic, not a generator.
- Why the rubric has only 8 criteria, not 20.
- Why I refuse to let the critic nitpick formatting.
- Why the critic must quote the PRD to score it.
Good answers name the tradeoff, not just the choice. -->

…

## The rubric (this is the PM thinking)

<!-- Embed or link 02-prd-rubric.md. Add 2–3 sentences on what you'd change with more time. -->

…

## Prompt design

<!-- Show the system prompt (or link 03-system-prompt.md). Call out 2–3 specific techniques:
- Forced quoting to prevent hallucination
- Priority-fix cap at 2–3 to force prioritization
- "No hedging sandwiches" rule to avoid flinching
- Separate "what's working" section for calibration
-->

…

## Evaluation

<!-- The differentiator. Show your eval spreadsheet. Include:
- n PRDs tested
- Avg calibration gap (|critic score − your score|)
- One table: your scores vs critic scores on the 3 sample PRDs
-->

**Setup:** I scored 10 PRDs myself (including the 3 samples in this kit), then ran the critic on each and recorded its scores.

**Result:**

- Average calibration gap: **[X.X]** points out of 5.
- Biggest agreement: **[criterion]** — critic and I aligned within ≤[X] point on [N/10] PRDs.
- Biggest disagreement: **[criterion]** — critic over-called on weak PRDs, under-called on strong ones.

## Failure modes I found

<!-- The part that proves you did the work. 2–3 concrete failure modes with examples. -->

1. **[Failure mode #1 — e.g., "Invents user research"]**
   - Example: _[quote the critic's hallucinated claim]_
   - Diagnosis: _[what in the prompt let this through]_
   - Fix I'd ship next: _[concrete change to the prompt or rubric]_

2. **[Failure mode #2]**
   …

3. **[Failure mode #3, optional]**
   …

## What I'd do with another week

<!-- 3–5 bullets. Tight. Examples:
- Pipe in a company-style guide so critiques match house tone.
- Add a "PM-level calibration" — APM, PM, senior PM modes.
- Build a self-critique pass: the critic critiques its own output and drops low-confidence points.
- Run a small blind study (3 friends score the critic's feedback vs a human PM's feedback).
-->

…

## What I learned

<!-- 3–4 sentences. Resist the urge to be profound. Things to mention if they're true:
- The rubric was 80% of the product; the prompt was just the delivery mechanism.
- The eval was the only part that made me change my mind about how good it was.
- I initially asked for too much output; forcing "top 3 only" made the critic sharper.
-->

…

## Artifacts

- [Interactive prototype](./08-prototype.html)
- [System prompt](./03-system-prompt.md)
- [Rubric](./02-prd-rubric.md)
- [Eval spreadsheet](./07-eval-template.xlsx)
- [Sample PRDs](./04-sample-prd-weak.md), [medium](./05-sample-prd-medium.md), [strong](./06-sample-prd-strong.md)

---

## For interviewers: a 60-second demo script

> "I'll load a weak PRD and a strong PRD side-by-side. Watch the rubric scores. Watch how the 'priority fixes' change in kind — on the weak PRD the critic goes after the problem statement; on the strong one it goes after an attribution risk buried three sections deep. The tool isn't the point. The calibration is what I built."

<!-- Replace with what you actually want to say. Practice it out loud once. -->
