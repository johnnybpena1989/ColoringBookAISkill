# Coloring-book art direction and prompt system

Use this only after reading SKILL.md. The purpose is to produce **cohesive, usable coloring artwork**, not generic attractive AI images.

## Set one style bible per book

Decide: age/skill level, average contour thickness, detail density, number of major colorable regions, recurring motifs, background density, margin size, and visual rhythm. Reuse these values across all 24 designs.

| Audience | Subject count | Complexity |
| --- | --- | --- |
| Ages 4–6 | 1–2 large recognizable objects | Very large shapes, big open interiors, almost no background |
| Ages 7–12 | 1 main scene and 1–3 details | Balanced moderate intricacy |
| Teens/adults | 1 main composition with layered ornaments | Dense but readable enclosed regions, not a dark scribble |

## Original theme starters

- Cozy cabins and woodland friends: fireplaces, tea, foxes, pumpkins, mushrooms, rain.
- Ocean garden creatures: seahorses, turtles, coral, shells, currents and treasure.
- Enchanted miniature villages: mushroom cottages, lantern bridges, garden kiosks.
- Botanical serenity: potted plants, ornamental borders, greenhouse arrangements.
- Friendly prehistoric explorers: unique dinosaurs in playful ancient landscapes.
- Whimsical food trucks: imaginary dessert trucks, cafés and markets without logos.
- Space gardening: robots caring for planetside plants, lunar greenhouses, asteroids.
- Cottagecore holidays: original non-branded seasonal scenes.

Theme list is inspiration, not a guarantee of originality or demand. Do not use copied illustrations or franchise branding.

## Composition variety mandate

For a 24-page book, distribute views among close-up subject studies, full-scene vignettes, medium-view interactions, symmetrical decorative spreads and border motifs. Vary subject, direction, scale, backdrop and negative space. Do not repeat the same character pose and simply change props. Avoid text puzzles or overlong verbal instructions inside the image.

## Reusable generation master prompt

Portrait vertical 2D printable coloring-book illustration. SUBJECT: <SCENE>. CREATIVE SYSTEM: <CONSISTENT STYLE BIBLE>. Clean smooth solid black connected lines on pure white background; no gray, halftone, gradients, shading, colored pixels, texture, watercolor, crosshatching, shadow, filled-in dark regions, lettering, logos, watermarks or signatures. Distinct closed shapes with generous room to color. Entire artwork inside generous white-safe border. Accurate recognizable anatomy and object structure, readable foreground/midground separation, balanced use of white space. Original unbranded artwork. High-definition line clarity appropriate for print. Do not include page frame unless specified in the style bible.

## Negative cues and repairs

- Fuzzy gray image → request pure two-tone line art, no antialias-heavy blur, no pencil sketch.
- Filled black areas → require unfilled white interior in clothing, fur, hair, leaves, clouds and buildings.
- Unclosed contours → simplify shape groups; generate large closed outlines with crisp intersections.
- Dense noise → reduce leaf, petal, fur, and background pattern count; enlarge white space.
- Cropped tails/ears/horns → scale scene down and put all objects within a white perimeter.
- Text gibberish → remove in-image lettering; typeset externally for cover and front matter.
- Repetition → rewrite composition and change visual viewpoint, pose, focal point and environment.

## Source image treatment

Retain source dimensions and approval status. Work from lossless files if native tools allow. Upscaling and binary thresholding may help clean previews but cannot create true original detail; inspect actual print-size edges. If effective print resolution is inadequate, regenerate at supported higher native detail or **flag it**. Do not claim an untested upscale is press-ready.

## Book consistency audit

Review the page set together: contour weights, age suitability, degree of difficulty, topic coverage, image completeness, number of near-duplicates and ink coverage. A visually consistent but boring book still fails creative QA.
