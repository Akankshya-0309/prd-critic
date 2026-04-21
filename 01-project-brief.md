# Project Brief — PRD Critic

## Problem

Writing a good PRD is a learned skill. Junior PMs (and candidates prepping for PM interviews) don't always have a senior reviewer available. Generic LLMs give vague, agreeable feedback ("great structure!") instead of the pointed critique a senior PM would give.

## The user

**Primary:** A PM or PM candidate who has drafted a PRD and wants sharper feedback before sharing it with their lead or an interviewer.

**Secondary:** Engineering or design partners reviewing a PRD and wanting a structured second opinion.

## The job to be done

> "When I finish a PRD draft, I want to know where it's weak, so I can fix it before someone more senior reads it."

## What "good" looks like

A good critique from this tool:

1. **Is specific, not vague.** "The success metric is a vanity metric — DAU doesn't tell you if the feature is working" beats "consider strengthening your metrics."
2. **Cites the draft.** Every critique quotes or references the specific sentence it's reacting to.
3. **Prioritizes.** Not all issues are equal. The critic should flag 2–3 high-priority issues, not 15 nitpicks.
4. **Suggests a fix.** For each issue, a concrete rewrite or question to answer.
5. **Knows what it doesn't know.** If the PRD depends on context the critic can't see (user research, company strategy), it says so explicitly instead of guessing.

## What "bad" looks like (failure modes to watch for)

- Generic praise ("clear problem statement!") with no specifics.
- Nitpicking formatting over substance.
- Inventing context that isn't in the PRD ("your competitors like X are doing Y…") — hallucination.
- Lecturing about PRD structure without engaging with the actual product.
- Being equally harsh on a strong PRD and a weak one (calibration failure).

## Non-goals

- Writing PRDs from scratch (this is a *critic*, not a generator).
- Replacing a human reviewer. The pitch is "better-than-nothing coach," not "fires your PM lead."

## Success criteria for the project itself (not the tool)

By Sunday night, I can:

- Demo the tool live on a fresh PRD in under 2 minutes.
- Point to a rubric I wrote and explain every line.
- Show an eval spreadsheet where I graded the tool on 10 real PRDs.
- Name 2–3 failure modes I found and how I'd fix them with more time.
- Link a 2-page case study from my résumé.
