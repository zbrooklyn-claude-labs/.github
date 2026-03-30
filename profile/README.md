<div align="center">

# Zbrooklyn Claude Labs

**Open-source infrastructure for AI-assisted development**

We build the missing pieces — the tools you reach for when your AI coding agent
hits a wall it shouldn't have hit.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/zbrooklyn-claude-labs/.github/blob/main/profile/README.md#contributing)
[![MCP Compatible](https://img.shields.io/badge/MCP-compatible-purple.svg)](https://modelcontextprotocol.io)

[Browse Projects](#projects) · [Who This Is For](#who-this-is-for) · [Get Started](#quickstart) · [Contribute](#contributing) · [Roadmap](#whats-coming)

</div>

---

## The Problem

AI coding tools are fast, but they have blind spots. They write frontend code they can't see. They claim things work without checking. They lose context when you move a folder. They review their own work and call it done.

Every project here came from a real workflow problem — something that broke, something that was missing, something that should have existed already. If you work with AI coding agents daily, you'll recognize a few of them.

---

## Who This Is For

- **Developers using AI coding agents** (Claude Code, Cursor, Windsurf, Copilot) who want their tools to actually see and verify what they build
- **Teams building AI agent pipelines** who need quality gates between "code generated" and "code shipped"
- **Anyone tired of re-explaining context** to their AI tools after moving a folder, switching machines, or losing a session

If you've ever watched an AI agent confidently tell you something works when it clearly doesn't — these tools are for you.

---

## Projects

### [Playwright Pool](https://github.com/zbrooklyn-claude-labs/playwright-pool)

[![GitHub stars](https://img.shields.io/github/stars/zbrooklyn-claude-labs/playwright-pool?style=social)](https://github.com/zbrooklyn-claude-labs/playwright-pool)
[![npm version](https://img.shields.io/npm/v/playwright-pool)](https://www.npmjs.com/package/playwright-pool)

**Give your AI agent a real browser.**

Most AI coding tools are blind — they can write frontend code but never see what it actually looks like. Playwright Pool is an MCP server that gives any AI coding tool full browser control with persistent authentication.

- **75+ tools** — navigate, click, fill forms, screenshot, run JavaScript
- **28 built-in audits** — accessibility, color contrast, overflow detection, dark mode, Core Web Vitals, broken links, tap targets
- **143 device presets** — test on any phone, tablet, or desktop viewport without leaving your editor
- **Golden profile auth** — log in once, stay logged in across sessions
- **4 modes** — MCP server or standalone CLI, headed or headless

Works with Claude Code, Cursor, Windsurf, and anything that speaks MCP.

**Why not just use Playwright directly?** You could — but you'd need to wire up MCP bindings, build audit logic, manage browser lifecycle, handle auth persistence, and maintain device presets yourself. Playwright Pool packages all of that into one install.

<details>
<summary><strong>Quickstart</strong></summary>

```bash
npm install -g playwright-pool

# Run as MCP server (add to your claude_desktop_config.json or .mcp.json)
playwright-pool serve

# Or use the CLI directly
playwright-pool open https://example.com
playwright-pool audit accessibility https://example.com
playwright-pool screenshot https://example.com --device "iPhone 15"
```

</details>

---

### [Human Engine Framework](https://github.com/zbrooklyn-claude-labs/Human-Engine-Framework)

[![GitHub stars](https://img.shields.io/github/stars/zbrooklyn-claude-labs/Human-Engine-Framework?style=social)](https://github.com/zbrooklyn-claude-labs/Human-Engine-Framework)

**A quality layer between "code that runs" and "code that ships."**

AI agents are fast but sloppy. They'll write code that passes tests but looks broken on mobile. They'll fix one bug by introducing two more. They'll tell you something works without actually verifying it.

The Human Engine is a 21-category cognitive review system modeled on how experienced developers actually evaluate work — from visual correctness to security to "did you even do what was asked?" Structured as phases that agents can run before claiming they're done, so you don't have to be the one catching everything.

**Why not just use a linter?** Linters catch syntax and style. The Human Engine catches the stuff linters miss — visual regressions, logic that doesn't match the spec, missing edge cases, security holes that pass CI, and the classic "it works on my machine" problems. It's the review a senior dev would do, not a style check.

<details>
<summary><strong>The 21 Categories</strong></summary>

The framework evaluates across 10 phases covering:

1. Request comprehension
2. Scope accuracy
3. Visual correctness
4. Responsive behavior
5. Accessibility compliance
6. Security review
7. Performance impact
8. Error handling
9. Edge case coverage
10. Documentation accuracy
11. Test coverage
12. Code quality
13. API contract compliance
14. State management
15. Data integrity
16. Cross-browser compatibility
17. Deployment readiness
18. Monitoring and observability
19. Backwards compatibility
20. User experience flow
21. Adversarial robustness

Full documentation in the [repo](https://github.com/zbrooklyn-claude-labs/Human-Engine-Framework).

</details>

---

### [Less Is More for AI Autonomous Agents](https://github.com/zbrooklyn-claude-labs/Less-Is-More-for-AI-Autonomous-Agents)

[![GitHub stars](https://img.shields.io/github/stars/zbrooklyn-claude-labs/Less-Is-More-for-AI-Autonomous-Agents?style=social)](https://github.com/zbrooklyn-claude-labs/Less-Is-More-for-AI-Autonomous-Agents)
[![Tests](https://img.shields.io/badge/tests-508%20passing-brightgreen)]()

**What's the minimum an AI agent actually needs to be useful?**

Not a theoretical exercise — a working Python implementation with 508 tests, backed by the research that informed every design decision.

- **Memory with teeth** — retrieval that fires when it matters, not just storage
- **Stateful daemon** — persistence across sessions without duct tape
- **Browser, vision, audio** — multimodal capabilities without bolting on five libraries
- **Multi-agent orchestration** — agents that coordinate, not just run in parallel

**Why not use LangChain / CrewAI / AutoGen?** Those frameworks optimize for flexibility and plugin ecosystems. This one optimizes for the smallest set of components that actually work in production. Ten components, no plugin system, no YAML configs, no "framework within a framework." The research and the code live in the same repo so you can see exactly why each decision was made.

<details>
<summary><strong>Quickstart</strong></summary>

```bash
git clone https://github.com/zbrooklyn-claude-labs/Less-Is-More-for-AI-Autonomous-Agents.git
cd Less-Is-More-for-AI-Autonomous-Agents
pip install -r requirements.txt
python -m pytest  # 508 tests
```

</details>

---

### [AI Workspace Move Sync](https://github.com/zbrooklyn-claude-labs/ai-workspace-move-sync)

[![GitHub stars](https://img.shields.io/github/stars/zbrooklyn-claude-labs/ai-workspace-move-sync?style=social)](https://github.com/zbrooklyn-claude-labs/ai-workspace-move-sync)

**Moved your project folder? This fixes everything that breaks.**

Claude Code, Codex CLI, and Gemini CLI all store absolute paths — to your project, your MCP configs, your conversation history. Move your folder or sync to a new machine and all of it silently breaks. No error messages, just tools that stop working and no obvious reason why.

This toolkit detects broken paths, fixes symlinks, updates configs, and gets you back to working in one command. Windows, macOS, Linux, and Termux.

**Why not just fix paths manually?** You could, if you knew where they all were. Claude Code alone scatters state across `~/.claude/`, project-level `.claude/` directories, MCP configs, and conversation metadata. Multiply that by three tools and two machines and you're spelunking through hidden directories for an hour. This does it in seconds.

<details>
<summary><strong>Quickstart</strong></summary>

```bash
git clone https://github.com/zbrooklyn-claude-labs/ai-workspace-move-sync.git
cd ai-workspace-move-sync

# Scan for broken paths
python sync.py scan

# Fix everything
python sync.py fix
```

</details>

---

## Quickstart

Pick the project that matches your problem:

| Problem | Solution | Install |
|---------|----------|---------|
| My AI agent can't see the UI it builds | [Playwright Pool](https://github.com/zbrooklyn-claude-labs/playwright-pool) | `npm i -g playwright-pool` |
| AI-generated code ships with obvious bugs | [Human Engine](https://github.com/zbrooklyn-claude-labs/Human-Engine-Framework) | Clone repo, add to agent workflow |
| I want to build autonomous agents from scratch | [Less Is More](https://github.com/zbrooklyn-claude-labs/Less-Is-More-for-AI-Autonomous-Agents) | `pip install -r requirements.txt` |
| I moved my project and everything broke | [Workspace Sync](https://github.com/zbrooklyn-claude-labs/ai-workspace-move-sync) | `python sync.py fix` |

---

## What's Coming

This org is actively growing. Here's what's in the pipeline:

- **More MCP tools** — extending the Playwright Pool model to other domains where AI agents need real-world access
- **Agent evaluation benchmarks** — standardized ways to measure whether an AI coding agent actually did what you asked
- **Workflow templates** — pre-built configurations for common Claude Code / Cursor / Windsurf setups
- **Documentation and guides** — deeper writeups on the problems these tools solve and the design decisions behind them

Want to influence what gets built next? [Open a discussion](https://github.com/orgs/zbrooklyn-claude-labs/discussions) or file an issue on the relevant repo.

---

## Contributing

Contributions are welcome across all repos. Here's how to get started:

1. **Pick a repo** — each one has its own issues and contribution needs
2. **Check open issues** — look for `good first issue` or `help wanted` labels
3. **Fork and branch** — standard GitHub flow. One feature per PR.
4. **Test your changes** — each project has its own test suite. Make sure it passes before opening a PR.
5. **Open a PR** — describe what you changed and why. Link to the issue if there is one.

No CLA, no contributor agreement, no hoops. Just good code and clear communication.

All projects are licensed under the **MIT License** — use them however you want.

---

## About

I'm [Edward](https://github.com/Zbrooklyn), a developer in Brooklyn, NY. I spend most of my time inside AI coding tools, building for the way this workflow actually works in practice — not how it looks in a demo.

If something here is useful, star it. If something is broken, open an issue. If you want to talk about any of it, [start a discussion](https://github.com/orgs/zbrooklyn-claude-labs/discussions).
