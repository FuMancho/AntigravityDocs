# Frequently Asked Questions

Find answers to common questions about Google Antigravity.

## General

### What is Google Antigravity?
Google Antigravity is an agentic development platform announced in November 2025 that combines a familiar, AI-powered coding experience with a new agent-first interface. It allows developers to deploy autonomous agents that can plan, execute, and verify complex tasks across the editor, terminal, and browser.

### Is Antigravity free to use?
Yes! Antigravity is currently available in public preview at no cost for individuals with personal Gmail accounts. It comes with generous rate limits on Gemini 3 Pro and full support for other AI models like Claude Sonnet and GPT-4.

### What operating systems are supported?
Antigravity supports Windows 10/11, macOS 10.15+ (Intel and Apple Silicon), and Ubuntu 20.04+ (and equivalent Linux distributions).

### Do I need a Google Workspace account?
During the public preview, Antigravity requires a personal Gmail account. Support for Google Workspace accounts is currently in development and will be released in a future update.

## Agents & Features

### How autonomous are the agents?
Agents operate at configurable levels of autonomy. You can allow them to run commands and edit files automatically, or require your approval for every action. This dual approach ensures you always have the right balance of automation and control.

### Can agents access my local files?
Yes, agents can read and write files within the workspace you open in Antigravity. They cannot access files outside of the open workspace unless explicitly granted permission.

### What is the Browser Extension for?
The Chrome browser extension allows agents to directly interact with web applications. They can click buttons, fill forms, take screenshots, and verify UI changes automatically. It is optional but highly recommended for web developers.

## Privacy & Security

### Is my code used to train AI models?
No. Google does not use your private code, workspace data, or agent interactions to train our foundation models. See our [Privacy Policy](./privacy.md) for complete details.

### How is my data protected?
All local code remains on your machine. When communicating with AI models, data is encrypted in transit and only the context necessary to complete your specific request is sent to the API.

## Troubleshooting

### My agent is stuck or looping. What should I do?
First, try clicking the "Restart Agent" button. If that doesn't work, cancel the current task and try breaking it down into smaller, more specific steps.

### I'm getting a "Rate Limit Exceeded" error.
During the preview period, we enforce generous but necessary rate limits to ensure fair usage. Please wait a few minutes and try again.
