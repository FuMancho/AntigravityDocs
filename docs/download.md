# Download and Install Google Antigravity

Google Antigravity is the premier agent-first AI development platform, designed to help you orchestrate complex tasks across your editor, terminal, and browser. It is currently available in public preview for individual developers at no cost.

## Official Download Links

Always ensure you are downloading Antigravity from official Google sources:

| Platform | Download Link | Supported Architecture |
|---|---|---|
| **Windows** | [Download for Windows](https://antigravity.google/download) | x64, ARM64 |
| **macOS** | [Download for macOS](https://antigravity.google/download) | Intel, Apple Silicon |
| **Linux** | [Download for Linux](https://antigravity.google/download) | .deb, .rpm |

## System Requirements

Before installing, ensure your workstation meets the following minimum specifications:

### Hardware Requirements
- **Processor:** 1.6 GHz or faster (multicore recommended)
- **RAM:** 4GB minimum (8GB+ recommended for multi-agent workflows)
- **Disk Space:** 500MB for application, additional space for agent knowledge bases
- **Network:** Stable internet connection required for AI model access

### Operating Systems
- **Windows:** Windows 10 or later
- **macOS:** macOS 10.15 (Catalina) or later
- **Linux:** Ubuntu 20.04+, Debian 11+, Fedora 36+, or OpenSUSE 15+

## Installation Instructions

### Windows Installation
1. Download the `.exe` installer from the [official site](https://antigravity.google/download).
2. Locate the downloaded file (typically in your `Downloads` folder) and double-click to run.
3. Follow the installation wizard. The default path is `%LocalAppData%\Programs\Google\Antigravity`.
4. Once complete, launch Antigravity from the Start Menu or desktop shortcut.

### macOS Installation
1. Download the `.dmg` disk image.
2. Open the `.dmg` file and drag the **Antigravity** icon into your **Applications** folder.
3. Launch the application from your Applications folder or via Spotlight (`Cmd + Space`).
4. On first launch, you may need to confirm opening a downloaded application in System Settings.

### Linux Installation
For Debian-based distributions (Ubuntu, Mint):
```bash
sudo dpkg -i antigravity_amd64.deb
sudo apt-get install -f # Install dependencies if needed
```

For RPM-based distributions (Fedora, RHEL):
```bash
sudo rpm -i antigravity_x86_64.rpm
```

## Post-Installation Setup

### 1. Authentication
Upon first launch, you will be prompted to sign in with a personal Google (Gmail) account. This is required to access the Gemini 3 Pro model and other agentic features during the public preview.

### 2. Browser Integration
To enable full agent capabilities (including web testing and navigation), install the [Antigravity Browser Extension](https://antigravity.google/download) when prompted.

### 3. CLI Access
To use Antigravity from your terminal, ensure the `agy` command is added to your PATH during installation, or follow the guide in [CLI Reference](./commands.md).
