# Red Inc site (local draft)

Static company site for [redincdc.github.io](https://redincdc.github.io/). Do not upload a new version until Red has approved the deploy.

The existing game stays in its own repo (`redincdc/castledefensecuh`) at `https://redincdc.github.io/castledefensecuh/`. Game links in these pages use `/castledefensecuh/` and `/castledefensecuh/play/`.

## Pages

- `/` — Red Inc home (what the company does, projects, founder pointer)
- `/projects/` — project cards (Castle Defense Cuh and placeholders)
- `/about/` — Redouan Djeebet, owner and creator, with a link to the CV
- `/cv/` — CV page, with a Download PDF button
- `/cv/Redouan-Djeebet-CV.pdf` — printable PDF of the same CV
- `/portfolio/` — redirect to `/projects/`
- `/404.html` — not-found page

Navigation is Home, Projects, About, Contact (`redincdc@gmail.com`).

The site footer and Contact link use `redincdc@gmail.com`. The CV contact line from Red's CV (address, phone, Outlook, and the game URL) stays in a single `#cv-contact` block on `/cv/` only.

## Local preview

From this folder:

```sh
python3 -m http.server 4173
```

Then open `http://127.0.0.1:4173/`. Game links 404 on a local preview because the game files are not in this folder. After a real deploy they resolve on the live domain.

## Deploy (only after Red OKs it)

1. Sign in to GitHub as **redincdc**.
2. The repo `redincdc/redincdc.github.io` already exists. Open the web upload page for each folder as needed: `https://github.com/redincdc/redincdc.github.io/upload/main`
3. Upload the changed files from this draft. Do not upload anything from `/workspace/site/preview/` or `/workspace/site/cv-source/`.
4. Commit. After Pages builds, check:
   - `https://redincdc.github.io/`
   - `https://redincdc.github.io/castledefensecuh/` (existing game, should be unchanged)
