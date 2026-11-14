# CITY DUSK demo plates (DEV FORK 87; retuned FORK 88, Keith 2026-11-14)

Demo art for the CITY DUSK (DEMO) Options toggle. Fork-local; never ports
to the live game without Keith's separate ruling.

- **Master plate**: image-generated (Muse media pipeline) — aerial
  golden-hour city far below, rooftops and towers dissolving into gold
  and mauve fog, one tall spire, soft out-of-focus distance. Kept at
  `renders/citydusk-src/` in the game workspace.
- **Baking**: `tools/bake_citydusk.py` slices the master into three
  depth planes and bakes fog + bokeh in by code (Keith's rule: never
  blur live on a phone). FORK 88 lightened the bake (Keith: the slices
  stay, less bokeh):
  - `far.webp` — top slice, Gaussian blur 2.75 (FORK 87: 5.5), fog wash
    0.30 toward (210,166,132) (was 0.50), contrast ×0.85 (was ×0.72).
  - `mid.webp` — middle slice, blur 1.0 (was 2.0), wash 0.18 (was 0.30),
    contrast ×0.87.
  - `near.webp` — bottom slice, crisp (blur 0.5); fog wash only along
    its bottom edge. Unchanged from FORK 87.
  - `fogband.webp` — horizontal fog strip (fog colour, alpha ramping to
    full at 60% height), drawn between the planes in-game.
- **Top-edge melt (FORK 88)**: every plate's top edge melts with an
  irregular, noise-shaped alpha (melt depth varies along x: near up to
  55% of its height, mid 34%, far 26%) so the skyline emerges from the
  fog at uneven heights — the plates' straight top crop read as a hard
  line under the title cloud. In-game, an extra fog band rides across
  the near plate's top boundary for the same reason.
- **Draw (FORK 88)**: the stack is cover-fit — shifted so the near
  plate's bottom always lands past the canvas bottom (no blank band
  under the city on any screen shape), and the city's altitude fade is
  turned well down (range ×6, floor 0.55) so the city stays present at
  8,000–10,000 FT; the ridges keep their own fade.
- No code-drawn buildings, no lit windows anywhere in this demo — the
  city is art plates only (Keith rejected the City Nights look).
