# PRD Critic — Project Starter Kit

A weekend portfolio project that demonstrates PM thinking through an AI-powered PRD reviewer. The deliverable is a working prototype + case study you can link from your résumé.

## What's in this folder

| File | Purpose |
|---|---|
| `01-project-brief.md` | One-pager: problem, user, success criteria. Read this first. |
| `02-prd-rubric.md` | The evaluation rubric. This *is* the PM thinking — spend time here. |
| `03-system-prompt.md` | Ready-to-paste system prompt for Claude. |
| `04-sample-prd-weak.md` | A deliberately weak PRD — for testing the critic. |
| `05-sample-prd-medium.md` | A mid-quality PRD. |
| `06-sample-prd-strong.md` | A strong PRD — the critic should push back less here. |
| `07-eval-template.xlsx` | Eval spreadsheet. Score 10 PRDs, see where the critic over/under-calls. |
| `08-prototype.html` | Standalone interactive demo you can open in a browser. |
| `09-case-study-template.md` | Fill-in-the-blanks for your portfolio writeup. |
| `10-setup-guide.md` | How to actually run this as a Claude Project in 15 minutes. |

## Suggested weekend timeline

- **Sat AM (3h):** Read the brief and rubric. Adjust the rubric to match *your* PM POV — this is the most important step. Set up the Claude Project using `10-setup-guide.md`.
- **Sat PM (4h):** Run the critic on the three sample PRDs. Iterate on the system prompt until the outputs match the kind of feedback *you* would give. Capture before/after screenshots.
- **Sun AM (3h):** Do the mini-eval. Fill in `07-eval-template.xlsx` with 10 PRDs (the 3 samples + 7 more you find online or write yourself). Grade the critic. Note failure modes.
- **Sun PM (3h):** Write your case study using the template. Push the final kit to GitHub or Notion. Add the link to your résumé.

## What to say in interviews

> "I was curious whether an LLM could give PRD feedback as useful as a senior PM. I designed a rubric, wrote the system prompt, tested it on 10 real PRDs, and measured where it helped vs. where it faked expertise. Want me to walk through the failure modes I found?"

That's the hook. The rubric, the evals, and the failure-mode analysis are what separate this from a generic ChatGPT wrapper.
