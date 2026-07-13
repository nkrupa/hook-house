# CLAUDE.md

Static site for Hook House Kitchen, a Gulf seafood restaurant in Aransas Pass, TX. Live at https://hookhousekitchen.com.

Zero-build, no framework, no package manager. Plain HTML/CSS deployed as-is to Cloudflare (Worker with static assets, project `hook-house`).

## Deployment

Push to `main` → Cloudflare auto-deploys (~1 minute). Never force-push.

`wrangler.jsonc` and `.assetsignore` are deploy config — leave them alone.

## Context

This repo's working tree lives inside a shared Dropbox folder that Andy's Claude Desktop (Cowork) also edits and commits from. The full project brief, brand source material, and session notes live one level up in that Dropbox folder (outside the repo). Only one side (Nick or Andy) should commit at a time; always pull before working. **Never delete or recreate this folder wholesale — the `.git` history lives here.**

## Conventions

- One stylesheet (`styles.css`), brand colors as CSS variables at the top: navy `#0A0E2E` / `#131A46`, cyan `#22C3E6`, wave blue `#3C6FE0`, bone `#F4EDDC`
- Type: Montserrat
- Mobile-first; most visitors are on phones
- Email capture posts directly to Mailchimp; the hidden anti-bot input in `index.html` must stay exactly as-is
- Commit messages in plain English — Andy reads them as the site's change history
