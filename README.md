# Floppy Knight

An HTML5 canvas game, deployed on Cloudflare Pages and embedded (iframe) into another website.

Your mouse is a floppy ragdoll knight with a physics-driven sword. Fling him around to protect a traveler
walking from town to town. Each level ends at a castle; levels go on forever and get harder.

- `public/index.html` — the entire game (no build step, no dependencies)
- `wrangler.jsonc` — Cloudflare Pages config (`pages_build_output_dir: ./public`)

## Versioning

The version shows in the bottom-right corner of the game. To release a new version, bump
`VERSION` (and the matching `<meta name="version">`) at the top of `public/index.html`,
commit, and tag it: `git tag v1.2.0 && git push --tags`.

## Run locally

    python3 -m http.server 8000 -d public

## Deploy

    npx wrangler pages deploy

## Embed

    <iframe src="https://<your-pages-domain>/" width="540" height="960" style="border:0" allow="autoplay"></iframe>

The game letterboxes a 540x960 playfield to any iframe size.
