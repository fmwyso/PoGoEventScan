# PoGo Event Scan

Single-page check-in board for a Campfire event. Paste a Campfire link (e.g. `https://cmpf.re/KnRPxW`), press **Update**, and split RSVPs into Checked in / Accepted.

## GitHub Pages

1. Push this repo (or just `index.html`) to GitHub.
2. Enable **Settings → Pages → Deploy from a branch** (usually `main` / root).
3. Open the Pages URL and press **Update**.

No build step. No server.

## Local preview

Open `index.html` via any static server (or GitHub Pages). Opening as a raw `file://` URL may fail because the CORS helper only allows browser origins like `localhost` and `*.github.io`.

```bash
npx --yes serve .
```

## Note

The events API does not send CORS headers, so the page loads it through [corsproxy.io](https://corsproxy.io/), which allows `github.io` and localhost for free.
