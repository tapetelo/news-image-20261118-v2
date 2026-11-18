# news-image-20261118 — Entry 2

[![make.fun · news-image-20261118](https://make.fun/badge/news-image-20261118.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)
[![rank](https://make.fun/badge/news-image-20261118/tapetelo/news-image-20261118-v2/rank.svg)](https://make.fun/bounty/news-image-20261118/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)
[![reward](https://make.fun/badge/news-image-20261118/tapetelo/news-image-20261118-v2/reward.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)

**Entry 2** for the make.fun competition
**"Sum up 18 November's world news in one image"**
(`news-image-20261118`), account @tapetelo, repo
`tapetelo/news-image-20261118-v2`.

**"The World Today — Wednesday 18 November 2026"** — a dense
newspaper front page summing up the day in a single image, with
**41 stories** on the page. `entry.png` is the bright/clear
1024x1024 version (near-white paper, darkened ink and rules —
see "High resolution + brighter / clearer" below).

## The image

A dense newspaper front page, 1024x1024, bright near-white paper
(`entry.png`, genuine PNG, 320,995 bytes — under the 1 MiB gate;
SHA-256 `03f22944e2dcfb739e0e1e1efccb0d3ed061d2e76f5e95231a577ca7f36f3ac6`):

- Masthead: **THE WORLD TODAY — WEDNESDAY 18 NOVEMBER 2026 •
  41 STORIES • 5 CONTINENTS • ONE DAY**
- 3 hero stories across the top, each with a drawn illustration
  (Pillow shapes/icons only, no photos): Gulf drone interceptions,
  the Xi–Putin talks in Shenzhen ahead of the first Trump–Xi–Putin
  trilateral, and the Kerch Bridge arch collapse.
- 12 medium stories in a 4×3 grid below the heroes, each with its
  own small drawn illustration strip at the top of the box
  (Alaska peaks/star, cyclone spirals, Nvidia chip + rising chart,
  drones, dove + olive branch, virus + clinic cross, Africa map +
  red cross, AI robot + circuit, £ + rising arrow, Voyager dish,
  Australia map + gavel).
- Bottom left: **WHERE IT HAPPENED** — a schematic drawn world map
  with 20 numbered pins and a legend. Bottom right: **ALSO ON
  WEDNESDAY 18 NOVEMBER** — numbered briefs 16–43.

## Story list (41 on the page)

Sole source: `../news-image-20261118-v2-draft/research.md` — its
exact corrected wording was used; nothing was invented, and none
of entry 1's errors were reused.

- **Heroes (3):** H1 Gulf skies alight — Kuwait/Bahrain intercept
  drones (Kuwait's statement did not name Iran; Bahrain blamed
  Tehran); H2 Three leaders, one table — Xi–Putin talks in
  Shenzhen, eve of the first Trump–Xi–Putin trilateral; H3 Kerch
  Bridge arch collapses under Ukrainian strike (strike reported
  17 Nov; it led the 18 Nov front pages — the body text does not
  claim it happened on 18 Nov).
- **Medium (12):** M1 Peltola flips Alaska, Senate 56–44; M2
  Cyclone Xavier Cat 5, N. Cook Islands; M3 Nvidia doubles revenue
  $115.8bn; M4 Russia fires 141 drones at Ukraine; M5 Board of
  Peace warns Gaza truce faces collapse; M6 Cyclone Akvan bears
  down on India's east coast (landfall forecast 20 Nov — stated);
  M7 US loses measles-free status; M8 Ebola in DR Congo passes
  11,000 cases; M9 Anthropic prices $90bn IPO; M10 UK inflation
  3.6%, one-year high; M11 Voyager 1 reaches one light-day;
  M12 Australia sanctions Daniella Weiss.
- **ALSO briefs (26):** #16–30 and #33–43 from the research list.

**Cut for space (in the brief's drop order): #44, #32, #31** — all
flagged roundup-only / weak source in the research. **Excluded
entirely:** the unverified 1,200-drone claim and the stale
Naro-Fominsk corvette story (11 Nov).

**Known gap:** no verified Latin America story was found, so the
map has no LatAm pin; this is stated on the page itself
("No verified Latin America story").

## High resolution + brighter / clearer (2026-11-18 ~20:50 WIB)

User asked for a high-resolution version that looks bright and
clear. The kit ceiling is 1024x1024, so the submittable file stays
1024x1024 — **only `entry.png` (1024x1024) can be submitted**.
A second file is provided for viewing only:

- `entry-hires.png` — **2048x2048, VIEWING ONLY, NOT submittable**
  (over the kit's 1024 ceiling). 689,499 bytes, genuine PNG,
  SHA-256 `485e089ab6c2c0cd0d44e410c389ce2100dc10e856c5930c4b6c4023c798bc38`.
  Built with `python3 render.py hires`.
- It is a **true redraw, not an upscale**: `render.py` is now
  scale-parameterised (`SCALE=1` or `2`). All layout code stays in
  1024-space; a `ScaleDraw` proxy scales every Pillow coordinate,
  line width and font size by 2x at the draw boundary, so fonts,
  illustration strips, map, pins and legend are all rendered
  natively at 2048. Proof: mean absolute pixel difference vs a
  Lanczos upscale of the 1024 file is 16.66/255 (max 255) — the
  hires file is visibly crisper, with sharp text edges.
- **Brightening, applied identically to both files:** paper
  CREAM 247,241,227 → 250,246,236 and PAPER 252,248,238 →
  255,253,248 (near-white warm); INK 20,20,20 → 10,10,10
  (near-black); RED 178,34,34 → 168,22,22; BLUE 30,70,130 →
  18,58,120; rules/grey darkened for contrast; map land
  brightened to 233,219,184. Plus a mild finish on the whole page:
  contrast +6%, sharpness +15%. No story fact or wording changed;
  the M2/M5/M6/M8 trimmed summaries are exactly as fixed before.
- **Verified:** the text-fit guard still passes for all 15 blocks
  at both scales (it runs in 1024-space); both files visually
  inspected, including 2x enlarged medium-box crops of the hires
  file — no text touches or crosses any box border in either file.
  512px preview of the submit file re-checked: PASS (masthead,
  hero and medium headlines readable; summaries small but legible).
  Two grader-style runs of `main.py` in fresh copies, exit 0,
  byte-identical to the bundled `entry.png`.

## Ultra high resolution (2026-11-18 ~20:58 WIB)

Zooming the 2048 preview in chat looked blurry. That is mostly
the chat preview, not the file: the chat app downscales the image
to fit the screen first, and zooming the preview zooms that
already-downscaled copy — the original file underneath is sharp.
Two things were done about it:

- `entry-ultra.png` — **4096x4096, VIEWING ONLY, NOT submittable**
  (over the kit's 1024 ceiling and 1 MiB gate). 50,351,853 bytes
  (~48 MB, deliberately big: saved with PNG `compress_level=0`,
  no optimisation), genuine PNG, SHA-256
  `b76a220a3d9dda57c74c59cfe3d77bb13932717b5941a00f96c4f287b7821552`.
  Built with `python3 render.py ultra` (S=4 true redraw — same
  scale-parameterised renderer, fonts loaded at 4x sizes, so every
  letter and shape is drawn natively at 4096, not upscaled).
  **To zoom: open this file itself** (download it and open it in a
  photo viewer / browser), not the chat preview — at 100% the
  masthead serifs and body text have clean, crisp edges (verified
  from native 100% crops of the masthead and the M1/M2/M5/M6
  boxes). Text-fit guard still passes for all 15 blocks.
- **No vector PDF.** A true vector PDF (selectable text, infinite
  zoom) would need the whole Pillow layout re-implemented in a
  vector library — reportlab is not installed here and the system
  pip refuses installs (PEP 668), and re-implementing ~1,000 lines
  of drawing code risks a layout that no longer matches the PNG.
  So no PDF was shipped rather than a broken or merely
  raster-embedded one. The 4096 PNG is the zoom solution: at 4x
  the submit size it stays sharp through any normal zoom.
- `entry.png` (1024) and `entry-hires.png` (2048) were NOT
  touched — their SHA-256 values are unchanged from the previous
  section.

## How it was built

- `render.py` — the Pillow renderer (local only; not part of the
  graded submission). Liberation Serif (headlines/masthead) +
  DejaVu Sans (body/labels). All artwork is drawn: drone
  silhouettes and sky bursts, three flag panels with leader
  silhouettes, a broken bridge arch, and a schematic continent map.
- `main.py` — stdlib-only; copies the pre-rendered `entry.png`
  to `$MAKEFUN_OUTPUT_DIR/entry.png`, exactly as the 17 Nov V3
  entry did.
- `preview-512.png` — a 512px downscale used for the readability
  check (the size the judge reads).

## Text-overflow fix (2026-11-18 ~20:33 WIB)

Enlarged crops showed four medium summaries touching or crossing
their box bottoms: M2's last line sat on the border, M5's 3rd line
was half cut off, M6's 3rd line spilled into the next row, and M8's
last line sat on the border. Root cause: a 2-line headline + 2-line
summary already filled the 112 px box under the old spacing, so
any 3-line summary overflowed by up to 14 px. Fixed in `render.py`:

- **Text-fit guard (real, measured):** every hero and medium text
  block is wrapped with the actual font metrics before drawing, and
  its bottom must stay ≥ 4 px inside its box. A medium summary
  that would overflow is retried at 10 pt; if it still does not
  fit, `compose()` raises instead of saving. The render now passes
  the guard for all 15 text blocks (heroes end exactly 4 px inside
  their boxes; medium blocks end 9–25 px inside).
- **Tighter spacing:** illustration strip 34 → 28 px, label at
  strip + 4, headline at strip + 18, headline leading 17 → 16,
  summary leading 13 → 12.
- **Illustration strips are tile-clipped:** each strip is drawn on
  its own tile and pasted in, so no art shape can bleed into a
  neighbouring box. The old M6 coastline arc used to spill into
  the M2 box above and M6's own text area; it now stays inside
  its strip.
- **Exact wording changes (facts kept, clauses dropped):**
  - M2: "Gusts to 315 km/h hit Pukapuka and Nassau — strongest
    since 2020." → "Gusts to 315 km/h hit Pukapuka and Nassau."
  - M5: "US-backed board tells the UN the year-old ceasefire may
    not hold; 1,650 killed since it began." → "US-backed board
    tells the UN the truce may not hold; 1,650 killed."
  - M6: "Severe storm stalls in the Bay of Bengal; landfall
    forecast 20 Nov near Andhra Pradesh, gusts 145 km/h." →
    "Severe storm stalls in the Bay of Bengal; landfall 20 Nov,
    gusts 145 km/h." (Andhra Pradesh dropped; date + gusts kept)
  - M8: "Second-largest outbreak on record; 5,400 deaths; 3 in 4
    infected under-fives die." → "Second-largest outbreak on
    record; 5,400 deaths." (under-five stat dropped)
  All four summaries now fit in 2 lines.
- **M10 strip nit fixed:** the white "3.6%" label used to overlap
  the rising arrow; the £ is now 24 pt, "3.6%" sits top-centre,
  and the arrow starts right of it in the lower half.
- **Verified:** every medium box and all 3 heroes re-checked from
  3x enlarged crops — no text touches or crosses any box border.
  Per-box: M1 ✓ (3-line summary, 13 px margin), M2 ✓, M3 ✓,
  M4 ✓, M5 ✓, M6 ✓, M7 ✓, M8 ✓, M9 ✓, M10 ✓, M11 ✓, M12 ✓,
  H1/H2/H3 ✓ (4 px margin each). 512px preview re-checked, still
  readable.

## Readability check (512px)

Masthead, subline, hero headlines and medium headlines stay
readable at 512px. Hero/medium summaries and the ALSO briefs are
small but legible — the dense-newspaper look of the leaderboard
top 5. To fit the medium illustration strips, the medium boxes
grew taller (heroes and the map shrank slightly, ALSO briefs went
to 10pt); hero summaries H1/H3 were trimmed by one clause each
(facts unchanged) so no text overflows its box. The masthead count
was corrected from "6 CONTINENTS" to "5 CONTINENTS" — no verified
Latin America story exists on the page.

## Verification

Two grader-style runs in a fresh copy
(`MAKEFUN_OUTPUT_DIR=out python3 main.py`) both exit 0 and write
byte-identical outputs (same size and SHA-256 as the bundled
`entry.png`).

## Files

- `entry.png` — the finished page (1024x1024, PNG) — the ONLY submittable file
- `main.py` — stdlib-only grader entrypoint
- `README.md` — this file
- `LICENSE` — MIT (copied from the 17 Nov V3 entry)

Not in this repo (local/viewing only): `entry-hires.png`
(2048x2048), `entry-ultra.png` (4096x4096, ~48 MB),
`preview-512.png` (512px readability preview) and `render.py`
(the Pillow build script) — see the sections above.
