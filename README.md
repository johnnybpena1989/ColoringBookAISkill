# Coloring Book AI Skill v2

**A portable AI-agent coloring-book production workflow — no API keys, installers or coding.**

Use with ChatGPT, Claude, Grok or another assistant **that can open a GitHub URL and has native image/file tools**. The same [Agent Skills](https://agentskills.io/specification) document directs planning, illustration, quality checks, printable interiors, full-wrap covers and Amazon KDP listing preparation.

## Install with one CLI command

Requires Node.js and npm and a supported AI coding agent.

```bash
npx skills add johnnybpena1989/ColoringBookAISkill
```

The installer prompts for your target agent and install scope. To make the skill available across projects:

```bash
npx skills add johnnybpena1989/ColoringBookAISkill -g
```

To list the skill without installing it:

```bash
npx skills add johnnybpena1989/ColoringBookAISkill --list
```

Update later with `npx skills update`. The standard CLI is maintained separately at https://github.com/vercel-labs/skills. This repository supplies the skill files, **not** a custom executable. CLI installation supports compatible agent environments such as Codex and Claude Code; it does not install skills directly into consumer ChatGPT, Claude or Grok chat apps.

## One copy-paste command

> Read https://raw.githubusercontent.com/johnnybpena1989/ColoringBookAISkill/main/skills/coloring-book-creator/SKILL.md and follow it as my coloring book production workflow. Load its linked references as needed. Use your own native image and file tools; no API keys, installers, code or external services. Start by asking my theme and whether I want Autonomous or Guided mode. Create real downloadable book files wherever your tools allow; inspect and correct every page. Be explicit about anything your platform cannot actually produce.

**[Skill](skills/coloring-book-creator/SKILL.md) · [Quick start](START_HERE.md) · [Capability guide](skills/coloring-book-creator/references/platform-capabilities.md) · [Acceptance tests](skills/coloring-book-creator/references/acceptance-tests.md)**

## v2 workflow

1. **S0:** Detect host tools, set Autonomous or Guided mode, create persistent project ledger.
2. **S1:** Develop original book concept, titles, consistent style bible and 24-scene plan.
3. **S2:** Generate one real pilot illustration and visually approve it.
4. **S3:** Generate 24 original coloring illustrations in batches; individually QA and retain source files.
5. **S4:** Build and inspect an actual 50-page, 8.5x11 no-bleed interior PDF when native tools support it.
6. **S5:** Build and validate an actual full-wrap cover PDF against KDP's official template when tools support it.
7. **S6:** Draft honest Amazon listing copy, keywords and required AI-content disclosure guidance.
8. **S7:** Run explicit PASS/FAIL/UNVERIFIED production acceptance tests and deliver a project manifest.
9. **S8:** Human publisher uses KDP Print Previewer, reviews a physical proof and authorizes publication.

### Autonomous vs Guided

**Autonomous:** Agent makes creative and technical choices, batches production, fixes defects and only pauses for material approvals or irreversible actions.

**Guided:** Agent asks for concept and pilot approval and presents batch/cover checkpoints. Both modes preserve progress across interruptions.

### What this can and cannot do

The skill is a **full-lifecycle orchestration recipe**, not a hosted generation engine. Its ability to create actual high-resolution illustrations, PDFs or access KDP is limited by the user's AI platform, account plan, tools and usage quotas. It never promises 24 generated images or KDP-ready PDFs where those capabilities don't exist. **No API keys are required by this skill.**

The public GitHub URL is read on demand in new conversations; this is not a silent installation or automatic background sync. Anyone can view a public repo, so access cannot be sold as exclusive without separate gating.

Not affiliated with Amazon, OpenAI, Anthropic or xAI. AI-generated artwork must be disclosed to KDP. Print proof and publisher review are required before sale.
