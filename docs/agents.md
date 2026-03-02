# AI Agents in Google Antigravity

Master the power of autonomous AI agents in Antigravity.

## What are Agents?

Agents in Antigravity are autonomous AI assistants that can plan, execute, and verify complex development tasks across your editor, terminal, and browser. Unlike traditional code completion tools, agents can work independently on entire features while you focus on higher-level tasks.

Each agent operates with configurable levels of autonomy, generating verifiable artifacts that help you build trust in their work.

## How Agents Work

### 1. Task Understanding
When you assign a task, the agent analyzes the request, examines your codebase context, and creates a detailed execution plan broken into manageable steps.

### 2. Autonomous Execution
The agent executes the plan by writing code, running commands, testing in the browser, and making adjustments based on results - all while generating artifacts for verification.

### 3. Verification & Learning
After completing tasks, agents verify their work through testing and visual inspection. They save useful patterns and context to a knowledge base for future reference.

## Best Practices

**✅ Start with Clear Task Descriptions**
- Good: "Create a React component for user authentication with email/password, include form validation, and add unit tests"
- Avoid: "Make a login thing"

**✅ Break Down Complex Tasks**
For large features, decompose them into smaller, focused tasks. Agents perform best when working on well-scoped objectives.

**✅ Review Artifacts Regularly**
Check generated task lists, plans, and test results. Artifacts help you catch issues early and provide feedback to improve agent performance.

**✅ Configure Appropriate Autonomy**
For critical operations or unfamiliar codebases, require approval before terminal commands. Increase autonomy as you build confidence.

## Using the Agent Manager

The Agent Manager is your mission control for orchestrating multiple agents across workspaces.

### Spawning Agents
Click "New Agent" and assign it to a specific workspace or task. You can run multiple agents in parallel for different features.

### Monitoring Progress
Track real-time progress, view generated artifacts, and see which files agents are modifying. Hover over agents to see detailed status.

### Intervention Controls
Pause agents, provide additional context, or manually approve pending actions. You maintain full control throughout execution.

## Advanced Techniques

### 🔄 Agent Chaining
Have one agent create scaffolding, another implement logic, and a third write tests. Chain their outputs for complex workflows.

### 📚 Knowledge Base
Manually save code patterns, architecture decisions, or common solutions to your agent's knowledge base for consistent application.

### 🎯 Model Selection
Use Gemini 3 Pro for general tasks, Claude Sonnet for complex reasoning, and GPT-4 for creative solutions. Match models to task types.

### 🔍 Iterative Refinement
After reviewing agent output, provide specific feedback and have the agent iterate. This builds better patterns over time.

## Common Use Cases

- **Feature Development:** Build complete features from specification to tests
- **Refactoring:** Modernize codebases, apply patterns, update dependencies
- **Test Generation:** Create comprehensive unit, integration, and E2E tests
- **Documentation:** Generate API docs, README files, and code comments
- **Bug Fixing:** Investigate issues, identify root causes, implement fixes
