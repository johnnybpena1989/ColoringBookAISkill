# Quality control: image, book and delivery

This document supplies inspection tests. Mark a check as **Pass / Fail / Unverified**; do not turn unknown into pass.

## Per-image review (all 24 must be inspected)

1. Topic and audience: is it a recognizable, appealing original scene at the expected skill level?
2. Line art: black outlines on white; no gray fills, smeared outlines, blurry antialias artifacts, shadow gradients, large inked black regions, accidental colors or texture.
3. Geometry: subjects have plausible limbs, eyes, fingers, ears, wheels and spatial connections. Count required parts where relevant.
4. Colorability: clear enclosed regions, practical coloring spaces, no accidental open shapes and no dense tangles.
5. Layout: no cut-off subject/illustration, consistent portrait proportion and generous white edges.
6. Branding: no existing licensed characters, marks, celebrity likenesses or imitations of a named living artist.
7. Differentiation: not a near-duplicate of another page; book does not promise material absent from the page.
8. Print image size: record source pixels and intended printed dimensions. Effective DPI = image pixels / printed inches in each direction. Target >=300 effective DPI at printed scale; lower => Unverified/Fail, not a fake pass.
9. File integrity: image really exists and can be opened, not merely described in chat.

### Disposition

- Pass all tests: Approved.
- Fixable image: Rejected; regenerate and recheck.
- Unable to inspect resolution, file or rights: Draft / Unverified, not "KDP ready".

## Cross-book audit

- 24 unique scenes exist; names align with approved concept list.
- Visual style consistent; background complexity varied thoughtfully.
- 50-page default map correct: title on 1, copyright on 2, 24 art pages at 3/5/…/49, blanks on 4/6/…/50.
- Blank backs are truly blank; front/back orientation and pagination are correct.
- No accidental blank art page or unintended dark backgrounds.
- Clear title and author text; author/publisher permission confirmed.
- Marketing claims match the actual book.
- All user-requested changes reflected in files and metadata.

## PDF and cover print checks

Check actual file, not a mockup or description: interior and cover PDFs are real, readable, separate, and complete. Interior single-page pages, correct trim, appropriate no-bleed/bleed mode, safe gutters/margins, at least 300 effective DPI for printed images, embedded fonts and no crop marks. Confirm exact page count and pages in the actual file.

Cover needs its own full wrap, computed for ACTUAL page count and chosen stock; correct spine, full bleed and safe regions, back/front ordering, clear barcode zone and no default spine lettering under the KDP minimum. Use the official KDP template to validate; the illustration itself is not a printable wrap.

If not able to inspect any given property, explicitly mark **Unverified** and don't issue a "print-ready" claim.

## Final human gate

Publisher must visually inspect every page, upload to KDP Print Previewer, resolve all warnings and ideally order a physical proof. Review accuracy, margins, spine, barcode, page order, ink coverage and real printed lines. **No AI-only approval substitutes for this.**
