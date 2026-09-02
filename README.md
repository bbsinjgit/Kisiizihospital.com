# Kisiizi Hospital website

Source code for the Kisiizi Hospital (Church of Uganda mission hospital, Rukungiri District, Uganda) website.

## Pages

| File | Section |
|---|---|
| `index.html` | Home |
| `about.html` | About — history & medical superintendents |
| `care.html` | Care — clinical departments |
| `programs.html` | Programs — SCBU, Ahumuza, Maternity, Malnutrition, Empower |
| `community.html` | Community — Health Co-op, Nursing School, Primary School, Power Company, Falls, Child Sponsorship |
| `news.html` | News + email digest signup |
| `visit.html` | Visit — electives, volunteering, accommodation & costs, travel |
| `give.html` | Give — bank account details |
| `contact.html` | Contact |

Each file is a complete, self-contained HTML page (styles and images inlined) generated from a Claude-built design. No build step is required — any one of them can be opened directly in a browser or deployed as-is to static hosting.

## Current status

These files are a snapshot of the site as currently published at claude.ai/code/artifact/... (one Artifact per page). **The navigation, header, and footer links in these files still point to those live claude.ai URLs**, not to the sibling files in this repo. That's fine for viewing each page standalone, but if this repo is deployed as the live site (e.g. via GitHub Pages, Netlify, or Vercel), those internal links should be updated to relative paths (`about.html`, `care.html`, etc.) so navigation stays on the new domain instead of bouncing back to claude.ai.

## Deploying

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages). For GitHub Pages: enable Pages on this repo (Settings → Pages → Deploy from branch → `main` / root), which will serve `index.html` at the repo's Pages URL automatically. A custom domain can then be attached in the same settings page.
