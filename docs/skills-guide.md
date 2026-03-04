# Skills Guide

## What are Skills?

Skills are lightweight, open-format extensions that let you customize AI agent behaviors in Antigravity. They codify team best practices, specialized workflows, and domain-specific knowledge into reusable packages that agents can follow.

## Skill Structure

A skill is a directory containing a `SKILL.md` file and optional supporting resources:

```
.agents/skills/<skill-name>/
├── SKILL.md          # Required — Main instruction file
├── scripts/          # Optional — Helper scripts
├── templates/        # Optional — File templates
├── examples/         # Optional — Reference implementations
└── resources/        # Optional — Additional assets
```

### SKILL.md Format

The `SKILL.md` file uses YAML frontmatter plus markdown:

```yaml
---
name: my-custom-skill
description: Short description of what this skill does
---

# Skill Name

Detailed instructions for the agent to follow when this skill is activated.

## Steps
1. First, do this...
2. Then do this...
3. Finally, verify by...
```

## Creating a Skill

### Step 1: Define the Purpose

Decide what behavior you want to codify:
- A specific coding pattern (e.g., "always use dependency injection")
- A workflow (e.g., "how to deploy to staging")
- Domain knowledge (e.g., "our API conventions")

### Step 2: Write the Instructions

Write clear, specific instructions in `SKILL.md`. Be explicit:

| ✅ Good | ❌ Bad |
|---|---|
| "Create a new file at `src/components/` with PascalCase naming" | "Make a component" |
| "Run `npm test` and verify all tests pass before committing" | "Test it" |
| "Use the `@injectable` decorator for all service classes" | "Follow DI patterns" |

### Step 3: Add Supporting Files

- **Scripts** — Automation helpers the agent can execute
- **Templates** — File starters (e.g., component scaffolds, config files)
- **Examples** — Reference implementations for the agent to learn from

### Step 4: Test the Skill

Ask the agent to use the skill and verify it follows instructions correctly. Iterate on the `SKILL.md` based on the results.

## Using Skills

Skills are automatically available when placed in the `.agents/skills/` directory. The agent detects and reads them when relevant to the current task.

You can also explicitly invoke a skill:
- Reference it by name in your prompt: *"Use the doc-maintainer skill to set up this repo"*
- The agent reads `SKILL.md` and follows the instructions

## Best Practices

### ✅ DO

- Keep instructions specific and actionable
- Include verification steps ("confirm X by checking Y")
- Organize complex skills into clear sections
- Include error handling guidance
- Version your skills alongside your code

### ❌ DON'T

- Write vague instructions the agent could misinterpret
- Create overly large skills — break them into focused modules
- Hard-code paths or secrets — use environment variables
- Skip testing — always verify the skill produces correct results

## Advanced: Skill Composition

Chain multiple skills together for complex workflows:

```
Agent reads skill-a → produces scaffolding
Agent reads skill-b → implements business logic
Agent reads skill-c → writes tests
```

This maps to Antigravity's **agent chaining** pattern where each agent specializes in one phase of the workflow.

## Example Skills

### Documentation Skill
```yaml
---
name: doc-maintainer
description: Automated documentation maintenance pipeline
---
# Doc Maintainer
1. Crawl official documentation sources listed in `docs/official-links.md`
2. Compare scraped content against existing `docs/` files
3. Update changed files preserving markdown formatting
4. Validate all links using the audit report
5. Update `docs/changelog.md` with new changes found
6. Commit with standard message format
```

### API Convention Skill
```yaml
---
name: api-conventions
description: Enforce REST API naming and response conventions
---
# API Conventions
- Endpoints use kebab-case: `/api/user-profiles`
- Response envelope: `{ "data": ..., "meta": { "total": N } }`
- Error format: `{ "error": { "code": "NOT_FOUND", "message": "..." } }`
- Always include `X-Request-Id` header
```

## See Also

- [Features](./features.md) — Core platform capabilities including rules and workflows
- [Agents](./agents.md) — Agent capabilities and advanced techniques
