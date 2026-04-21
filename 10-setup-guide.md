# Setup Guide — 15 minutes from zero to demo

You don't need to write code. The fastest path for a PM portfolio piece is to run this in a **Claude Project** and link the prototype HTML for interview demos. Full instructions below.

## Option A (recommended) — Claude Project (no coding, ~10 min)

**What you need:** a Claude account (free tier works; Pro gives you Projects; Pro is ~$20/mo and worth it if you're doing portfolio work).

1. Go to [claude.ai](https://claude.ai) and sign in.
2. Click **Projects** in the left nav → **New project**.
3. Name it: **PRD Critic**.
4. Under **Custom instructions**, paste the entire contents of `03-system-prompt.md` (everything between the `---` lines).
5. Under **Project knowledge**, upload `02-prd-rubric.md`. This is what the critic references when it scores.
6. Click **Start chat** inside the project.
7. Paste the contents of `04-sample-prd-weak.md`. You should get a structured critique with scores, priority fixes, and open questions. If the output format is off, adjust the system prompt and retry.
8. Repeat with the medium and strong samples. Iterate on the prompt until the critic calibrates differently across the three.
9. Screenshot 2–3 critiques for your case study.

That's it. You now have a demoable tool you can open in front of an interviewer.

**Tip:** create a second project called "PRD Critic — harsh mode" with a slightly more aggressive system prompt. Running both on the same PRD and showing the difference is a great interview beat — it demonstrates that you understand prompt design as a design surface, not just a text field.

## Option B — Interactive prototype for your portfolio site

`08-prototype.html` is a standalone, zero-dependency page that demonstrates the UX with pre-built critiques for the three sample PRDs. Use this for:

- Embedding in a Notion/Read.cv portfolio.
- Live demos where you don't want to depend on the Claude UI.
- GitHub Pages hosting (drop the HTML in a repo, enable Pages).

To host on GitHub Pages in 5 minutes:

1. Create a new public GitHub repo named `prd-critic`.
2. Upload all the files from this folder.
3. In repo settings → Pages → select the main branch, root folder.
4. Your site will be at `https://<username>.github.io/prd-critic/08-prototype.html`.
5. Link it from your résumé.

## Option C (optional, for the ML/engineering-curious) — wire Claude's API to the prototype

If you want the prototype to actually call Claude instead of using the pre-built critiques, it's about 20 lines of Python + a lightweight HTML form. This is **not required** for a PM portfolio — in fact, hiring managers for PM roles will be more impressed by your rubric and eval work than by a working API integration. Only do this if you're curious.

Minimum steps:

1. Get an API key from [console.anthropic.com](https://console.anthropic.com).
2. Write a small FastAPI or Flask endpoint that accepts a PRD string and returns Claude's critique. Anthropic has a [quickstart](https://docs.claude.com/en/docs/get-started).
3. Update `08-prototype.html` to POST to that endpoint instead of returning pre-built text.
4. Deploy on Vercel or Replit (both free tiers).

## Interview demo checklist

Before your first interview where you'll show this, practice once end to end:

- [ ] Open the Claude Project with the system prompt loaded.
- [ ] Have the 3 sample PRDs open in another tab.
- [ ] Have the prototype HTML open in a third tab.
- [ ] Have the eval spreadsheet open in a fourth tab.
- [ ] Rehearse: "Here's the rubric → here's the weak PRD critique → here's the strong PRD critique → here's one failure mode I found." 90 seconds.

## Troubleshooting

**The critic is being too nice.** The system prompt likely isn't being loaded. Confirm it's in Project instructions, not pasted into the chat. Also check that the rubric is attached as project knowledge — without it, the critic invents criteria.

**The critic hallucinates research or numbers.** Strengthen the "No fabrication" rule in the system prompt and add: "If you cite a number or a quote, it must be a verbatim substring of the PRD." Re-test.

**The critic is too harsh on the strong PRD.** Calibration drift. Add 1–2 examples of "what a 4 or 5 looks like" to the system prompt, drawn from the strong sample PRD.

**The critic's output format keeps drifting.** Move the output format block to the top of the system prompt and phrase it as: "Your output MUST follow this exact structure, with these exact section headings."

---

That's the full setup. When in doubt, the most portfolio-leveraged hour you can spend this weekend is **iterating the rubric and system prompt** — not adding features.
