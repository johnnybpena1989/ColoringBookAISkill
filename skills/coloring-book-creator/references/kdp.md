# Amazon KDP paperback production and disclosure reference

Verified against public KDP pages on 2026-10-23. KDP can change specifications; recheck official pages during each publishing job if web access exists. Where the host can't browse, disclose that re-verification was not performed.

## Beginner paperback default

| Property | Default |
| --- | --- |
| Format | Paperback (not Kindle eBook) |
| Trim | 8.5 x 11 inches (215.9 x 279.4 mm) |
| Interior | Black ink on white paper |
| Bleed | No interior bleed |
| Artworks | 24 unique pages, one-sided |
| PDF pages | 50 total, title/copyright plus 24 art pages and 24 blank backs |
| Safe content region | At least 0.5 inch all around for this 50-page edition; also verify true KDP gutter minimum |
| Artwork | Original black-and-white drawings, minimum effective 300 DPI at actual print size |

The full raster page at 300 DPI is **2550 x 3300 pixels**. If artwork only occupies a 7.5 x 10-inch region, that region requires at least **2250 x 3000 source pixels** for 300 effective DPI; native pixel detail matters. Do not relabel 1024px files as printable 300 DPI at full-size without inspecting quality.

## Binding, pages and image quality

- KDP typically requires a **minimum of 24 pages** for B&W paperback, with maximum depending on stock and trim. The 50-page default meets the minimum.
- Submit **single pages**, not spreads/two-up.
- For no-bleed, PDF page size matches chosen trim exactly.
- For full bleed, KDP's manuscript needs 0.125 in extra width at the outside and 0.125 in at top and bottom (trim width + 0.125, trim height + 0.25). It is NOT a symmetric 0.125 bleed on both inner and outer edges. The default avoids this complication.
- KDP minimum image resolution is **300 DPI**. Avoid excessive 600+ DPI exports with huge files; verify actual effective resolution.
- For 24–150 pages, KDP minimum inside/gutter margin is **0.375 in**; outside (no-bleed) **0.25 in**. Our conservative 0.5-in art/text inset for the 50-page edition exceeds both. Higher page counts need a larger gutter.
- KDP recommends line thickness of at least **0.75 pt** for printed graphics. Very fine AI hairlines can disappear in print.
- Embed fonts in the PDF and verify actual sizes/rotation/legibility.
- Cover dimensions depend on **actual final page count**, stock and trim, so do not use precomputed dimensions for a different edition.
- Spine width for **B&W white paper** is page count x **0.002252 in**, but use official KDP calculator/template to validate.
- KDP permits spine text only for books with **more than 79 pages**; default 50-page book needs an unlettered spine.
- Paperback cover PDF is a **single back + spine + front full-wrap** flattened file, with **0.125-in outside bleed** and safe zones; reserve a barcode region per the official template.

## Disclosure and listing integrity

- In KDP's AI-content questions, **disclose AI-generated illustrations and cover art**. Text or translations created by AI can require disclosure as well. Distinguish AI-generated from AI-assisted as KDP defines it.
- KDP says coloring books generally are **not** low-content books; there can be exceptions. Do not automatically select the low-content category or invent an ISBN.
- The paperback is the preferred format: Kindle books intended mainly to be colored in are often unsuitable.
- Review image-use rights under the originating AI product's current terms; avoid third-party copyrighted artwork or trademarks and misleading attribution.
- Make no claims of bestseller status, official brand licensing or guaranteed KDP acceptance.

## Official pages

- [Paperback Submission Guidelines](https://kdp.amazon.com/en_US/help/topic/G201857950)
- [Set trim, bleed and margins](https://kdp.amazon.com/en_US/help/topic/GVBQ3CMEQW3W2VL6/)
- [Official cover calculator and downloadable template](https://kdp.amazon.com/en_US/cover-templates)
- [KDP content and AI-generated content policy](https://kdp.amazon.com/en_US/help/topic/G200672390)
- [KDP low-content book definitions](https://kdp.amazon.com/en_US/help/topic/GGE5T76TWKA85DJM)
- [Cover Creator](https://kdp.amazon.com/en_US/help/topic/G201113520)
- [KDP tools and resources](https://kdp.amazon.com/en_US/help/topic/G200735480)
