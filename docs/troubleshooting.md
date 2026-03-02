# Troubleshooting Google Antigravity

## Quick Fixes (Try These First!)

Before diving deep, try these quick solutions that resolve 80% of issues:

1. **Restart Antigravity:** Close and reopen the application completely
2. **Restart Agent:** Click "Restart Agent" in the agent panel
3. **Check Output Panel:** `View > Output > Antigravity` for error logs
4. **Use Personal Gmail:** Google Workspace accounts may have restrictions

## Most Common

### 1. Login & Authentication Issues

**Login Stuck or Infinite Loop**

- **Symptom:** Login button clicked but nothing happens, or redirects back to login
- **Solutions:**
  - Clear browser cookies for `google.com` and `antigravity.google`
  - Try using a personal Gmail account instead of Google Workspace
  - Disable browser extensions that may interfere with OAuth
  - Try a different browser (Chrome recommended)

**"Not Eligible" Error**

- **Solutions:**
  - Check if Antigravity is available in your region
  - Ensure you're using a supported Google account type
  - Try signing up for the waitlist if in early access period

## China Users

### 2. China & Restricted Regions

Google services including Antigravity are not directly accessible in mainland China. A VPN or proxy is required.

**Proxy Configuration**
- Use a reliable VPN service with US/Japan/Singapore servers
- Configure proxy settings in Antigravity: `Settings > Network > Proxy`
- Ensure your proxy supports HTTPS connections

**Region Restrictions**
Google may restrict access based on IP location. Using a VPN to connect from a supported region can help.

### 3. WSL2 Authentication

WSL2 users may experience authentication issues due to browser launch limitations in the Linux subsystem.

**Browser Launch Failed**
- Install wslu package: `sudo apt install wslu`
- Set Windows browser as default: `export BROWSER=wslview`
- Alternatively, copy the auth URL and paste in Windows browser manually

## Agent

### 4. Agent Issues

**Agent Stuck or Not Responding**
- Click "Restart Agent" button in the agent panel
- Check the Output panel for error messages
- Ensure stable internet connection
- Try simplifying your request into smaller steps

**Agent Execution Errors**
- Grant necessary file system permissions when prompted
- Check if antivirus is blocking agent processes
- Ensure Node.js is installed for JavaScript projects

> [!TIP]
> Enable detailed logging in `Settings > Advanced > Verbose Logs` for debugging

### 5. Installation & Setup

**Windows Installation Issues**
- Run installer as Administrator
- Disable Windows SmartScreen temporarily if blocked
- Ensure Windows 10 version 1903 or later

**macOS Installation Issues**
- Allow app in `System Preferences > Security & Privacy`
- For M1/M2 Macs, ensure Rosetta 2 is installed if needed
- Grant necessary permissions when prompted

**Linux Dependencies**
Install required dependencies for Debian/Ubuntu:
```bash
sudo apt update && sudo apt install libgtk-3-0 libnotify4 libnss3 libxss1
```

### 6. Chrome Extension

**Extension Not Connecting**
- Ensure Antigravity desktop app is running
- Check that extension is enabled in `chrome://extensions`
- Try removing and reinstalling the extension
- Verify Chrome is updated to the latest version

### 7. Rate Limits & Quotas

**Rate Limit Exceeded**
- Wait a few minutes before retrying
- Reduce the frequency of requests
- During public preview, limits are generous but exist
- Check your account dashboard for usage statistics

### 8. Performance Issues

**High Memory Usage**
- Close unused tabs and projects
- Reduce the number of concurrent agents
- Restart Antigravity periodically for long sessions
- Increase system swap space if available

**Slow Response Times**
- Check your internet connection speed
- Try connecting to a closer server region
- Reduce context window size for faster responses

### 9. Compatibility

**Windows Requirements**
- Windows 10 version 1903 (May 2019) or later
- Windows 11 fully supported
- 64-bit operating system required

**macOS Requirements**
- macOS 10.15 (Catalina) or later
- Apple Silicon (M1/M2/M3) and Intel supported
- 8GB RAM minimum, 16GB recommended

**Linux Requirements**
- Ubuntu 20.04 LTS or later, Debian 11 or later
- Fedora 35 or later supported
- X11 or Wayland display server

### 10. Network & Connectivity

**Connection Timeout**
- Check your internet connection
- Verify firewall isn't blocking Antigravity
- Try disabling VPN temporarily to test
- Check Google services status page for outages

## Getting More Help

**Official Resources**
- Documentation: [antigravity.google/docs](https://antigravity.google/docs)
- Community Forum: [discuss.ai.google.dev](https://discuss.ai.google.dev)
- GitHub Issues: [github.com/google/antigravity/issues](https://github.com/google/antigravity/issues)

**Before Reporting an Issue**
1. Check the Output panel for error messages
2. Note your Antigravity version (`Help > About`)
3. Try to reproduce the issue consistently
4. Search existing issues before creating a new one

> [!NOTE]
> This troubleshooting guide is community-maintained. For official support, please visit [antigravity.google](https://antigravity.google).

## Related Resources
- [Getting Started Guide](./getting-started.md)
- [Features Overview](./features.md)
- [FAQ](./faq.md)
