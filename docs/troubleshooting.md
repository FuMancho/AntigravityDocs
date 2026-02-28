# Troubleshooting Google Antigravity

## Common Issues

### Installation Problems

**Issue:** Installer fails on Linux

> [!TIP]
> Verify your system meets the requirements: glibc >= 2.28, glibcxx >= 3.4.25.

```bash
ldd --version
strings /usr/lib/x86_64-linux-gnu/libstdc++.so.6 | grep GLIBCXX
```

### Authentication Issues

**Issue:** Unable to link Google account

- Ensure you're using a personal Gmail account
- Check that Chrome is available as the default browser
- Try clearing browser cookies and retrying

### Agent Not Responding

**Issue:** Agent appears stuck or unresponsive

1. Try pausing and resuming the agent
2. Cancel the task and start a new one with a clearer description
3. Check the activity feed for error messages
4. Verify your internet connection

### Model Errors

**Issue:** "Model unavailable" or rate limit errors

- Switch to a different supported model
- Wait a few minutes and try again
- Check [Antigravity status](https://antigravity.google) for outages

## See Also

- [Getting Started](./getting-started.md) — Installation guide
- [Features](./features.md) — Feature overview
