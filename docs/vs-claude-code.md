# Antigravity vs Claude Code — Comparison

## Overview

| Aspect | Google Antigravity | Claude Code |
|---|---|---|
| **Paradigm** | Agent-first IDE | CLI-based coding agent |
| **Interface** | GUI (desktop IDE) | Terminal (CLI) |
| **AI Model** | Multi-model (Gemini 3, Claude, GPT) | Claude only |
| **Primary Mode** | Visual + autonomous | Conversational CLI |
| **Pricing** | Free (Gemini tier) | Anthropic API credits |

## Architecture

### Antigravity — Desktop IDE
A full visual IDE with Agent Manager, editor view, integrated terminal, and browser subagent. Agents produce artifacts (screenshots, recordings, plans) for transparent verification.

### Claude Code — CLI Agent
A terminal-based agent that reads your codebase, proposes changes, and executes commands. Runs in your existing terminal alongside any editor.

## Feature Comparison

| Feature | Antigravity | Claude Code |
|---|---|---|
| Visual IDE | ✅ | ❌ (CLI only) |
| Terminal integration | ✅ | ✅ (native) |
| Multi-file editing | ✅ | ✅ |
| Autonomous execution | ✅ Agent Manager | ✅ (with permissions) |
| Browser testing | ✅ Browser subagent | ❌ |
| Multi-model | ✅ Gemini, Claude, GPT | ❌ Claude only |
| Artifacts (screenshots) | ✅ | ❌ |
| MCP integration | ✅ (Google Cloud) | ✅ (general) |
| Headless/CI mode | ⚠️ Via Jules | ✅ Native |
| Extended thinking | ❌ | ✅ |
| Git integration | ✅ | ✅ |
| Skills/rules | ✅ Skills | ✅ CLAUDE.md |
| Free tier | ✅ | ❌ (API costs) |

## Complementary Use

Many developers use both tools together:

- **Antigravity** for visual tasks: UI development, browser testing, screenshot verification
- **Claude Code** for deep terminal tasks: complex refactors, debugging, CI pipelines

## When to Choose

### Choose Antigravity if:
- You want a **visual IDE** with agent capabilities
- You need **browser-based** UI testing and verification
- You want **multi-model** flexibility
- You prefer **artifact-based** transparency
- You want a **free tier** with generous limits

### Choose Claude Code if:
- You prefer working in the **terminal**
- You want **deep reasoning** with extended thinking
- You need **headless/CI** automation
- You're already on the **Anthropic** platform
- You want **maximum control** over agent permissions

## See Also

- [Features](./features.md) — Antigravity feature details
- [Getting Started](./getting-started.md) — Try Antigravity yourself
