# Portfolio — Deploy to GitHub Pages (github.com/t-rexx1)

## Fastest option: your personal site (t-rexx1.github.io)

1. Create a new repo on GitHub named exactly `t-rexx1.github.io`
2. Upload everything in this `site/` folder to the repo root (`index.html` must sit at the repo root, `assets/` alongside it)
3. Settings → Pages → Source: `Deploy from branch` → `main` / `(root)` → Save
4. Live in ~1 minute at **https://t-rexx1.github.io**

## Alternative: a project repo (e.g. github.com/t-rexx1/portfolio)

1. Create any repo, e.g. `portfolio`
2. Upload this folder's contents to the repo root
3. Settings → Pages → Source: `main` / `(root)`
4. Live at **https://t-rexx1.github.io/portfolio**

## Command-line push (either option)

```bash
cd site
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/t-rexx1/REPO_NAME.git
git push -u origin main
```

Then turn on Pages in the repo Settings as above.

## One thing to fix before/after publishing

`assets/wmr/` is currently empty — the Wheeled Mobile Robot section shows a placeholder box.
The docx you sent had no embedded images, and the photo pasted directly into chat couldn't be
saved as a file on this end. To fix:

1. Drop your WMR photo(s) into `assets/wmr/` (e.g. `assets/wmr/wmr-1.jpg`)
2. In `index.html`, find the `<!-- WMR -->` card and replace the `<div class="placeholder">...</div>`
   line inside `.mosaic.n3` with `<img>` tags, e.g.:
   ```html
   <img src="./assets/wmr/wmr-1.jpg" alt="Wheeled mobile robot prototype" data-cap="Wheeled mobile robot — UC Berkeley capstone build">
   ```

## Notes

- All copy pulled from your resume + the two intern project PDFs; images extracted directly from those PDFs.
- Simulation-section GIFs (Aerial Firefighting, Autonomous Security Fleet) are hot-linked from your GitHub repos — they'll always reflect the current `master`/`main` branch, no need to re-upload if you update those repos.
- `assets/misc/Aaditya_Shrivastava_Resume.pdf` is linked from the "Download Résumé" button — swap in a newer version any time by replacing that file (keep the same filename, or update the `href` in `index.html`).
