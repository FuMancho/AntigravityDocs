# Browser Extension

## Overview

Google Antigravity includes a Chrome browser extension that gives AI agents direct access to web pages. This enables automated UI testing, screenshot capture, session recording, and visual regression detection — all driven by agents without manual intervention.

## Installation

1. **Launch Antigravity** — The extension installs automatically on first launch
2. **Setup Prompt** — Accept the extension installation when prompted
3. **Chrome Web Store** — Alternatively, install manually from the [Chrome Web Store](https://chromewebstore.google.com)
4. **Verify Connection** — The extension icon turns green when connected to Antigravity

> [!NOTE]
> The extension requires Chrome or a Chromium-based browser. It connects to Antigravity via a local WebSocket on port 9222.

## Key Features

### Automated UI Testing

Agents can navigate web pages, click buttons, fill forms, and verify expected behavior. This enables true end-to-end testing workflows without manual browser interaction.

```
Example: "Test the login form with valid and invalid credentials"
→ Agent fills email/password, submits, verifies redirect or error message
```

### Screenshot Capture

Agents automatically capture screenshots at key points during testing. These become **artifacts** you can review to verify visual correctness without watching the agent work.

Screenshots are saved as `.png` or `.webp` files and can be embedded in walkthroughs and implementation plans.

### Session Recording

Record entire browser sessions showing agent interactions as `.webp` video files. Useful for:

- Debugging complex multi-step workflows
- Documenting user flows
- Sharing reproductions of bugs

### DOM Inspection

Agents can read and analyze the DOM structure, including:

- Element presence and visibility
- Text content extraction
- CSS property inspection
- Form field states
- Accessibility attributes

### Visual Regression

Detect unintended visual changes by comparing screenshots across code changes. This catches:

- CSS bugs and layout shifts
- Missing or broken images
- Typography changes
- Responsive design regressions

## Common Use Cases

### 🎨 UI Component Development

Build and verify components visually. The agent creates the component, launches it in the browser, captures a screenshot, and iterates based on your feedback.

### 🔐 Form Validation

Test all validation paths: required fields, format errors, success states, and edge cases — all automated through the browser extension.

### 🚦 End-to-End Testing

Run full user flows from login to checkout. The agent navigates through the entire application, verifying each step produces the expected outcome.

### 🐛 Bug Reproduction

Describe a bug, and the agent reproduces it in the browser, capturing screenshots and session recordings as evidence for debugging.

## Permissions & Security

The extension requests the following Chrome permissions:

| Permission | Reason |
|---|---|
| `activeTab` | Interact with the current page |
| `debugger` | DOM inspection and JavaScript execution |
| `tabs` | Navigate between pages |
| `storage` | Save extension settings |

> [!IMPORTANT]
> The extension only communicates with the local Antigravity instance. No data is sent to external servers.

## Troubleshooting

### Extension not connecting
- Verify Antigravity is running
- Check that port 9222 is not blocked by a firewall
- Restart Chrome and Antigravity

### Screenshots not capturing
- Ensure the target page is fully loaded
- Check that the extension has the required Chrome permissions
- Try disabling other extensions that might conflict

### Agent can't interact with page
- Some pages block automated interaction (banking, captchas)
- Cross-origin iframes may require additional configuration
- Try running Chrome with `--disable-web-security` for local testing only

## See Also

- [Features](./features.md) — Core platform capabilities
- [Agents](./agents.md) — Agent capabilities and advanced techniques
- [Troubleshooting](./troubleshooting.md) — General troubleshooting
