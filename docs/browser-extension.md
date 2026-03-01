# Browser Extension

Enable agents to interact directly with web applications.

## Overview

The Antigravity Browser Extension extends agent capabilities beyond the IDE, allowing them to directly interact with, test, and verify web applications in Chrome. This creates a seamless development workflow where agents can write code, launch it, and validate functionality in the browser.

The extension is optional but highly recommended for web development tasks, enabling automated UI testing, visual regression detection, and interactive debugging.

## Installation

### 1. Launch Antigravity
Open Antigravity IDE and start a conversation in the Playground

### 2. Setup Prompt
Click the "Setup" button when prompted to install the browser extension

### 3. Chrome Web Store
You'll be directed to the Chrome Web Store. Click "Add to Chrome" and grant permissions

### 4. Verify Connection
Return to Antigravity and confirm the extension is connected (green indicator in status bar)

## Key Features

### Automated UI Testing
Agents can navigate web pages, click buttons, fill forms, and verify expected behavior. Perfect for end-to-end testing and validation workflows.

### Screenshot Capture
Agents automatically capture screenshots at key points during testing. These become artifacts you can review to verify visual correctness.

### Session Recording
Record entire browser sessions showing agent interactions. Great for debugging and understanding complex workflows.

### DOM Inspection
Agents can read and analyze the DOM structure, extract data, and verify element presence and properties.

### Visual Regression
Detect unintended visual changes by comparing screenshots across code changes. Catch CSS bugs and layout issues automatically.

## Common Use Cases

- **🎨 UI Component Development:** Agents build components, launch them in the browser, and verify they render correctly across different states and breakpoints.
- **🔐 Form Validation:** Test form submissions, validation logic, error messages, and success states automatically by having agents fill and submit forms.
- **🚦 E2E Testing:** Create comprehensive end-to-end test flows that simulate real user journeys through your application.
- **🐛 Bug Reproduction:** Agents can reproduce reported bugs by following specific steps in the browser and capturing evidence.

## Permissions & Security

The extension requires the following permissions:
- **Active Tab:** Read and modify content on active tab
- **Screenshots:** Capture visible tab for artifacts
- **Native Messaging:** Communicate with Antigravity IDE

> [!NOTE]
> **Privacy Note:** The extension only operates when explicitly commanded by you or an agent you've authorized. All data stays local and is never sent to external servers.

## Troubleshooting

### Extension not connecting
- Ensure Antigravity IDE is running
- Restart Chrome after installation
- Check that extension is enabled in `chrome://extensions`
- Verify firewall isn't blocking localhost connections

### Screenshots not capturing
- Grant screenshot permission when prompted
- Ensure tab is visible (not minimized)
- Check available disk space

### Agent can't interact with page
- Refresh the page after installing extension
- Some sites may block automation - check console for errors
- Verify extension has permissions for the site
