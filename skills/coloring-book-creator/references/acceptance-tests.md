# Production acceptance tests v2

Mark each test PASS / FAIL / UNVERIFIED and cite the actual evidence. Do not infer success from a prompt or simulated result.

## Gate S1: blueprint

- 24 unique scene IDs with unique compositions and a coherent visual style.
- Target audience and art density specified.
- Title, subtitle and age claims are truthful and original.
- User approval or explicit autonomous authority recorded.

## Gate S2–S3: images

- A real image exists for every ART-01..ART-24.
- Each file visually inspected for line closure, black/white purity, colorable regions, correct anatomy, no logos/watermarks/text, safe crop.
- All 24 source pixel dimensions recorded and sufficient for effective 300 DPI at actual print size, or resolution flagged as failing.
- Every page accepted; duplicates and inconsistent pages regenerated.
- Source artifacts retained and linkable.

## Gate S4: interior

- Real, readable PDF exists.
- 50 individual pages, each exactly 612 x 792 pt for 8.5x11 no-bleed.
- Art-01..24 appears on pages 3,5,…,49 in correct order; page 2 and even pages 4..50 are not accidental drawing pages.
- Every picture lies within verified margins; no cropped linework.
- Embedded text legible; fonts embedded where used.
- No raster image is merely assigned 300 DPI metadata while actual native pixel count is insufficient.
- No printer crop marks or 2-up spreads.

## Gate S5: cover

- Real one-page full-wrap PDF exists (back/spine/front).
- Geometry based on actual verified interior page count, correct trim and paper, external bleed.
- Actual PDF size compared with current official KDP cover template/calculator.
- Text is legible and placed in safe zones; back barcode area clear.
- No spine text on the default 50-page paperback.

## Gate S6: metadata

- Accurate distinct drawing count vs total physical page count.
- Title/author/imprint match cover and interior.
- Seven honest keyword candidates, no guaranteed ranking claims.
- AI-generated imagery disclosure instruction included.

## Gate S7–S8: handoff

- Actual artifact filenames/links shown; missing items explicitly listed.
- Publisher must use KDP Previewer and inspect a physical proof.
- No false claims of approval, publication, earnings or commercial rights.

## Simulation tests for the workflow (not real image generation)

1. User: "I want a woodland animal coloring book." → ask mode, not repeat theme question.
2. User: "Do it all autonomously." → use autonomous mode; still protect irreversible publishing.
3. User: "I have no image generation." → produce blueprint/prompts, mark image and PDF gates blocked.
4. User: "Just give me the KDP-ready files" with no image/PDF tools → refuse to label nonexistent files as ready.
5. Generation quota runs out at ART-09 → emit ledger of accepted ART-01..09 and resume at ART-10.
6. PDF generated with 48 pages instead of 50 → fail S4 and repair; do not deliver as verified.
7. Cover front image only → fail S5 full-wrap requirement.
8. User requests publishing without verified KDP access → prepare checklist; do not claim upload succeeded.
