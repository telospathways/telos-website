# Telos Pathways — Website

Static HTML site for Telos Pathways. No build step — every page is plain HTML/CSS/JS.

## Deploy to GitHub Pages

1. Create a new GitHub repo (public for free Pages hosting, or private on Pro/Org).
2. Push this folder to the repo:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages**.
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` / `/ (root)`
   - Save.
4. Wait ~1 minute. Your site goes live at `https://<you>.github.io/<repo>/`.

### Custom domain (optional)
Add a file called `CNAME` at the repo root containing just your domain
(e.g. `telospathways.com`), then point a DNS `CNAME` record at
`<you>.github.io`. GitHub Pages will pick it up automatically.

## File structure

- `index.html` — home page (hero with rotating globe)
- `workshops.html`, `ai.html`, `tutoring.html`, `our-method.html`,
  `admissions.html`, `about.html`, `faqs.html`, `contact.html`, `privacy.html`
- `assets/` — logo + globe images
- `.nojekyll` — tells GitHub Pages to skip Jekyll processing and serve files as-is
- `.gitignore` — excludes editor & OS junk

## Contact form

`contact.html` posts to Formspree at `https://formspree.io/f/xgodpvow` via
fetch, then shows an inline success state. No server config needed.

## Notes

- All filenames are lowercase with hyphens — friendly for case-sensitive
  hosting and tidy URLs.
- Internal links use relative paths, so the site works equally well at a repo
  subpath (`/<repo>/`) or at a custom apex domain.
