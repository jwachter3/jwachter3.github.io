# personal-site

Source for Jessica Wachter's personal research website.

Plain HTML/CSS, no build step. Hosted on GitHub Pages.

## Files

- `index.html` — the page (bio, working papers, publications)
- `style.css` — styling
- `cv.pdf` — CV (source lives at `~/Projects/sandbox/CV/Wachtercv.tex`; refresh with
  `cp ~/Projects/sandbox/CV/Wachtercv.pdf cv.pdf` whenever the source is recompiled)
- `research/` — one subfolder per interactive supplement (see `research/README.md`)

## Editing

To add a paper, copy one of the `<li>` blocks in `index.html` and edit in place.

`<a href="#">…</a>` is a placeholder link. The site styles these in muted/dotted
gray so they're easy to spot. Replace each with the real URL — either an SSRN
abstract page, a publisher DOI, or a PDF you drop into the repo.

## Local preview

Open `index.html` in a browser, or run:

```
python3 -m http.server 8000
```

then visit http://localhost:8000.

## Deploying to GitHub Pages

1. Create a new GitHub repo named `<your-username>.github.io` (a *user site* —
   one per account, served at the clean root URL `https://<your-username>.github.io`).
2. From this directory:

   ```
   git remote add origin git@github.com:<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```

3. In the repo's Settings → Pages, set the source to the `main` branch.
4. Site is live at `https://<your-username>.github.io` within a minute or two.

To hook up a custom domain later (e.g. `jessicawachter.com`), add a `CNAME` file
to this repo with the domain on a single line and configure DNS at the registrar.
