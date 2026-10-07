# CONTEXT — hello-world-static-app

Orientation for contributors to this **static HTML** Hello World example for
[Webflow Cloud](https://developers.webflow.com/webflow-cloud). Keep this file
current when structure or workflows change.

## What this is

The simplest possible Webflow Cloud app: **plain HTML, CSS, and JavaScript** with
**no framework and no build step**. What is committed is what gets served. It exists
to exercise Webflow Cloud's static-site support (no framework detection, no bundler).

The page shows a Webflow brand hero, gradient logo, and curated doc cards pointing at
the Webflow Cloud documentation — matching the other `hello-world-*` examples visually.

## Stack

- Framework: **none** (static HTML/CSS/JS)
- Styling: plain CSS with `wf-*` brand tokens (see `styles.css`)
- Build: **none** — files are served as-is
- Deploy target: Cloudflare Workers static assets via **Webflow Cloud**

## Repo layout

```
index.html      ← page markup (header, hero, doc cards, footer)
404.html        ← branded "page not found" page (served for unmatched URLs)
styles.css      ← .wf-* design tokens and layout (plain CSS)
script.js       ← optional progressive enhancement (footer year)
favicon.svg     ← Webflow mark
```

## Running locally

No dependencies. Serve the folder with any static server, e.g.:

```bash
python3 -m http.server 4321
```

Or just open `index.html` in a browser.

## Editing the UI

- **Page content (hero, CTAs, doc cards):** `index.html`
- **Not-found page:** `404.html`
- **Brand tokens and `.wf-*` styles:** `styles.css`
- **Optional JS enhancement:** `script.js`

## 404 handling

`404.html` at the repo root is served for any unmatched URL with a `404` status.
Webflow Cloud's static deploy config sets `assets.not_found_handling: "404-page"`, so the
nearest `404.html` is used for misses; apps without one get a generic 404. The 404 lookup
is internal to the served assets, so it works the same under any mount path. The "Back to
home" link uses a relative `./` href for the same reason, so keep 404 asset paths relative.

## Deploying to Webflow Cloud

1. Push this repo to GitHub.
2. In your Webflow Cloud project, connect the repo and pick a mount path
   (e.g. `/my-app`). The app runs under any prefix.
3. There is no build command — Webflow Cloud serves the files directly.

See [Deployments](https://developers.webflow.com/webflow-cloud/deployments)
and [Environments](https://developers.webflow.com/webflow-cloud/environments).

## Contributing

- Keep the **Webflow brand tone**: blue gradient (`#4353FF` → `#146EF5`), dark
  background, minimal copy. Reuse the existing `.wf-*` CSS tokens.
- This is a Hello World. Do **not** add a framework, a build step, bundlers, or
  dependencies — the whole point of this example is that it has none.
- Keep asset paths **relative** (`styles.css`, not `/styles.css`) so the app works
  under any mount path.
- Keep **cross-app parity**: if you change shared copy or doc links, update the
  sibling `hello-world-*-app` apps too.

## Related docs

- [Webflow Cloud overview](https://developers.webflow.com/webflow-cloud)
- [Getting started](https://developers.webflow.com/webflow-cloud/getting-started)
- [Environments](https://developers.webflow.com/webflow-cloud/environments)
- [Deployments](https://developers.webflow.com/webflow-cloud/deployments)
- [Limits](https://developers.webflow.com/webflow-cloud/limits)
