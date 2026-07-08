# chadburmeister.com — new site

Static site (no build step): `index.html`, `experience.html`, `books.html`, `podcast.html`, `styles.css`.

## Deploy via GitHub + Vercel
1. Create a GitHub repo (e.g. `chadburmeister-com`), upload these files to the repo root.
2. In Vercel: Add New Project → Import the repo → Framework preset: **Other** → Deploy (no build command, no output dir).
3. Every push to `main` auto-deploys.

## Point the domain (when ready)
1. Vercel → Project → Settings → Domains → add `chadburmeister.com` and `www.chadburmeister.com`.
2. At your DNS provider (or transfer DNS from Squarespace): A record `@` → `76.76.21.21`, CNAME `www` → `cname.vercel-dns.com`.
3. Keep Squarespace active until DNS cutover is verified, then cancel.

## Before canceling Squarespace
- Images are currently hot-linked from the Squarespace CDN (marked with TODO comments). Download them using the **Image + Asset Manifest** doc in the Google Drive backup folder, put them in `/images/`, and update the `src` URLs.
- Download the About-page video from Squarespace admin.
- Export the two password-protected pages (Curriculum, The Cycle of Grace) manually if you want to keep them.
