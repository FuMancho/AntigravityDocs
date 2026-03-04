# Getting Started with Google Antigravity

## Quick Start

Follow these simple steps to install and configure Antigravity on your system.

### 1. System Requirements

Before installing, make sure your system meets these requirements:

**Windows**
- Windows 10 or later
- 4GB RAM minimum
- 500MB disk space

**macOS**
- macOS 10.15+
- 4GB RAM minimum
- 500MB disk space

**Linux**
- Ubuntu 20.04+ or equivalent
- 4GB RAM minimum
- 500MB disk space

### 2. Download Antigravity

Visit the official download page and select your operating system:
[https://antigravity.google/download](https://antigravity.google/download)

- **Windows:** Download the `.exe` installer (x64 or ARM64)
- **macOS:** Download the `.dmg` file
- **Linux:** Download the `.deb` or `.rpm` package

### 3. Install the Application

**Windows Installation**
1. Double-click the downloaded `.exe` file
2. Follow the installation wizard (takes 3-5 minutes)
3. Default installation path: `C:\Program Files\Google\Antigravity`
4. Launch Antigravity from Start Menu

**macOS Installation**
1. Open the downloaded `.dmg` file
2. Drag Antigravity to Applications folder
3. Open from Applications (allow in Security settings if needed)

**Linux Installation**
```bash
# Debian/Ubuntu
sudo dpkg -i antigravity_*.deb

# Fedora/RHEL
sudo rpm -i antigravity_*.rpm
```

### 4. Initial Setup

When you first launch Antigravity:

1. **Choose setup flow:**
   - Import settings from VS Code or Cursor
   - Start with a fresh configuration
2. **Select theme:** Choose between Light, Dark, or High Contrast themes
3. **Sign in:** Use your personal Gmail account (required for public preview)
4. **Configure AI model:** Select your preferred default model (Gemini 3 Pro recommended)

### 5. Install Browser Extension

To enable agent browser integration:

1. Start a conversation in the Antigravity Playground
2. Click "Setup" when prompted for browser extension
3. Follow the link to Chrome Web Store
4. Click "Add to Chrome" to install the extension
5. Grant necessary permissions for agent control

> [!TIP]
> The browser extension is optional but highly recommended for web development tasks.

### 6. Deploy Your First Agent

Try these starter tasks:

- **Simple Task:** "Create a hello world React component with TypeScript"
- **Complex Task:** "Build a todo app with React, add styling with Tailwind, and create unit tests"

## Next Steps

- [Learn About Agents](./agents.md) — Master agent orchestration and best practices
- [Browser Extension Guide](./browser-extension.md) — Deep dive into browser integration capabilities

## Common Issues

**Installation fails on Windows**
Run the installer as Administrator and temporarily disable antivirus software.

**Cannot sign in with Gmail**
Antigravity public preview requires a personal Gmail account. Workspace accounts are not supported yet.

**Browser extension not working**
Make sure you've granted all required permissions and restarted Chrome after installation.

Need more help? Check out our [FAQ page](./faq.md).
