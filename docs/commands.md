# Antigravity CLI Reference

The Antigravity CLI (`agy`) allows you to interact with the Antigravity platform directly from your terminal. It provides commands for managing agents, workspaces, and system configuration.

## Command Syntax

The general syntax for the Antigravity CLI is:

```bash
agy <command> [options] [arguments]
```

## Essential Commands

### Authentication
Manage your session and access to AI models.

- **`agy login`**: Authenticate with your Google account. Opens a browser window for OAuth.
- **`agy logout`**: End your current session and clear local credentials.
- **`agy status`**: Check your current authentication status and model quota.

### Workspace Management
Initialize and configure your development environment.

- **`agy init`**: Initialize a new Antigravity workspace in the current directory.
- **`agy open <path>`**: Open a specific directory or project in the Antigravity editor.
- **`agy config`**: View or modify workspace-specific settings.

### Agent Operations
Spawn and control autonomous agents from the command line.

- **`agy run "<task>"`**: Spawn a new agent to execute the specified task in the current workspace.
- **`agy list`**: List all active and recently completed agent tasks.
- **`agy stop <task-id>`**: Cancel a running agent task.
- **`agy logs <task-id>`**: View the execution logs and artifacts for a specific task.

## Advanced Usage

### Model Selection
You can specify which AI model an agent should use for a specific command:

```bash
agy run "Refactor the authentication module" --model claude-4.5
```

### Autonomy Levels
Control how much permission an agent has when running commands:

- **`--autonomy high`**: Agent can run most commands without approval.
- **`--autonomy medium`**: (Default) Agent requires approval for critical commands (e.g., `rm`, `git push`).
- **`--autonomy low`**: Agent requires approval for every terminal command.

## Help and Documentation

To see a full list of available commands and global options, run:

```bash
agy --help
```

For help with a specific command:

```bash
agy <command> --help
```
