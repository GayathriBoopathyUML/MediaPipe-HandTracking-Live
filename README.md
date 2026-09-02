# MP Hand Tracking Live

Real-time two-hand tracking with background blur — runs entirely client-side
in the browser using MediaPipe's JavaScript solutions (Hands + Selfie
Segmentation). No backend, no build step — just static files, deployable
straight to GitHub Pages.

**Live demo (after deploy):** `https://<your-username>.github.io/<repo-name>/`

## Run locally

Just open `index.html` in a browser — or, since some browsers block
camera access on `file://` URLs, serve it locally:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Notes

- Everything (hand landmarks + background blur) runs on-device via WebAssembly -- no video is ever uploaded anywhere.
- Works best in Chrome or Edge. Requires HTTPS (GitHub Pages provides this automatically) for camera permission to be granted.
- Adjust blur strength live with the on-page slider.
