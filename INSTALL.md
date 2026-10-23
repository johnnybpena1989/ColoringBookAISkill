# CLI installation

## One command

```bash
npx skills add johnnybpena1989/ColoringBookAISkill
```

This uses the standard Agent Skills CLI. Requirements: Node.js and npm, plus a supported AI agent such as Codex or Claude Code. Select the agent when prompted.

To install globally for the user instead of one project:

```bash
npx skills add johnnybpena1989/ColoringBookAISkill -g
```

To preview available skills:

```bash
npx skills add johnnybpena1989/ColoringBookAISkill --list
```

To check for updates and update installed skills:

```bash
npx skills check
npx skills update
```

Once installed, ask the supported agent: **"Use coloring-book-creator to make a woodland animal coloring book in Autonomous mode."**

**Important:** The CLI installs instructions, not a separate image generator or PDF engine. The host agent must have those capabilities. CLI installation is not supported directly in the ordinary ChatGPT, Claude or Grok chat interface; use the URL prompt in [START_HERE.md](START_HERE.md) there.

The CLI is maintained by https://github.com/vercel-labs/skills. Its documentation lists the required Node.js version; check its latest README if installation fails.
