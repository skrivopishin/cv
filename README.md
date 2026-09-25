# cv

One-page CV served at https://cv.krivopishin.by. Plain `index.html` + `styles.css`, no build step.

## Publish

`.github/workflows/pages.yml` deploys to GitHub Pages on every push to `main`. It copies `index.html`, `ru/`, `styles.css` and an optional `assets/` folder into the artifact. No Jekyll step runs with an Actions deploy, so no `.nojekyll` is needed.

One-time setup:

1. Settings → Pages → Build and deployment → Source: **GitHub Actions**.
2. Settings → Pages → Custom domain: `cv.krivopishin.by`. With an Actions deploy the domain lives in the repo settings, not in a `CNAME` file.
3. DNS at the `krivopishin.by` registrar: `CNAME cv → skrivopishin.github.io.`
4. Once the certificate is issued, enable **Enforce HTTPS**.

## Local preview

```sh
python3 -m http.server 8000
```
