# Nocturne — landing page

Static landing page for a web design studio. No build step, no dependencies.

## Files

- `index.html` — the whole page (CSS and JS inline)
- `thanks.html` — form success fallback for no-JS submissions
- `netlify.toml` — deploy config, security headers, cache rules

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy

Connected to Netlify. Pushing to `main` deploys automatically.

- Build command: none
- Publish directory: `.`

## Forms

The enquiry form uses Netlify Forms (`project-brief`). Two constraints:

- The hidden `<input name="form-name">` must stay — Netlify routes submissions with it
- Total request is capped at **8 MB**, one file per field. Enforced client-side in `index.html`

Submissions appear under **Site configuration → Forms**. Add an email notification there or they'll sit in the dashboard unread.

## Before launch

- [ ] Replace placeholder work with real screenshots
- [ ] Remove or replace the testimonials — they're currently invented
- [ ] Confirm the name and swap the wordmark
- [ ] Add OG / Twitter card meta
- [ ] Run Lighthouse
