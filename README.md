# Ahsan Jamal Cheema — academic website

A plain HTML site. No build step is needed. `index.html` is the whole site, and everything it uses lives in `assets/`.

```
index.html              the site
assets/cv.pdf           CV linked from the site
assets/favicon.svg      browser-tab icon
assets/img/profile.jpg  headshot
assets/img/pubs/        publication thumbnails
drafts/                 the two layouts not chosen (git-ignored)
```

## Preview locally

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765.

## Publish on GitHub Pages

1. Create a public repository on GitHub named exactly `YOUR-USERNAME.github.io`.
2. From this folder, push the site:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
   git push -u origin main
   ```
3. On GitHub, open **Settings → Pages**. Set **Source** to "Deploy from a branch", choose `main` and `/ (root)`, and save.
4. After a minute or two, the site is live at `https://YOUR-USERNAME.github.io`.

`.gitignore` keeps the raw `papers/`, `pictures/` and `resume/` folders out of the repository, so only the copies in `assets/` are published.

## Common updates

- **New paper:** copy one `<div class="pub">…</div>` block in the Publications section. Link the PDF from arXiv or the publisher (paper PDFs are not stored in this repo), and put a thumbnail in `assets/img/pubs/`.
- **News:** edit the `<ul>` under "News" in the About section.
- **CV:** replace `assets/cv.pdf`. Note that the current file includes your phone number.
- **More profile links (e.g. GitHub):** copy the Google Scholar `<li>` in the sidebar and change the icon, URL and label.
