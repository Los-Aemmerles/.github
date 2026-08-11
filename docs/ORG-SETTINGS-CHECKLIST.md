# Organisation settings checklist

Items that can only be configured in the GitHub UI for **Los-Aemmerles**. Work through this once when bootstrapping the organisation or after adding new repositories.

## Security

- [ ] **Private vulnerability reporting** — Organisation → Settings → Code security and analysis → enable *Private vulnerability reporting* for all repositories. After enabling, the **Report a vulnerability** button on each repo's Security tab routes reporters privately; [`SECURITY.md`](../SECURITY.md) describes the contact address.
- [ ] **Dependabot alerts** — Enable org-wide under Code security and analysis so dependency vulnerabilities surface in consuming repos.
- [ ] **Secret scanning** — Enable org-wide under Code security and analysis (where available on your plan).

## Organisation profile

- [ ] **Profile picture** — Upload [`assets/logo.png`](../assets/logo.png) (Organisation → Settings → Profile).
- [ ] **Description** — Set to:

  > Open-source software for Los Ämmerles — the Kinderspielstadt in Ammerbuch. Website: https://los-aemmerles.de

- [ ] **Profile README** — Confirm [`profile/README.md`](../profile/README.md) renders on [github.com/Los-Aemmerles](https://github.com/Los-Aemmerles) (requires this repo to be named `.github` and public).

## Repository defaults

- [ ] **Issue form labels** — Create the labels referenced by [`.github/ISSUE_TEMPLATE/`](https://github.com/Los-Aemmerles/.github/tree/main/.github/ISSUE_TEMPLATE) in **every consuming repository** (`la-server`, `la-client`, `la-jobcenter-kiosk`, and any future public repo). Labels must exist in each repo or issue forms will fail to apply them. If a repo adds its own file under `.github/ISSUE_TEMPLATE/`, it **ignores** all inherited templates from this repo.
- [ ] **`la-client` license** — Confirm [`la-client`](https://github.com/Los-Aemmerles/la-client) has a `LICENSE` file (not verified from this checkout).

## Optional private defaults

- [ ] **`.github-private` repository** — This `.github` repo is **public**, so its community defaults apply only to **public** org repositories. If you need the same defaults for **private** repos, create and maintain [`Los-Aemmerles/.github-private`](https://github.com/Los-Aemmerles/.github-private); otherwise skip it.

## After changes

- [ ] Open a test issue in a repo that inherits templates (e.g. `la-jobcenter-kiosk`) and confirm forms and [`CONTRIBUTING.md`](../CONTRIBUTING.md) links work.
- [ ] Run the [link-check workflow](../.github/workflows/link-check.yml) or `lychee` locally on markdown files after editing profile or policy docs.
