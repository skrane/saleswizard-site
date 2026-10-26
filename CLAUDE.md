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
- Rebuilt here from the live site's text (2026-10-21): `about.html`, `support.html`,
  `privacy.html`, `terms.html`, `demo.html` (Calendly embed), the App Store / Google Play
  badges, and the full footer. Marketing pages use the one-word brand "SalesWizard"; the
  Privacy and Terms text is copied word-for-word, so it still says "Sales Wizard".
- Removed on purpose: the setup fee (pricing row, FAQ sentence, and the About-page line).
- Still missing, so this repo cannot replace the live site yet:
  - `/login`: the live Sign in goes to a web app we have no source for. The Sign in links here
    point at `https://saleswizard.app/login`, which only works while Vercel serves the domain.
  - Anything else behind the live site's login (manager dashboard, any API).
- Internal links are relative (`about`, `demo`, `./#how`) so they work on GitHub Pages and
  Cloudflare Pages. Locally, `python3 -m http.server` needs `about.html`, not `about`.

If Steven asks to change saleswizard.app, say plainly that the live source is still
unlocated, and do not tell him it is live after pushing here. To resolve it: get into the
Vercel project (Settings, Git, or Deployments), or rebuild the missing pages here and move
the domain to Cloudflare Pages (ask first before touching DNS).

## Publish a change to the mockup

1. Edit `index.html` or the images in this folder.
2. `git add -A && git commit -m "..." && git push origin main` (check `git status` first).
3. GitHub Pages rebuilds in about a minute. Check the Pages URL above.

## Where things live

- Code: this repo, working copy at `~/Projects/SalesWizard/site`. Do not edit the old copy
  inside Google Drive (`Claude Projects/SalesWizard/SalesWizard app/mockup`); syncing a
  `.git` folder through Drive can corrupt it.
- Logos, decks, pricing research: Google Drive, `Claude Projects/SalesWizard/`.


## Documents in the cloud (not in this repo)

Steven keeps decks, contracts, spreadsheets and other documents in OneDrive and Google
Drive, both synced to this Mac. Look there before saying a document does not exist, and
save new documents there, not in this repo. Paths on this Mac:

- OneDrive: `~/Library/CloudStorage/OneDrive-Personal/SalesWizard` (company docs such as articles of incorporation and EIN, email signatures, PPT, Aerus, misc)
- Google Drive: `~/Library/CloudStorage/GoogleDrive-skrane@skrane.com/My Drive/Claude Projects/SalesWizard` (prospecting, app notes, logo, competitor pricing, Lessons from the Edge)
