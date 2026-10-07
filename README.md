# hello-world-static-app

A minimal **static HTML/CSS/JS** starter deployed on [**Webflow Cloud**](https://webflow.com/cloud).

No framework, no build step, no dependencies — just plain files served as-is. This is the
simplest possible Webflow Cloud app: what you commit is what gets served.

> Looking for a framework starter instead? See the other
> [`hello-world-*-app`](https://github.com/Webflow-Examples) examples (Astro, Next.js, React, Vue, Svelte).

## Quickstart

There's nothing to install. Open `index.html` directly, or serve the folder with any
static file server:

```bash
python3 -m http.server 4321
# → http://localhost:4321
```

## Deploy to Webflow Cloud

1. Fork this repo.
2. In your Webflow site, open **Apps → Webflow Cloud → Create new app** and select this repo.
3. Pick a mount path and click **Deploy**.

Full walkthrough: <https://developers.webflow.com/webflow-cloud/quickstart>.

## What's included

- `index.html` — the page markup
- `404.html` — branded "page not found" page, served for unmatched URLs
- `styles.css` — branded `wf-*` styles (plain CSS, no preprocessor)
- `script.js` — tiny progressive enhancement (the page works without it)
- `favicon.svg` — Webflow mark

## Customizing

Edit `index.html` for content and `styles.css` for styling. There is no compile step —
save and reload.

## Custom 404 page

A `404.html` at the repo root is served for any URL that doesn't match a file, with a
`404` status. Edit it like any other page; it reuses the same `wf-*` styles as the
homepage. Remove it if you don't want a custom 404, and Webflow Cloud falls back to a
generic one.

## Learn more

- [Webflow Cloud docs](https://developers.webflow.com/webflow-cloud)
- [Getting started](https://developers.webflow.com/webflow-cloud/getting-started)

---

Built with static HTML · Deployed on Webflow Cloud.
