# Coloring Book AI Skill

**One link. A guided AI coloring-book production workflow. No API keys, code, or installer required.**

This repository contains a vendor-neutral [Agent Skill](https://agentskills.io/specification) that guides a complete beginner from a coloring-book idea through original artwork, print-layout checks, and a draft Amazon KDP listing.

## Give your AI this one instruction

> Open and read https://raw.githubusercontent.com/johnnybpena1989/ColoringBookAISkill/main/skills/coloring-book-creator/SKILL.md and follow it as my coloring book creator. Read any reference files you need from the same GitHub repository. Start a new coloring book project with me now, use your built-in image and document tools where available, and guide me through the entire process one decision at a time. Do not require programming, software installation, or an API key. Tell me explicitly if you cannot open the link or create a required file.

**[Open the skill](skills/coloring-book-creator/SKILL.md) · [Beginner instructions](START_HERE.md) · [Project template](templates/BOOK_BRIEF.md)**

## The workflow

1. Pick a theme and audience. The AI provides ideas for anyone who doesn't know where to start.
2. Develop an original series of 24 coloring-page concepts in one coherent illustration style.
3. Generate and review every image using the AI platform's own image-generation capability, if available.
4. Assemble a single-sided paperback interior: 8.5 x 11 inches, black ink on white paper, 50 pages by default.
5. Produce a professional front-cover concept, paperback wrap where possible, and Amazon listing copy.
6. Validate print dimensions, image detail, page order, originality, and KDP disclosure before publishing.

## What "universal" means

The instructions work as a standard [Agent Skills format](https://agentskills.io/specification) and can also be read directly as a prompt by ChatGPT, Claude, Grok, or another assistant that can open a GitHub URL. No external image API is used.

**Platform capabilities are not universal.** Some assistants cannot browse GitHub, generate 24 images, keep files between turns, produce PDFs, or export press-ready covers. The skill must disclose those limitations and generate the best useful artifacts it can—**never claim completion when outputs don't exist**. An AI subscription may impose image-generation quotas. There is no promised unlimited free generation.

## Cloud updates

This repository is the source of truth. Every time a user starts a new book with the instruction above, their AI is asked to fetch the latest version. This is **read on demand**, not a persistent automatic installation or background sync.

## For the creator / seller

This repository is currently **public**. Anyone who knows the URL can read the workflow, and GitHub does not collect license payments for you. See [TERMS.md](TERMS.md) and [SELLER_NOTES.md](SELLER_NOTES.md) for distribution considerations.

## KDP and rights

Books must contain original publishable content, undergo human review, and follow current Amazon KDP rules. KDP requires disclosure of AI-generated cover and interior artwork. Coloring books are generally not classed as low-content books. See the [print reference](skills/coloring-book-creator/references/kdp.md).

_Not affiliated with Amazon, OpenAI, Anthropic, or xAI. Does not guarantee KDP acceptance, sales, or commercial rights to every generated image._
