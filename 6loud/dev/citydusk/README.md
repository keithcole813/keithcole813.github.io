# CITY DUSK demo plates (DEV FORK 87, Keith 2026-11-14)

Demo art for the CITY DUSK (DEMO) Options toggle. Fork-local; never ports
to the live game without Keith's separate ruling.

- **Master plate**: image-generated (Muse media pipeline) — aerial
  golden-hour city far below, rooftops and towers dissolving into gold
  and mauve fog, one tall spire, soft out-of-focus distance. Kept at
  `renders/citydusk-src/` in the game workspace.
- **Baking**: `tools/bake_citydusk.py` slices the master into three
  depth planes and bakes fog + bokeh in by code (Keith's rule: never
  blur live on a phone):
  - `far.webp` — top slice, heavy Gaussian blur, strong fog wash toward
    (210,166,132), contrast ×0.70.
  - `mid.webp` — middle slice, light blur, moderate wash, contrast ×0.87.
  - `near.webp` — bottom slice, crisp; fog wash only along its bottom edge.
  - `fogband.webp` — horizontal fog strip (fog colour, alpha ramping to
    full at 60% height), drawn between the planes in-game.
- No code-drawn buildings, no lit windows anywhere in this demo — the
  city is art plates only (Keith rejected the City Nights look).
