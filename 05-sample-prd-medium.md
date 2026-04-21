# PRD: Saved Views for Project List

**Author:** J. Doe, PM
**Status:** Draft v2
**Reviewers:** Eng lead, Design lead

## Problem

Project managers in our largest accounts (teams of 50+) have told us that the default project list is hard to work with. In our last round of customer interviews (7 PMs across 5 accounts), 6 out of 7 mentioned that they re-apply the same filters every morning — typically "my team, active, this sprint." One called it "the first 30 seconds of my day I'll never get back."

We also see this in the data: the top 10% of users by session count apply filters on 82% of their project-list visits. The same 2–3 filter combinations appear across a majority of those sessions.

## Target user

This is for our **power users in mid-market and enterprise accounts** — users who visit the project list daily and manage 20+ active projects. It is **not** for casual users on the free plan, who typically have <5 projects and don't use filters.

## Proposed solution

Add "Saved Views" to the project list. A user can:

1. Apply any combination of filters/sorts.
2. Save that combination as a named view.
3. Pin up to 3 views to the top of the project list for one-click access.
4. Set a default view that loads on app open.

## Why this over alternatives

- **URL-based shareable filters (considered):** solves sharing, not the daily friction. Rejected for v1, but we'll keep the URL encoding so we can layer sharing on later.
- **Smart default ("your most-used filter"):** magical but opaque; users told us they want control, not guessing.
- **Do nothing / rely on browser bookmarks:** works for some, but only 12% of power users have bookmarks to filtered views. Friction is clearly too high.

## Success metrics

**Primary:** % of eligible power users who have created ≥1 saved view within 30 days of launch. Target: 40%.

**Secondary:** Time from app open to first project interaction for power users. Target: decrease by 20%.

**Counter-metric:** Support ticket volume related to project-list confusion. Must not increase.

## Scope

**In scope:** creating, editing, pinning, deleting saved views. Personal only, not team-shared.

**Non-goals:** sharing views with teammates, template views from admin, scheduled email digests of a view.

## Risks

- Feature discoverability — saved views will be a new concept. Mitigation: onboarding tooltip the first time a user applies 2+ filters.
- Performance — views with complex filter combinations on large accounts could be slow. Eng team is investigating.

## Rollout

Gradual: 10% of eligible accounts → 50% → 100% over 3 weeks. We'll pause if counter-metric regresses.

## Open questions

- Should the default view be editable from mobile, or desktop-only for v1?
