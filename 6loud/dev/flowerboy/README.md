# FLOWER FIELD demo plates (DEV FORK 108; bees + rainbow removed in DEV FORK 110; identity plates in DEV FORK 116)

Demo backdrop for the flower world, at Keith's order (2026-11-15)
— a working label only; Keith names worlds himself. As of FORK 116
the master is OURS (Keith, 2026-11-15 22:29-22:30 ET: the album
cover was inspiration only, the world must be unique — he picked
"Notes in the field": giant musical notes among the sunflowers,
6loud's own currency as the world's signature).

- Master (demo provenance, like the Golden Hour masters):
  `renders/flowerboy-src/media-generation-flowerboy-master-v3-notes-*.webp`
  (2448×1024) — sunset sky, green hills + road + car, sunflower
  field, and SEVEN gold notes: two giants flanking, note 2, a
  beamed pair, three small drifts. No bees, no rainbow.
- Bake: `tools/bake_flowerboy_v3.py` (QC:
  `renders/flowerboy-src/flowerboy-plates-qc-v3.jpg`; parallax
  rigidity: `renders/flowerboy-src/flowerboy-parallax-qc-v3.jpg`
  via `tools/flowerboy_parallax_qc.py`).
- THE BANDING LAW (settled from the __flowerDraw math): every
  note lives WHOLE in the hills plate — heads and full stems at
  their painted positions — so no note shears across the
  parallax split; the strip draws over the hills' bottom band
  in play, so stem bases (and note 2's head) tuck behind the
  flowers and the notes read as rising out of the field.
- sky.webp — sky + clouds, opaque, full-cover backdrop
  (1600×322). The giants' stems are painted out of it — their
  tops live in the hills; a sky copy would ghost at the split.
- hills.webp — green hills + road + car AND all seven notes,
  top edge noise-melted with the notes' alpha restored through
  the melt. Band extended to master y 330–975 to hold the notes
  whole; plate 1600×421 keeps the painting's aspect. No note
  straddles a tile edge (≥150 plate px clear), so mirror tiling
  never halves one.
- strip.webp — PURE sunflower band (2000×197, FORK 110's exact
  size and anchor), mirror-tiled foreground strip (the sea
  strip's role). Every note pixel in its band is painted out
  with cloned flowers; only the giants' green stalks remain,
  reading as flower stems.
- bee1–bee6.webp — the FORK 108 bee sprites. As of FORK 110 they are
  UNREFERENCED: the code neither loads nor draws them. The files stay
  on disk and on the site by decision; nothing in the game points at
  them.
- rainbow.webp — STAGED, NOT WIRED (asset prepared 2026-11-15).
  Keith's ruling (2026-11-15 22:43 ET): "You could put a single
  rainbow we pass / In the distance" — ONE rainbow, far away, passed
  once per run. It must NOT be baked into the tiling plates; wire it
  as a single far-plane sprite at a fixed world position.
  Source: route (a) — a fresh arc generated on pure black
  (`renders/flowerboy-src/media-generation-flowerboy-rainbow-onblack-v2-*.webp`;
  black chosen because every saturated chroma hue collides with one
  of the rainbow's own bands), lifted by additive max-channel alpha
  extraction + un-premultiply, ~22% atmospheric desaturation, alpha
  capped at 0.95. NOT extracted from the v1 master — its rainbow is
  a partial arc exiting the canvas corner. QC:
  `renders/flowerboy-src/rainbow-qc-v1.jpg`.
  Canvas 1600×880, lossless WebP, straight (un-premultiplied) alpha.
  Anchors for the wiring: visual centre x = 0.506 of width; arc top
  edge at y ≈ 0.015 of height; the FOOT LINE IS THE CANVAS BOTTOM
  EDGE — both feet dissolve to zero alpha right at the bottom, so
  anchor placements by the bottom edge and set it at or just below
  the hills line so the feet read as lost in the hills. Strong span
  (alpha > 0.25): x 0.065–0.946 of width.
