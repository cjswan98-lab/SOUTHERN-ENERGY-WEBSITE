# Southern Energy — draft website

Single-page static site for Southern Energy. No build step: `index.html` is the whole site (logo embedded inline). Pages are switched with hash links (`#group`, `#projects`, `#pipeline`, `#operations`, `#delivery`, `#team`, `#contact`).

## Deploy to Netlify via GitHub

1. Create a new GitHub repository (e.g. `southern-energy-site`) and push these files:
   ```
   git init
   git add .
   git commit -m "Draft Southern Energy website"
   git branch -M main
   git remote add origin https://github.com/<your-account>/southern-energy-site.git
   git push -u origin main
   ```
2. In Netlify: **Add new site → Import an existing project → GitHub**, pick the repo.
3. Leave the build command empty and set the publish directory to `.` (already set in `netlify.toml`). Deploy.
4. Netlify gives you a `*.netlify.app` URL to share as the draft. Rename it under **Site configuration → Site details → Change site name**.

Every push to `main` redeploys automatically.

## Before going live

- Delete `robots.txt` (it currently blocks search engines because this is a draft).
- Point the Southern Energy domain at Netlify under **Domain management**.
- Fill in the Transmission & Distribution and Solar team entries (Prince, Leonard) and add photos if wanted.
- Confirm George Robinson's bio wording and the Bendera MW figure.

## Editing

All content and styling lives in `index.html`. Colours are CSS variables at the top of the `<style>` block; each page is a `<section>` inside `<main>`.
