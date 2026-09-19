# hearthealth-legal

Public legal and support pages for the **CPR360** iPhone app, served by
GitHub Pages at <https://atalreja777.github.io/hearthealth-legal/>.

This repo is public **only** because GitHub Pages requires it on a free plan. The
app's source lives in a separate private repository.

## This repo is the canonical source of the published text

Edit the Markdown here. Do not edit copies elsewhere and expect them to appear.

| Page | File | URL |
|---|---|---|
| Home | `index.md` | `/hearthealth-legal/` |
| Privacy Policy | `privacy.md` | `/hearthealth-legal/privacy/` |
| Consumer Health Data Privacy (WA) | `consumer-health-data.md` | `/hearthealth-legal/consumer-health-data/` |
| Community Terms of Use | `terms.md` | `/hearthealth-legal/terms/` |
| Support | `support.md` | `/hearthealth-legal/support/` |

The Privacy Policy and Support URLs are filed in App Store Connect. **Never change
a `permalink:` value** — that breaks a URL Apple has on record.

## Editing

Open a file on github.com, click the pencil, edit, and commit to `main`. The site
rebuilds in about a minute. No local checkout, no build step, no Node.

Each page's `version:` and `effective:` front-matter drives the stamp under its
title. When the text changes materially, bump both.

## How it's built

Plain Jekyll — GitHub Pages does the build. `_layouts/default.html` is
self-contained (inline CSS, no JavaScript, no external requests) and deliberately
uses **no theme**: a `theme:`/`remote_theme:` line makes the build depend on gem
resolution, which fails quietly and serves a 404.

## Keeping in sync with the app

The app carries its own condensed copies of this text in `constants/legal.js`
(rendered on the in-app Legal screen) and links out to these URLs. When the text
here changes materially, update that file too — they must not diverge.

`terms.md`'s `version:` must match `TERMS_VERSION` in `constants/legal.js`. That
string is what users' recorded consent points at, so a mismatch means the
published Terms advertise a version nobody agreed to.

## Status

Published as v1.0, effective 2026-07-29. Legal review is still outstanding; the
reviewer's revisions land here as v1.1 at the same URLs.
