# SalesWizard site: working notes for Claude

Steven manages his websites by talking to Claude in plain English. He is not a developer
and does not use git directly. When he asks for a change, do the whole thing: edit,
commit, push to `main`, then confirm in plain language what a visitor will see.

## READ FIRST: this repo is NOT what serves saleswizard.app

- **https://saleswizard.app** is a multi-page Next.js app hosted on **Vercel** (DNS on
  Cloudflare). Its source code has NOT been found. It is not in this GitHub account,
  Google Drive, or OneDrive, and Steven's Google/GitHub logins are not linked to the
  Vercel account. Edits made here do not change that site.
- This repo is the homepage **mockup**: one static page (`index.html` plus images).
  It publishes to GitHub Pages at https://skrane.github.io/saleswizard-site/ (the repo
  was renamed from `saleswizard-mockup`; GitHub redirects the old name).
- Gaps versus the live site, so this repo cannot replace it yet:
  - Live has `/about`, `/support`, `/privacy`, `/terms`, `/demo`, `/login`; this repo has none.
  - Live has App Store and Google Play badges and a footer; this repo does not.
  - Live writes "Sales Wizard" (two words); this repo uses "SalesWizard".

If Steven asks to change saleswizard.app, say plainly that the live source is still
unlocated, and do not tell him it is live after pushing here. To resolve it: get into the
Vercel project (Settings, Git, or Deployments), or rebuild the missing pages here and move
the domain to Cloudflare Pages (ask first before touching DNS).

## Publish a change to the mockup

1. Edit `index.html` or the images in this folder.
2. `git add -A && git commit -m "..." && git push origin main` (check `git status` first).
3. GitHub Pages rebuilds in about a minute. Check the Pages URL above.

## Where things live

- Code: this repo, working copy at `~/Projects/saleswizard-site`. Do not edit the old copy
  inside Google Drive (`Claude Projects/SalesWizard/SalesWizard app/mockup`); syncing a
  `.git` folder through Drive can corrupt it.
- Logos, decks, pricing research: Google Drive, `Claude Projects/SalesWizard/`.
