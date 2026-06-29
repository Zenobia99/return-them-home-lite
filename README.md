# Return Them Home — 2D Map (edge / mobile)

The lightweight 2D companion to the full 3D *Return Them Home* experience, for
phones, tablets and low-power devices. The original Leaflet map (select objects,
send them home with a fly animation, photo + detail per object) — now backed by
the full 5,000-object collection.

To keep mobile hardware safe, the map only ever shows a **date-filtered slice**
of the collection (capped at ~700 active markers). Use the **year range** to
explore different periods; object photos are **atlas-tile thumbnails** (cropped
from bundled sprite sheets — no per-object image downloads).

Standalone, static, no build step. Separate from the 3D project by design.

## Stack
- **Leaflet** (from CDN).
- `artifacts.json` — all 5,000 objects (bundled).
- `atlas/atlas_0..4.jpg` — 4096px sprite sheets for the thumbnails.

## Run locally
```bash
python3 -m http.server 8000   # open http://localhost:8000/
```

## Deploy (GitHub Pages)
Push, then **Settings → Pages → Source: Deploy from a branch → `main` /
`/ (root)`**. No build. The "Switch to 3D" link points at `../return-them-home/`.

## Licence
Object photographs © The Trustees of the British Museum, CC BY-NC-SA 4.0.
