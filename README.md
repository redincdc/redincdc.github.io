# Redouan Djeebet (local draft)

Static personal site for [redincdc.github.io](https://redincdc.github.io/). This folder is a **local draft only**. Do not create the GitHub repo, push, or upload anything until Red has approved the deploy.

The existing game stays in its own repo (`redincdc/castledefensecuh`) and keeps working at `https://redincdc.github.io/castledefensecuh/`. This user-site repo only serves the root (`/`). Game links use `/castledefensecuh/` and `/castledefensecuh/play/`.

## Pages

- `/` — about / bio, then the CV, then a short projects section
- `/#cv` — CV section on the home page (Download PDF is here too)
- `/cv/` — standalone CV page, with a Download PDF button
- `/cv/Redouan-Djeebet-CV.pdf` — printable PDF of the same CV
- `/projects/` — project cards (Castle Defense Cuh and placeholders)
- `/portfolio/` — redirect to `/projects/`
- `/404.html` — not-found page

Navigation is About, CV, Projects. Castle Defense Cuh is one project, not the site brand.

The site footer contact is `redincdc@gmail.com`. The CV contact line from Red's CV (address, phone, Outlook, and the game URL) is in a single `#cv-contact` block, so it is easy to swap to `redincdc@gmail.com` only if he asks.

## Local preview

From this folder:

```sh
python3 -m http.server 4173
```

Then open `http://127.0.0.1:4173/`. Game links 404 on a local preview because the game files are not in this folder. After a real deploy they resolve on the live domain.

## Deploy (only after Red OKs it)

1. Sign in to GitHub as **redincdc**.
2. Create a new **public** repository named exactly `redincdc.github.io`. Leave it empty (no auto README) if GitHub offers that option.
3. Open the web upload page: `https://github.com/redincdc/redincdc.github.io/upload/main`
4. Upload the files and folders from this draft (`index.html`, `style.css`, `404.html`, `robots.txt`, `README.md`, `favicon.ico`, `favicon-32.png`, `apple-touch-icon.png`, `assets/`, `projects/`, `portfolio/`, and `cv/` including `cv/index.html` and `cv/Redouan-Djeebet-CV.pdf`). Do not upload anything from `/workspace/site/preview/` or `/workspace/site/cv-source/`.
5. Commit once.
6. If the site is not live within a minute or two, in the repo go to **Settings → Pages** and set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**. A user site at `redincdc.github.io` is then served at `https://redincdc.github.io/`.
7. Check both:
   - `https://redincdc.github.io/`
   - `https://redincdc.github.io/castledefensecuh/` (existing game, should be unchanged)

Do not put Castle Defense Cuh source files in this repo, and do not rename or move `redincdc/castledefensecuh`.
