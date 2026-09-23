# Lumo Pay — Messenger demo page

A one-file static landing page for a **fictional** consumer-payments brand, built to host the
Intercom Messenger (and Fin) on GitHub Pages for demos.

Everything is in `index.html`: markup, inline CSS, and the Messenger snippet. No build step,
no dependencies.

## Set your workspace

Open `index.html`, find the snippet near the bottom, and replace the placeholder with your
Intercom App ID:

```js
window.intercomSettings = { app_id: "APP_ID" };
```

## Publish on GitHub Pages

1. Create a repo in the `intercom` GitHub org and push this folder to `main`.
2. **Settings -> Pages -> Build and deployment -> Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Wait a minute, then share the `https://<org>.github.io/<repo>/` URL.

## Preview locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Notes

- GitHub Pages is public - keep tokens, customer names and any non-public data off this page.
- The page is `noindex` and labelled as fictional in the footer.
- "Talk to us" calls `Intercom('showNewMessage')`; the nav "Support" link calls `Intercom('show')`.
