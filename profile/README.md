# Zbrooklyn Claude Labs

Tools for developers who work with AI coding agents every day and got tired of the gaps.

---

## What's Here

### [Playwright Pool](https://github.com/zbrooklyn-claude-labs/playwright-pool)
**Give your AI agent a real browser.**

Most AI coding tools are blind — they can write frontend code but can't see what it looks like. Playwright Pool fixes that. It's an MCP server that gives any AI coding tool (Claude Code, Cursor, Windsurf, anything that speaks MCP) full browser control with persistent auth.

- **75+ tools** — navigate, click, fill forms, take screenshots, run JavaScript
- **28 built-in audits** — accessibility, color contrast, overflow detection, dark mode, Core Web Vitals, broken links, tap targets, and more
- **143 device presets** — test on any phone, tablet, or desktop viewport without leaving your editor
- **Golden profile auth** — log in once, stay logged in across all browser sessions. No re-authenticating every time you open a page.
- **4 modes** — MCP server or standalone CLI, headed or headless

This is the flagship project. If you only look at one repo, make it this one.

---

### [Human Engine Framework](https://github.com/zbrooklyn-claude-labs/Human-Engine-Framework)
**A quality framework that catches what AI agents miss.**

AI agents are fast but sloppy. They'll write code that passes tests but looks broken on mobile. They'll "fix" a bug by introducing two more. They'll claim something works without actually checking.

The Human Engine is a 21-category cognitive review system modeled on how experienced developers actually evaluate work. It covers everything from visual correctness to security to "did you actually do what was asked?" — structured as phases that agents can run before claiming done.

Think of it as a senior dev review, automated.

---

### [Less Is More for AI Autonomous Agents](https://github.com/zbrooklyn-claude-labs/Less-Is-More-for-AI-Autonomous-Agents)
**A 10-component autonomous agent framework — research paper and working code.**

This started as a question: what's the minimum set of components an AI agent actually needs to be useful? Not a theoretical exercise — a working Python implementation with 508 tests.

The architecture:
- **Memory with teeth** — not just storing context, but retrieving it when it matters
- **Stateful daemon** — persistent agent that maintains state across sessions
- **Browser, vision, audio** — multimodal capabilities without bolting on five different libraries
- **Multi-agent orchestration** — agents that coordinate, not just run in parallel

The research and the code live in the same repo.

---

### [AI Workspace Move Sync](https://github.com/zbrooklyn-claude-labs/ai-workspace-move-sync)
**Moved your project folder? This fixes everything that breaks.**

Claude Code, Codex CLI, and Gemini CLI all store absolute paths — to your project, your MCP configs, your conversation history. Move your folder or sync to a new machine and everything silently breaks. No error messages, just tools that stop working.

This toolkit detects broken paths, fixes symlinks, updates configs, and gets you back to working in one command. Works across Windows, macOS, Linux, and even Termux on Android.

---

## Who's Behind This

I'm [Edward](https://github.com/Zbrooklyn) — a developer in Brooklyn, NY. I build tools for the way AI-assisted development actually works in practice, not how it works in demos.

If something here is useful to you, star it. If something is broken, open an issue.
