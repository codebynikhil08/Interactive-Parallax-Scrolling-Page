# Techfest — Orbit Deck (Parallax Scrolling Page)

A multi-layer parallax scrolling page built for the **"Interactive Parallax Scrolling Page"** Campus Ambassador task — same space/tech universe as the Flight Path 3D build, but a lighter, pure CSS+JS parallax experience (no WebGL).

## Concept
Four full-height sections — Hero, Mission Brief, Tracks, Footer — each with 2-4 layered elements (starfield, nebula, planets, rings, asteroids, a tech grid, a satellite, a moon) that move at different speeds as you scroll, creating a sense of depth. Slower layers feel "further away," faster layers feel closer.

## Tech
- Pure HTML/CSS + vanilla JS — no frameworks, no build step
- `requestAnimationFrame`-throttled scroll listener computes each layer's offset from its own `data-speed` attribute
- CSS-only visuals (radial gradients, borders, blends) — no external images, fast to load
- Subtle mouse-based parallax on the hero planet for extra depth on desktop
- Google Fonts: Space Grotesk (display), Inter (body), IBM Plex Mono (labels)

## Run locally
Just open `parallax.html` in a browser. Or serve it:
```bash
python3 -m http.server 8000
```

## Deploy to GitHub Pages
1. Push to your repo (can live alongside the Flight Path project or in its own repo).
2. Settings → Pages → Deploy from branch → `main` / root.
3. Live URL: `https://<username>.github.io/<repo-name>/parallax.html`

## Notes
- Respects `prefers-reduced-motion` (parallax transforms disabled).
- Fully responsive; track cards stack to a single column under 820px.
