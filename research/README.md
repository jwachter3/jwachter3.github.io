# Interactive research pages

Drop one folder per interactive demo here, with an `index.html` inside.

For example, to host an interactive supplement for *Correlation neglect and asset prices*:

```
research/
  correlation-neglect/
    index.html
    figure-data.json
    plot.js
```

It will be served at `https://<your-site>/research/correlation-neglect/`.
Link to it from the main page with:

```html
<a href="research/correlation-neglect/">Interactive supplement</a>
```

Anything self-contained (D3, Observable Plot, Plotly, Shinylive, pyodide, etc.)
will work on GitHub Pages with no build step.
