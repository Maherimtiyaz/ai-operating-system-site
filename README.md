# AIOP — landing site

Marketing / download site for [AIOP](https://github.com/Maherimtiyaz/ai-operating-system),
the local-first voice assistant and automation engine for Windows.

Served automatically by GitHub Pages via `.github/workflows/pages.yml`.

## How the download button works

`index.html` links the primary CTA to the AIOP app repo's latest release asset:

```
https://github.com/Maherimtiyaz/ai-operating-system/releases/latest/download/aiop-windows-x64.zip
```

That URL resolves only after a GitHub Release is published on the **app repo**
(`Maherimtiyaz/ai-operating-system`) with a file named exactly
`aiop-windows-x64.zip`. The release asset lives there — never in this repo —
so the 150 MB+ distribution stays out of version control.

## Deploying

1. Enable **Settings → Pages → Source: GitHub Actions** in this repo.
2. Push to `main`; the `pages.yml` workflow publishes `./` (index.html + assets).

The site links point at the app repo regardless of this repo's name/host.

## License

Site content: Apache-2.0 (see `LICENSE`).