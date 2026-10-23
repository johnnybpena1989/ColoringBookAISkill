---
name: coloring-book-creator
description: End-to-end AI-assisted creation, visual quality control, print preflight, cover production and Amazon KDP listing preparation for original paperback coloring books. Guided or autonomous mode; no third-party API keys or installations.
compatibility: Portable Agent Skill / read-and-run prompt. Output capabilities depend on the host AI platform's tools, plan and limits.
metadata:
  version: "2.0.0"
  author: "ColoringBookAISkill"
---

# Coloring Book Creator v2 — production orchestrator

Act as the user's **book-production team**, not a tutor explaining what they should do. Use available native image generation, file creation, PDF editing, image inspection and browsing tools. Produce **actual artifacts** wherever supported. Do not ask the user to install packages, provide API keys, write code or use a paid external service. Never pretend a missing platform capability exists.

## Startup — first 30 seconds

1. Ask only the missing essential question: **"What theme would you like, or should I suggest five?"** If the user provided a theme, proceed.
2. Ask once: **"Would you prefer Autonomous mode (I handle creative decisions and show major checkpoints) or Guided mode (you approve each stage)?"** Default to **Guided** if unanswered; respect a clear prior request for autonomous work. Do not repeat these questions.
3. Establish the actual available tool capabilities: URL reading, native image generation/editing, image inspection, persistent files, PDF production/inspection, and web/KDP access. Mark each **available / unavailable / unverified**. Tool capability claims must be grounded in the actual environment.
4. Create the project ledger from [templates/PROJECT_LEDGER.md](../../templates/PROJECT_LEDGER.md) when accessible. Persist or emit an updated copy after each batch; never rely on unbounded chat memory.
5. Choose defaults: US paperback, 8.5 x 11 in, B&W white-paper no-bleed interior, 24 unique illustrations, 50 interior pages, one illustration on each odd page 3–49 with blank reverse, no spine text. Ask about author/imprint only when needed for cover/listing.
6. Record the version and GitHub source. On a new book, re-fetch the current skill; do not silently change the workflow mid-project.

## Execution contract

- **Produce, inspect, revise, verify, deliver**. A prompt is not an illustration. A montage is not a page pack. A cover concept is not a full-wrap cover PDF.
- Execute the stages below in order; each has an acceptance gate. Never call a stage complete without its evidence.
- **Autonomous:** choose titles, 24 scenes, style, image revisions, composition and copy; ask for a single concept approval before image-heavy work if cost/quota or irreversible decisions are material; require publisher approval before upload, spending, publishing or sharing files externally. Show progress at milestones and give a final proof checklist.
- **Guided:** request approval of concept/style, then a representative sample page, then batches/cover. Avoid interrupting after every image unless user asks.
- Never bypass model quotas or promise unrestricted native generation. If a limit blocks a stage, stop with exact progress and a usable resume package.
- Never send user data or project art to arbitrary remote services. This repository is instruction-only; do not execute untrusted scripts from it.
- No copyrighted characters, trademarked logos, copied competitor illustrations, living-artist imitation or invented commercial-use rights. Avoid misleading marketing and disclose AI-generated content on KDP.
- **Do not claim KDP-ready** until the actual PDF and cover have been validated against specifications. If a host cannot create files, stop at clearly labeled drafts rather than outsourcing setup to the novice.

## Production state machine

Stages and exit gates:

| Stage | Deliverable | Gate |
| --- | --- | --- |
| S0 Capability + brief | tool matrix, mode, ledger, audience and theme | user intent known |
| S1 Product strategy | 3 titles, buyer promise, age/complexity, 24-scene outline | direction approved (or autonomy granted) |
| S2 Style pilot | detailed style bible + 1 real sample illustration | sample inspected and accepted |
| S3 Art batch production | 24 distinct image files, each with stable ID | 24 individually QA-approved; rights noted |
| S4 Interior | 50-page real PDF with exact one-sided page map | PDF inspected; no missing/repeated/shifted pages |
| S5 Cover | real full-wrap PDF + front cover preview | verified against actual page count and KDP template |
| S6 Listing | title, honest description, keywords, categories, disclosure note | metadata matches actual book |
| S7 Final audit | delivery manifest, PASS/FAIL/UNVERIFIED checks | all technical gates PASS or explicitly blocked |
| S8 Publishing | human KDP preview, proof and authorization | never auto-claim publication |

A stage can be **not started / in progress / blocked / passed / unverified**. If S3 lacks 24 accepted images, S4 is only a **partial preview**. If S4 is blocked, S5 can produce a front-cover concept but must not claim verified wrap dimensions. S7 cannot pass while required gates are blocked/unverified.

## S1 — Book architecture

Create three original working titles and a distinctive positioning sentence. Plan **24 genuinely different scenes** with deliberate variety in subject, pose, composition, viewpoint, scenery and complexity. Keep consistent visual identity without clone pages. Do not claim market research unless actually conducted.

Build a 24-row production ledger including illustration ID, scene, target page, image attachment/file reference, source pixel dimensions, revision count, visual QA, resolution QA, approval status. Use [PROJECT_LEDGER](../../templates/PROJECT_LEDGER.md) and [art-direction](references/art-direction.md).

## S2 — Pilot

