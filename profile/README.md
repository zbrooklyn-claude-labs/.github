<div align="center">

# Zbrooklyn Claude Labs

**Open-source infrastructure for AI-assisted development**

We build the missing pieces — the tools you reach for when your AI coding agent
hits a wall it shouldn't have hit.

[Browse Projects](#projects) · [About](#about)

</div>

---

AI coding tools are fast, but they have blind spots. They write frontend code they can't see. They claim things work without checking. They lose context when you move a folder. They review their own work and call it done.

This org exists to close those gaps. Every project here came from a real workflow problem — something that broke, something that was missing, something that should have existed already. If you work with AI coding agents daily, you'll probably recognize a few of them.

---

## Projects

### [Playwright Pool](https://github.com/zbrooklyn-claude-labs/playwright-pool)
**Give your AI agent a real browser.**

Most AI coding tools are blind — they can write frontend code but never see what it actually looks like. Playwright Pool is an MCP server that gives any AI coding tool full browser control with persistent authentication.

- **75+ tools** — navigate, click, fill forms, screenshot, run JavaScript
- **28 built-in audits** — accessibility, color contrast, overflow detection, dark mode, Core Web Vitals, broken links, tap targets
- **143 device presets** — test on any phone, tablet, or desktop viewport without leaving your editor
- **Golden profile auth** — log in once, stay logged in across sessions
- **4 modes** — MCP server or standalone CLI, headed or headless

Works with Claude Code, Cursor, Windsurf, and anything that speaks MCP. If you only look at one repo, make it this one.

---

### [Human Engine Framework](https://github.com/zbrooklyn-claude-labs/Human-Engine-Framework)
**A quality layer between "code that runs" and "code that ships."**

AI agents are fast but sloppy. They'll write code that passes tests but looks broken on mobile. They'll fix one bug by introducing two more. They'll tell you something works without actually verifying it.

The Human Engine is a 21-category cognitive review system modeled on how experienced developers actually evaluate work — from visual correctness to security to "did you even do what was asked?" Structured as phases that agents can run before claiming they're done, so you don't have to be the one catching everything.

---

### [Less Is More for AI Autonomous Agents](https://github.com/zbrooklyn-claude-labs/Less-Is-More-for-AI-Autonomous-Agents)
**What's the minimum an AI agent actually needs to be useful?**

Not a theoretical exercise — a working Python implementation with 508 tests, backed by the research that informed every design decision.

- **Memory with teeth** — retrieval that fires when it matters, not just storage
- **Stateful daemon** — persistence across sessions without duct tape
- **Browser, vision, audio** — multimodal capabilities without bolting on five libraries
- **Multi-agent orchestration** — agents that coordinate, not just run in parallel

The research and the code live in the same repo.

---

### [AI Workspace Move Sync](https://github.com/zbrooklyn-claude-labs/ai-workspace-move-sync)
**Moved your project folder? This fixes everything that breaks.**

Claude Code, Codex CLI, and Gemini CLI all store absolute paths — to your project, your MCP configs, your conversation history. Move your folder or sync to a new machine and all of it silently breaks. No error messages, just tools that stop working and no obvious reason why.

This toolkit detects broken paths, fixes symlinks, updates configs, and gets you back to working in one command. Windows, macOS, Linux, and Termux.

---

## About

I'm [Edward](https://github.com/Zbrooklyn), a developer in Brooklyn, NY. I spend most of my time inside AI coding tools, and I build for the way this workflow actually works in practice — not how it looks in a demo.

More projects are on the way. If something here is useful, star it. If something is broken, open an issue.
