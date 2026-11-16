# FLOWER FIELD demo plates (DEV FORK 108)

Demo backdrop recreating the Flower Boy cover scene, at Keith's order
(2026-11-15) — a working label only; Keith names worlds himself.

- Master (demo provenance, like the Golden Hour masters):
  `renders/flowerboy-src/media-generation-flowerboy-master-v1-*.webp`
- Bake: `tools/bake_flowerboy.py` — sky / hills / sunflower strip
  plates split by the painting's natural bands; bees cut from the sky
  band by border flood-fill keying (QC: `renders/flowerboy-src/`).
- sky.webp — sky + clouds + rainbow, opaque, full-cover backdrop.
- hills.webp — green hills + road + car, top edge noise-melted.
- strip.webp — sunflower band, mirror-tiled foreground strip (the sea
  strip's role).
- bee1–bee6.webp — individual bee sprites for the drifting dressing
  layer. Ambient only, never obstacles: decks stay clouds, death
  stays fall-only.
