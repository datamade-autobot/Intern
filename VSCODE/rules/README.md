# Rules Files Directory

This folder contains ready-to-use rules file templates for different AI coding assistants.

## Quick Start

1. **Choose your AI assistant:**
   - Using Claude Code? → Copy `CLAUDE.md` to your project root
   - Using any AI tool? → Copy `AGENTS.md` to your project root (works everywhere)
   - Using GitHub Copilot? → Copy `copilot-instructions.md` to your project root
   - Using Cursor? → Copy `.cursorrules` to your project root

2. **Customize for your project:**
   - Fill in your tech stack
   - Add your code style preferences
   - List common commands
   - Note any gotchas or constraints

3. **Test it:**
   - Open your project in VS Code
   - Ask your AI assistant: "What are the rules for this project?"
   - It should reference your file

## File Descriptions

| File | Purpose | Works With |
|------|---------|------------|
| `AGENTS.md` | Universal rules for all AI agents | Claude Code, Cursor, Copilot, and others |
| `CLAUDE.md` | Claude Code specific configuration | Claude Code extension |
| `copilot-instructions.md` | GitHub Copilot instructions | GitHub Copilot |
| `.cursorrules` | Cursor IDE rules | Cursor |
| `template-basic.md` | Minimal template to get started | All AI tools |
| `template-full.md` | Comprehensive template with examples | All AI tools |

## Best Practices

### Start Simple
Begin with `template-basic.md` and add sections as needed. Don't over-engineer.

### One Source of Truth
**Recommended approach:** Use `AGENTS.md` as your primary file. It works with all tools.

### Project-Specific
Each project should have its own rules file tailored to that codebase.

### Keep It Updated
Update your rules file as your project evolves and you discover what works.

### Test with AI
After creating a rules file, ask your AI: "What coding standards should I follow?" to verify it's working.

## Examples by Project Type

### Web API
```markdown
## Stack
- Node.js 20
- Express.js
- PostgreSQL
- Redis

## Code Style
- Use async/await
- REST conventions
- OpenAPI documentation
```

### Python CLI
```markdown
## Stack
- Python 3.11
- Click (CLI framework)
- pytest

## Code Style
- Type hints everywhere
- PEP 8 compliance
- Docstrings for all functions
```

### React App
```markdown
## Stack
- React 18
- TypeScript
- Tailwind CSS
- Vite

## Code Style
- Functional components
- Custom hooks for logic
- Tailwind for styling
```

## Troubleshooting

**AI not following rules?**
- Check file is in project root
- Verify file name is correct
- Ask AI: "Can you see the project rules?"

**Which file should I use?**
- **Best for most:** `AGENTS.md` (universal)
- **Claude Code only:** `CLAUDE.md`
- **Copilot only:** `copilot-instructions.md`
- **Cursor only:** `.cursorrules`

## Resources

- [Full guide on rules files](../01-rules-files/)
- [Markdown best practices](../MARKDOWN-GUIDE.md)
- [Example projects with rules](../06-workflows/)
