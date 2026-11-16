# FLOWER FIELD demo plates (DEV FORK 108; bees + rainbow removed in DEV FORK 110)

Demo backdrop recreating the Flower Boy cover scene, at Keith's order
(2026-11-15) — a working label only; Keith names worlds himself.

- Master (demo provenance, like the Golden Hour masters):
  `renders/flowerboy-src/media-generation-flowerboy-master-v2-nobees-*.webp`
  — the clean re-generation with no bees and no rainbow (Keith,
  2026-11-15: "Remove the beas and the rainbow").
- Bake: `tools/bake_flowerboy_v2.py` — sky / hills / sunflower strip
  plates split by the painting's natural bands (QC:
  `renders/flowerboy-src/flowerboy-plates-qc-v2.jpg`).
- sky.webp — sky + clouds, opaque, full-cover backdrop. No rainbow.
- hills.webp — green hills + road + car, top edge noise-melted.
- strip.webp — sunflower band, mirror-tiled foreground strip (the sea
  strip's role).
- bee1–bee6.webp — the FORK 108 bee sprites. As of FORK 110 they are
  UNREFERENCED: the code neither loads nor draws them. The files stay
  on disk and on the site by decision; nothing in the game points at
  them.
