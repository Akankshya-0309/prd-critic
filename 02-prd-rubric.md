# PRD Rubric

This is the rubric the critic uses. Edit freely — a rubric you can *defend* in an interview is worth far more than one you copy-pasted. The headings are the minimum; feel free to rename, merge, or weight them differently based on the PM culture you want to signal.

Each criterion is scored 1–5:

- **1 — Missing or wrong.** The PRD doesn't address this, or gets it actively wrong.
- **2 — Weak.** Addressed but vague, unsupported, or confused.
- **3 — Adequate.** A reasonable take. A senior PM wouldn't reject it, but wouldn't praise it either.
- **4 — Strong.** Clear, specific, and defensible.
- **5 — Exceptional.** Reframes the problem or surfaces an insight most PMs would miss.

---

## 1. Problem clarity (weight: high)

Is the problem stated in terms of a *user's* situation, not a solution or a feature?

- Does it name the user and the moment of pain?
- Could a reader state the problem in one sentence after reading the section?
- Does it avoid describing the feature as if it were the problem? (Red flag: "Users need a button to…")
- The problem statement must be clear for what the PRD aims to achieve to solve rather than directly jump to solutioning 

## 2. Evidence & grounding (weight: high)

Is there evidence this problem is real and worth solving?

- Qualitative: quotes, research, usage observations.
- Quantitative: funnel drop-offs, support ticket volume, segment sizes, market research analysis from internal or external sources like customer questions, or industry analyst reports.
- Does the PRD distinguish between "we assume" and "we've verified"?
- Assumptions that are taken for the PRD must be clearly called out too in a separte section

## 3. Target user & segmentation (weight: medium)

Is the target user specific enough to make tradeoffs?

- "Power users of our analytics dashboard who run >5 reports/week" beats "our users."
- Does the PRD name who this is *not* for?
- PRD also needs to define what is the expected outcome or benefit for the different category of users

## 4. Success metrics (weight: high)

Are the metrics the PM proposes actually measuring the job getting done?

- Is there a primary metric (one), not a grab-bag? 
- Are there counter-metrics to catch harm? (e.g., "engagement up, but refund rate flat or down")
- Does the PRD avoid pure vanity metrics (raw DAU, page views) unless tied to a business outcome?
- Is there a target or threshold, or is it "move the needle"?
- Metrics that we are measuring the PRD success against has to be clearly mentioned, it can be a base metric and other supporting primary and secondary metrics used for the evaluation of PRD success

## 5. Solution rationale & tradeoffs (weight: medium)

Does the PRD explain *why this solution* vs. alternatives?

- Are 2+ alternatives discussed, not just dismissed?
- Does the PRD name what it's giving up? (scope cuts, UX compromises)
- Is there a "we considered X and rejected it because Y" paragraph?

## 6. Scope & non-goals (weight: medium)

Is the scope tight enough to ship?

- Is there an explicit list of non-goals?
- Does the MVP feel genuinely minimal, or is it MVP-in-name?
- Are dependencies on other teams called out?
- Provide a detailed view of Functional requirements for the developers with objective, how to achieve, acceptance criteria, and other details mentioned to avoid any ambiguity in development. Example- Existing data movement jobs to be imported into the new product, *including the ones in deleted folder*- this is important to have such details for engineering else it gets missed out. 

## 7. Risks & unknowns (weight: medium)

Does the PM know what could go wrong?

- Technical risks (scale, latency, integration).
- User risks (will people actually adopt / understand / trust it?).
- Strategic risks (does this conflict with another team's roadmap?).
- Are the risks ranked, or is it a laundry list?

## 8. Rollout & learning plan (weight: low–medium)

How will the PM learn whether this worked?

- Is there a staged rollout (internal → beta → GA)?
- Are the learning milestones tied to specific metrics?
- Is there a kill/iterate criterion? ("If metric X doesn't move by Y%, we'll…")
- Contingency plan

## 9. Conclusion/Summary/Action Items (weight: low–medium)

Clear summary of the PRD, what it will achieve, and immediate vs long term action items for stakeholders in a summarized format 

- With explanation of PRD details above, come to a braoder view here and summarize the benefits and key takeaway for each stakeholder
- The action items and RACI (Responsible, Accountable, Consulted, Informed) matrix need to be defined for clear ownership 
- Closing notes and PM view should be reflected as closing section 

---

## How the critic should use the rubric

- Score each section 1–5 with a one-sentence justification that **quotes the PRD**.
- Surface only the **top 2–3 weakest sections** as priority fixes — don't dump all 8.
- For each priority fix, give a concrete rewrite or a question the PM must answer before the review meeting.
- If a section is genuinely strong (4–5), say so briefly. Calibration matters.

## Things the critic should never do

- Invent context (research studies, competitor moves, metric numbers) not present in the PRD.
- Give formatting feedback when structural issues exist.
- Say "this is a great PRD, here are 15 small suggestions." That's not a critique, it's flinching.
