# New-repo checklist

Run this checklist whenever a new repo is added to the `Claude-Code-Academy` GitHub organization (e.g. `web-aios`, `genie-desktop-apps`, etc.).

## Automatic — nothing for you to do

These inherit from the org-level `.github` repo (this repo) the moment the new repo exists, with zero per-repo setup:

- ☑ Issue templates (bug report, feature request)
- ☑ Issue config (no blank issues, community link)
- ☑ PR template (informational "no PRs" warning)
- ☑ `CONTRIBUTING.md` link surfaced when contributors click "New PR"

## Manual — short list, do once

For each new repo:

1. **Set repo description and topics** on github.com (Settings → General → at the top).
2. **Enable branch protection on `main`** — Settings → Branches → Add rule:
   - Restrict pushes that create matching branches: **on** (only the maintainer can push)
   - Require status checks: **on** (if there's CI on this repo)
   - Require pull request reviews before merging: **off** (you're the only reviewer)
3. **Add the contribution paragraph to the README** — paste this near the top, just below the project description:
   > **Contributions**: Pull requests aren't accepted on this repo. If you've found a bug or have a feature request, please [file an issue](../../issues/new/choose). For questions and discussion, join the community at <https://www.skool.com/claude-code-academy>. The owner is the sole maintainer.
4. **Add a row to the `report-issue` skill's `references/repo-mapping.md`**, then republish the skill via `_publish-skills` so the next plugin update propagates the new routing to all members.
5. **Decide whether the repo should be public or private**, and whether it should be visible to the Premium team. Default for code repos: private + Premium team has Read.

## Verification

Within ~10 minutes of finishing the manual steps:

- Visit `github.com/Claude-Code-Academy/<new-repo>/issues/new/choose` — both bug + feature templates should appear, blank issues hidden, community link visible.
- Visit the "New PR" page — the PR template warning should appear.
- Visit the main page — the README contribution paragraph should be visible.
- Run a `python install.py <skill>` (or `/plugin install`) of `genie-essentials`, then say "report a bug in <new-repo>" from any directory — the skill should route to the new repo correctly.
