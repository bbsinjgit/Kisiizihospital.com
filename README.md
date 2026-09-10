# Kisiizi Hospital website

Source code for the Kisiizi Hospital (Church of Uganda mission hospital, Rukungiri District, Uganda) website.

## Pages

| File | Section |
|---|---|
| `index.html` | Home |
| `about.html` | About — history & medical superintendents |
| `care.html` | Care — clinical departments |
| `programs.html` | Programs — SCBU, Ahumuza, Maternity, Palliative Care, Empower, Nutrition Project |
| `community.html` | Community — Health Co-op, Nursing School, Primary School, Power Company, Falls, Child Sponsorship |
| `news.html` | News + email digest signup |
| `visit.html` | Visit — electives, volunteering, accommodation & costs, travel |
| `give.html` | Give — bank account details |
| `contact.html` | Contact |

Each file is a complete, self-contained HTML page (styles and images inlined) generated from a Claude-built design. No build step is required — any one of them can be opened directly in a browser or deployed as-is to static hosting.

## Current status

All internal navigation, header, and footer links now point to the sibling files in this repo (`about.html`, `care.html`, etc.) rather than to claude.ai. This repo is self-contained and ready to deploy as the live site — see **Deploying** below.

**Important — when re-uploading these files to GitHub:** upload the whole `files/` folder together (drag it into the upload box as a folder), not just the two PDFs on their own. If the PDFs land at the repo root instead of inside `files/`, the links in `news.html` (which point to `files/leah-prairie-update-2026-09.pdf`) will 404. If that's already happened, either move the two PDFs into a `files/` folder in the repo, or delete the root-level copies once the `files/` versions are uploaded.

## files/

Source documents referenced by news items (PDFs, etc.) live here rather than embedded in the HTML, so the pages stay small and each document gets its own stable link. Currently:

| File | Used by |
|---|---|
| `files/leah-prairie-update-2026-09.pdf` | Full "Medical Missions in Kisiizi" report, Sept 2026 news item |
| `files/leah-prairie-update-2026-09-onepage.pdf` | One-page summary of the same |

`news.html` in this repo already links to these two files this way (plain `<a href="files/...">`) rather than embedding them — that's different from the version currently live on claude.ai, which embeds the PDFs as base64 because the Artifact viewer's download feature needs the bytes on the page. This repo's copy is the version to keep using once it becomes the real deployed site.

To add a future news PDF: upload the file into `files/` (drag it into that folder path the same way you upload any file to GitHub — see below), then link to it from the relevant news card as `<a href="files/your-file-name.pdf">Read the full update &rarr;</a>`. No embedding needed — this is the pattern to use going forward.

### Creating a folder on GitHub

GitHub's web upload doesn't have a separate "new folder" button — a folder is created the moment a file is placed inside it. Two ways to do that from **Add file → Upload files**:

- Drag the whole `files` folder (from the unzipped download) straight into the upload box — GitHub keeps the folder structure and creates `files/` automatically.
- Or drag individual files in one at a time and rename each one with the folder as a prefix, e.g. type `files/leah-prairie-update-2026-09.pdf` as the filename — GitHub creates the folder from that path.

Either way works; dragging the whole folder is quicker when there's more than one file.

## Deploying

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages). For GitHub Pages: enable Pages on this repo (Settings → Pages → Deploy from branch → `main` / root), which will serve `index.html` at the repo's Pages URL automatically. A custom domain can then be attached in the same settings page.
