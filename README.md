# Claude-Code-Academy / .github

This is the **org-level configuration repo** for the [Claude-Code-Academy](https://github.com/Claude-Code-Academy) GitHub organization. It is not a code repo and not meant to be cloned by members.

## What lives here

- **`.github/ISSUE_TEMPLATE/`** — bug + feature request issue forms shown on every CCA repo's "New Issue" page (unless that repo overrides locally).
- **`.github/PULL_REQUEST_TEMPLATE.md`** — informational body shown when anyone opens a PR against any CCA repo. Surfaces the no-PRs policy *before* the contributor invests effort.
- **`.github/CONTRIBUTING.md`** — short contribution policy (PRs not accepted; please file an issue).
- **`profile/README.md`** — public org profile shown at https://github.com/Claude-Code-Academy.
- **`NEW-REPO-CHECKLIST.md`** — checklist for the maintainer to follow whenever a new repo is added to the CCA org.

## How it applies to other CCA repos

When anyone visits `github.com/Claude-Code-Academy/<any-repo>/issues/new` or opens a PR, GitHub looks up this repo at the org level and **inherits these defaults** for any file the target repo doesn't define locally. There is no per-repo install, sync, or import — the inheritance is server-side.

## What this repo is **not**

- It does **not** contain GitHub Actions workflows. Workflows do not inherit org-wide; each repo manages its own.
- It does **not** ship code, scripts, or libraries.
- It is **not** a marketplace, plugin, or skill.

If you've landed here looking for the actual Genie OS, see [genie-aios](https://github.com/Claude-Code-Academy/genie-aios). If you're looking for vetted third-party Claude Code extensions, see [genie-curated-marketplace](https://github.com/Claude-Code-Academy/genie-curated-marketplace).
