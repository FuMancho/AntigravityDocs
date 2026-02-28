# Antigravity vs Cursor — Comparison

## Overview

| Aspect | Google Antigravity | Cursor |
|---|---|---|
| **Paradigm** | Agent-first (delegates entire tasks) | AI-assisted (enhances your editing) |
| **Base** | Custom IDE (VS Code-based) | Fork of VS Code |
| **AI Model** | Multi-model (Gemini 3, Claude, GPT) | Claude, GPT, custom |
| **Primary Mode** | Autonomous agents | Tab completions + chat |
| **Pricing** | Free (Gemini 3 Pro tier) | Free tier + Pro ($20/mo) |

## Architecture

### Antigravity — Agent-First
You describe what you want, and autonomous agents plan, implement, test, and deliver. Agents operate across editor, terminal, and browser.

```
User → "Build a login page with JWT auth"
Agent → Plans → Codes → Tests → Delivers artifacts
```

### Cursor — Edit-First
You write code with AI assistance. Tab completions, inline chat, and Composer help you code faster, but you remain the driver.

```
User → writes code → gets suggestions → accepts/rejects
```

## Feature Comparison

| Feature | Antigravity | Cursor |
|---|---|---|
| Tab completions | ✅ | ✅ |
| Inline chat | ✅ | ✅ |
| Multi-file editing | ✅ (agent-driven) | ✅ (Composer) |
| Autonomous execution | ✅ Agent Manager | ❌ |
| Terminal access (agent) | ✅ | ⚠️ Limited |
| Browser testing | ✅ Browser subagent | ❌ |
| Screenshot artifacts | ✅ | ❌ |
| Session recording | ✅ | ❌ |
| Multi-model switching | ✅ Per-task | ✅ Per-chat |
| Knowledge base | ✅ Persistent learning | ❌ |
| Skills/extensions | ✅ Open format | ⚠️ Rules files |
| Free tier | ✅ Generous | ✅ Limited |

## When to Choose

### Choose Antigravity if:
- You want to **delegate** entire tasks to AI
- You need **browser-based testing** and validation
- You want **multi-agent** parallel execution
- You prefer **artifact-based** verification
- You use Google Cloud services (MCP integration)

### Choose Cursor if:
- You prefer **hands-on** coding with AI assistance
- You want the **fastest** tab completions
- You need **VS Code extension** compatibility
- You're already invested in the VS Code ecosystem

## See Also

- [Features](./features.md) — Antigravity feature details
- [Getting Started](./getting-started.md) — Try Antigravity yourself
