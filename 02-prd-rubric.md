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

## 2. Evidence & grounding (weight: high)

Is there evidence this problem is real and worth solving?

- Qualitative: quotes, research, usage observations.
- Quantitative: funnel drop-offs, support ticket volume, segment sizes.
- Does the PRD distinguish between "we assume" and "we've verified"?

## 3. Target user & segmentation (weight: medium)

Is the target user specific enough to make tradeoffs?

- "Power users of our analytics dashboard who run >5 reports/week" beats "our users."
- Does the PRD name who this is *not* for?

## 4. Success metrics (weight: high)

Are the metrics the PM proposes actually measuring the job getting done?

- Is there a primary metric (one), not a grab-bag?
- Are there counter-metrics to catch harm? (e.g., "engagement up, but refund rate flat or down")
- Does the PRD avoid pure vanity metrics (raw DAU, page views) unless tied to a business outcome?
- Is there a target or threshold, or is it "move the needle"?

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