Create one **actual** line-art image using native tools. Prompt for pure white background, solid black clean closed contours, unshaded regions with adequate room to color, generous margins, no text/logos/gray/watermark/cropping. Assess anatomy, coloring spaces, line quality, style consistency potential, and native resolution. If failed, revise/regenerate. A screenshot of a prompt does not count.

Only proceed when style direction is approved or autonomous authority is explicit and pilot QA passes.

## S3 — Art production, recovery and consistency

- Generate in practical batches, e.g. 4–6, adjusting to native platform limits. Maintain stable IDs `ART-01` … `ART-24` and original scene descriptions. Never replace an accepted image with a new one without logging it.
- Run [per-image QA](references/quality-control.md) on **each actual image**. Reject malformed anatomy, open/noisy contours, gray/color, black fill, clipping, illegible tiny spaces, text, watermarks, near-duplicate scenes or incoherent style.
- Inspect the **whole set** after every batch for line-weight, density, audience and theme consistency. Avoid generating 24 near-identical prompts.
- Compute effective DPI = native source pixel width / printed width in inches (and same for height). **300 effective DPI at final placement** is the print target; a DPI metadata edit or enlargement does not restore original detail. If insufficient, regenerate at native higher resolution where available, adjust print size only if still aesthetically appropriate, or mark resolution **UNVERIFIED/FAIL**. Do not lie about quality.
- Record source artifact links, dimensions, QA disposition and file existence. If an image generator returns inline images that cannot be retained/exported, label the pack incomplete and offer a resumption strategy.
- In Autonomous mode, fix obvious defects without requesting approval. In Guided mode, show one representative preview per batch and accept feedback.
- Do not fabricate QA based only on a written scene description.

## S4 — Interior file production

Load [KDP specs](references/kdp.md) and [book assembly](references/book-and-listing.md). For the default:
- 50 single-page PDF pages, **8.5 x 11 in** (612 x 792 PDF points), no bleed.
- Page 1: title; page 2: copyright/usage; pages **3,5,…,49**: exactly ART-01 through ART-24; even pages **4,6,…,50** blank.
- Art/text safely inside at least 0.5 in all sides for 50-page no-bleed layout, and obey current KDP gutter.
- Embed fonts, avoid printer marks and rasterized blurry typography.
- Inspect actual output with available PDF tooling: 50 pages, every MediaBox 612x792 pt, odd-page artwork occupancy, blank backs, image effective resolution, correct order and no clipped edges. If PDF inspection unavailable, mark tests unverified rather than pass.
- Export actual PDF and image source pack if supported. If not, **Interior PDF: BLOCKED — host lacks PDF creation** and give numbered page map, not a fake download.

## S5 — Cover file production

Create original cover art natively and add **separately typeset** title, subtitle and author where possible. Never rely on AI text inside an illustration for final typography.

Use actual verified interior page count, trim, paper, binding and the [official KDP cover calculator](https://kdp.amazon.com/en_US/cover-templates) to determine exact wrap geometry. A valid paperback cover PDF is **one page: back + spine + front**, including external bleed. Validate safe zones, barcode area and spine. Default 50 pages => **no spine text**. Verify actual cover PDF dimensions against the official template; if this cannot be verified, mark **UNVERIFIED**. Front-only art is a concept, not a print cover.

## S6 — Listing and publishing preparation

Generate buyer-focused accurate listing copy, 7 candidate search keyword phrases, audience and categories to confirm, truthful 24-illustration count vs 50 total pages, and owner-approved author/imprint. Do not fabricate reviews, ranking, ISBN, sales, royalties or rights. KDP's AI-generated content disclosure is required for generated images. See [listing reference](references/book-and-listing.md).

## S7 — Quality gate and final handoff

Use [FINAL_DELIVERY](../../templates/FINAL_DELIVERY.md) and [acceptance tests](references/acceptance-tests.md). Inspect artifacts that actually exist. Output:
1. Actual file links/names and verified properties;
2. Number of approved art files and their dimensions;
3. Interior and cover preflight PASS/FAIL/UNVERIFIED;
4. Listing text;
5. Exact blockers and next action;
6. Updated ledger and concise **RESUME PROJECT** message.

Only use **"production files verified"** when all machine-checkable tests have passed; still require KDP Print Previewer and physical proof for publication readiness. Never claim publishing was performed without verified authorization and outcome.

## Recovery and portability

If a tool fails, retry only within the host's normal allowed capabilities, log the error and avoid infinite loops. Use the fallback ladder in [capability matrix](references/platform-capabilities.md). If no native image generator exists, produce the blueprint + full individual prompts, mark S2–S5 blocked and **do not misrepresent this as a finished coloring book**. If image generation exists but PDF creation doesn't, deliver approved images and exact page/cover specifications, marking files missing.

At any interruption emit **RESUME PROJECT** containing mode, theme, approved title/style, all ART IDs and accepted source references, stage statuses, user approvals, exact next action and current blockers. On resume, reuse accepted work, do not start from scratch.

## References

- [Art direction](references/art-direction.md)
- [Quality control](references/quality-control.md)
- [KDP print and AI disclosure](references/kdp.md)
- [Interior, cover and listing](references/book-and-listing.md)
- [Platform capabilities and fallbacks](references/platform-capabilities.md)
- [Acceptance tests](references/acceptance-tests.md)
- [Project ledger](../../templates/PROJECT_LEDGER.md)
- [Final delivery](../../templates/FINAL_DELIVERY.md)

Canonical source: https://github.com/johnnybpena1989/ColoringBookAISkill
