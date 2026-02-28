# Google Antigravity Changelog

> Curated changelog sourced from official Antigravity releases and announcements.
> Last updated: 2026-02-28

## February 2026

### IDE Updates
- **Multi-model support expanded**: Added model switching per-task with Gemini 3 Pro, Gemini 3 Flash, Claude Sonnet 4.5, and GPT-OSS-120B
- **Agent Manager improvements**: Real-time progress tracking, artifact streaming, and intervention controls (pause/resume/cancel/redirect)
- **Browser subagent enhancements**: Session recording as `.webp` video, improved screenshot capture, DOM inspection capabilities
- **Task grouping**: Group related tasks for complex multi-step projects
- **Skills system**: Open-format `.agents/skills/` directory with `SKILL.md` instruction files
- **Rules & workflows**: Define project-specific constraints in `.agents/rules.md` and workflows in `.agents/workflows/`

### Jules Integration
- **Automated PR generation**: Jules can create pull requests from task descriptions
- **Weekly documentation updates**: Scheduled tasks for keeping docs current
- **API key management**: Personal API keys for programmatic Jules access

### Platform
- **Windows support**: Full Windows 10/11 64-bit compatibility
- **Linux improvements**: Better glibc compatibility, reduced system requirements
- **OAuth enhancements**: Smoother Chrome-based Google OAuth flow with protocol handler

## January 2026

### IDE Updates  
- **Initial public preview launch** for Windows, macOS, and Linux
- **Agent-first architecture**: Autonomous agents that plan, execute, test, and deliver
- **Three development modes**: Agent-Driven (Autopilot), Review-Driven, Agent-Assisted
- **MCP integration**: Connect to BigQuery, Cloud SQL, Cloud Storage, and custom APIs via Model Context Protocol
- **Chrome browser extension**: Automated UI testing, screenshot capture, visual regression detection

### Supported Models at Launch
| Model | Provider | Best For |
|---|---|---|
| Gemini 3 Pro | Google | General coding (balanced) |
| Gemini 3 Flash | Google | Fast iteration |
| Claude Sonnet 4.5 | Anthropic | Complex reasoning |
| GPT-OSS-120B | OpenAI | Creative solutions |

---

*See [official announcements](https://antigravity.google) for the full release history.*
