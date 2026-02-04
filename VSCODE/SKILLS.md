# Agent Skills in VS Code

## What Are Agent Skills?

Agent skills are specialized mini-programs that AI coding assistants can execute to perform complex tasks. Think of them as "superpowers" you can give your AI assistant.

## Available Skills

### Claude Code Skills

Claude Code supports custom skills through a `/` command interface:

- `/commit` - Intelligent git commit creation
- `/review-pr` - Pull request review and analysis
- `/test` - Test file generation and execution
- `/docs` - Documentation generation
- `/refactor` - Code refactoring assistance

### GitHub Copilot Agent Skills

Copilot has built-in agent mode with skills:

- `@workspace` - Workspace-wide code search and analysis
- `@terminal` - Terminal command assistance
- `@vscode` - VS Code command execution
- `@github` - GitHub integration (PRs, issues, etc.)

## Creating Custom Skills

### For Claude Code

Create skills in `~/.claude/skills/`:

```bash
~/.claude/skills/
  my-skill/
    skill.yaml    # Skill definition
    prompt.md     # Skill instructions
```

**Example skill.yaml:**

```yaml
name: deploy
description: Deploy application to staging or production
parameters:
  - name: environment
    description: Target environment
    required: true
    type: choice
    choices: [staging, production]
```

### For GitHub Copilot

Configure in `.github/copilot-instructions.md`:

```markdown
## Custom Workflows

When deploying:
1. Run tests first
2. Check for uncommitted changes
3. Build the project
4. Deploy to specified environment
5. Verify deployment
```

## Best Practices

### 1. **Start Simple**
Begin with built-in skills before creating custom ones.

### 2. **Clear Descriptions**
Make skill descriptions self-explanatory:
```yaml
# Good
description: "Deploy app to staging with health checks"

# Bad
description: "Deploy"
```

### 3. **Document Parameters**
Always explain what each parameter does:
```yaml
parameters:
  - name: branch
    description: "Git branch to deploy (default: main)"
```

### 4. **Error Handling**
Include clear error messages in your skill logic.

### 5. **Test Thoroughly**
Test skills in safe environments before production use.

## Common Use Cases

### Code Review
```bash
# Claude Code
/review-pr 123

# Copilot
@github review pull request #123
```

### Testing
```bash
# Claude Code
/test src/components/Button.tsx

# Copilot (in chat)
@workspace generate tests for Button component
```

### Documentation
```bash
# Claude Code
/docs --update

# Copilot
@workspace document all public APIs
```

### Refactoring
```bash
# Claude Code
/refactor extract-function

# Copilot
@workspace refactor UserService to use dependency injection
```

## Skill Discovery

### Finding Available Skills

**Claude Code:**
```bash
# In CLI
claude --help

# In VS Code
Type / in chat to see available skills
```

**GitHub Copilot:**
```
# In chat
@workspace /help
```

## Advanced: Skill Composition

Chain multiple skills for complex workflows:

```markdown
1. @workspace find all API endpoints
2. /docs generate API documentation
3. /commit with message "docs: update API documentation"
4. @github create PR for documentation
```

## Debugging Skills

If a skill isn't working:

1. **Check logs:**
   - Claude Code: `~/.claude/logs/`
   - Copilot: VS Code Output panel → "GitHub Copilot"

2. **Verify configuration:**
   - Check skill definitions
   - Validate YAML/JSON syntax

3. **Test in isolation:**
   - Run skill with minimal parameters
   - Check permissions

## Quick Reference

| Task | Claude Code | GitHub Copilot |
|------|-------------|----------------|
| Commit | `/commit` | Chat → git operations |
| Review | `/review-pr` | `@github review` |
| Test | `/test` | `@workspace test` |
| Docs | `/docs` | `@workspace document` |
| Workspace search | Task tool | `@workspace` |
| Terminal help | Bash tool | `@terminal` |

## Resources

- [VS Code Agent Skills](https://code.visualstudio.com/docs/copilot/agent-skills)
- [Claude Code Skills](https://code.claude.com/docs/skills)
- [Creating Custom Skills](https://docs.anthropic.com/en/docs/skills)

---

**Pro Tip:** Start by mastering 2-3 skills that match your daily workflow, then gradually expand your toolkit as you discover new needs.
