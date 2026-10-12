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

## Unlisted AI paper draft

The current AI paper is available at
`https://jwachter3.github.io/research/ai-transition/current-draft.pdf`.
This is a public, shareable URL with no link from the main page or the workbook
page. Keep the URL stable when Jessica requests a refreshed draft.

Source: `~/Projects/Research/rare-ai-growth/aiv09.pdf`. The October 12, 2026
upload is the 78-page revised v09 reviewed on October 11 (paper changes in
research commit `0216bc4`). After a future approved refresh, copy the verified
paper PDF to `research/ai-transition/current-draft.pdf`, commit and push, then
verify that the deployed file matches the source. Do not use the older blinded
JFE submission build.

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
