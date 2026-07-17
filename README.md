# Dustin Lawrence — CV site

Personal CV / portfolio for Dustin Lawrence, Founder of MissionCTRL.

## What's in here

| File | Purpose |
|---|---|
| `index.html` | The interactive CV — open in any browser, or deploy as a site |
| `Dustin-Lawrence-CV.pdf` | The 2-page landscape PDF version (linked from the HTML's "Download CV" button) |
| `netlify.toml` | Netlify config — sets cache headers and pretty URLs (`/cv`, `/cv.pdf`, `/download`) |
| `_redirects` | Fallback redirects in case netlify.toml isn't picked up |
| `README.md` | This file |

## Deploy to Netlify

### Option 1 — Netlify Drop (fastest, no account needed for the demo)

1. Go to <https://app.netlify.com/drop>
2. Drag this entire folder onto the drop zone
3. You'll get a random `*.netlify.app` URL immediately
4. Sign in to claim the site and add a custom domain

### Option 2 — Netlify CLI

```bash
# one-time
npm install -g netlify-cli
netlify login

# from inside this folder
netlify deploy            # preview deploy
netlify deploy --prod     # production deploy
```

### Option 3 — Git connected

1. Push this folder to a GitHub/GitLab repo
2. In Netlify: **Add new site → Import an existing project**
3. Connect the repo
4. **Publish directory:** `.` (root) — already set in `netlify.toml`
5. **Build command:** leave empty (static site, no build needed)

## Custom domain ideas

- `cv.missionctrl.agency` (subdomain on your existing domain)
- `dustinlawrence.com` (if you want it standalone)
- `dl.missionctrl.agency`

Add the custom domain under **Site settings → Domain management** in Netlify and follow the DNS instructions.

## Updating the CV

When you tweak the HTML or replace the PDF:

- **Netlify Drop** — drag the folder again, you'll get a new URL (or replace files on the existing site)
- **CLI** — re-run `netlify deploy --prod`
- **Git** — commit and push; Netlify auto-deploys

## Pretty URLs (already configured)

Once deployed, these all work:

- `your-site.netlify.app/` → CV (the HTML)
- `your-site.netlify.app/cv` → opens the PDF
- `your-site.netlify.app/cv.pdf` → opens the PDF
- `your-site.netlify.app/download` → opens the PDF

Handy for sharing — `cv.missionctrl.agency/cv` reads cleaner than the full PDF path.
