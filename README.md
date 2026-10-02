# Floppy Knight

An HTML5 canvas game, deployed on Cloudflare Pages and embedded (iframe) into another website.

Your mouse is a floppy ragdoll knight with a physics-driven sword. Fling him around to protect a traveler
walking from town to town. Each level ends at a castle; levels go on forever and get harder.

- `public/index.html` — the entire game (no build step, no dependencies)
- `wrangler.jsonc` — Cloudflare Pages config (`pages_build_output_dir: ./public`)

## Run locally

    python3 -m http.server 8000 -d public

## Deploy

    npx wrangler pages deploy

## Embed

    <iframe src="https://<your-pages-domain>/" width="540" height="960" style="border:0" allow="autoplay"></iframe>

The game letterboxes a 540x960 playfield to any iframe size.
