# Authentication & OAuth

## Google OAuth Integration

Google Antigravity uses standard OAuth 2.0 with your Google account. Because Antigravity is a Google-native agentic IDE, authentication integrates directly with your browser.

### Setup Flow

1. Launch Antigravity IDE
2. When prompted, click the Chrome icon to open a Google sign-in session
3. Sign in with your Google account
4. Antigravity syncs your profile, extensions, and credentials

> [!TIP]
> Set Chrome as your default browser for the smoothest OAuth handshake. The `antigravity://` protocol handler works best with Chrome.

### OAuth Callback

Antigravity uses a local callback listener for authentication:

```
http://localhost:36742/oauth-callback
```

This receives the token from Chrome after you click "Approve" in the Google sign-in flow.

## Third-Party Tool Authentication

Developers can use Antigravity's OAuth session to power CLI tools like **OpenCode** or **Clawdbot**, allowing access to Antigravity model quotas (including Gemini 3 and Claude 4.5) from the terminal.

### Available Auth Plugins

| Plugin | Purpose |
|---|---|
| [opencode-antigravity-auth](https://github.com/opencode-antigravity-auth) | Enables `opencode auth login` with "OAuth with Google (Antigravity)" provider |
| [opencode-google-antigravity-auth](https://www.npmjs.com/package/opencode-google-antigravity-auth) | NPM package implementing the local callback listener |

### Usage

```bash
opencode auth login
# Select "OAuth with Google (Antigravity)"
# Chrome opens for verification
# Token received at localhost:36742/oauth-callback
```

## MCP Integration

Antigravity's Model Context Protocol (MCP) uses your authenticated Google identity to securely connect to services like:
- BigQuery
- Cloud SQL
- Other Google Cloud services

No additional passwords or re-authentication required once the initial OAuth flow completes.

## Troubleshooting

### Windows OAuth Redirect Issues

If Chrome OAuth succeeds but Antigravity fails to receive the token:

1. Ensure Chrome is set as your default browser
2. Verify the `antigravity://` protocol handler is registered
3. Check that no firewall is blocking `localhost:36742`
4. Try running Antigravity as administrator if the protocol handler fails

### Browser-Specific OAuth Bugs

> [!NOTE]
> If authenticated successfully but stuck on redirect, try clearing the Antigravity auth cache:
> - Windows: `%APPDATA%\google-antigravity\auth\`
> - macOS: `~/Library/Application Support/google-antigravity/auth/`
> - Linux: `~/.config/google-antigravity/auth/`

### Resources

- [Google AI Developers Forum — OAuth Issues](https://discuss.ai.google.dev)
- [Community Troubleshooting](https://antigravity.im/troubleshooting)
