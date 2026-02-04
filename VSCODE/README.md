# VS Code Power Hour: Agentic IDE Foundations

Welcome to your VS Code deep dive! This repository contains everything you need to transform VS Code from a text editor into a powerful agentic development environment.

---

## 🎯 Session Objectives

By the end of this hour, you'll understand:
1. **Why configuration matters** - How rules files shape AI behavior
2. **The agentic toolchain** - Claude Code, Copilot, Cursor, and when to use each
3. **MCP (Model Context Protocol)** - Connecting AI to external tools
4. **Skills & Extensions** - Extending your IDE's capabilities
5. **Markdown mastery** - The universal language of AI communication

---

## 📁 Repository Structure

```
VSCODE/
├── README.md                    # You are here
├── 01-rules-files/
│   ├── CLAUDE.md               # Claude Code configuration template
│   ├── AGENTS.md               # Universal agent instructions
│   └── copilot-instructions.md # GitHub Copilot custom instructions
├── 02-extensions/
│   └── EXTENSIONS.md           # Recommended extensions by category
├── 03-mcp-setup/
│   ├── MCP-GUIDE.md            # Model Context Protocol explained
│   └── mcp-config-example.json # Sample MCP configuration
├── 04-skills/
│   ├── SKILLS-OVERVIEW.md      # Understanding agent skills
│   └── example-skill/
│       └── SKILL.md            # Template skill file
├── 05-markdown/
│   └── MARKDOWN-CONVENTIONS.md # Writing effective AI prompts
├── 06-workflows/
│   └── DAILY-WORKFLOW.md       # Recommended daily practices
└── CHEATSHEET.md               # Quick reference card
```

---

## 🚀 Quick Start (Do This First!)

### 1. Install VS Code Extensions
Open VS Code, press `Cmd+Shift+X` (Mac) or `Ctrl+Shift+X` (Windows), and install:
- **Claude Code** (Anthropic) - Your primary agentic assistant
- **GitHub Copilot** - AI pair programmer
- **GitLens** - Git supercharged
- **Prettier** - Code formatting
- **ESLint** - JavaScript/TypeScript linting

### 2. Copy Configuration Files
```bash
# Copy rules files to your project root
cp 01-rules-files/CLAUDE.md ~/your-project/
cp 01-rules-files/AGENTS.md ~/your-project/
```

### 3. Verify Claude Code Setup
```bash
# In terminal, check Claude Code is working
claude --version
claude /doctor
```

---

## 📚 Training Modules

### Module 1: Rules Files (15 min)
**Location:** `01-rules-files/`

Rules files are how you teach AI assistants about YOUR project. Think of them as onboarding documents for your AI pair programmer.

| File | Purpose | Used By |
|------|---------|---------|
| `CLAUDE.md` | Project conventions, build commands, style guides | Claude Code |
| `AGENTS.md` | Universal instructions for any AI agent | VS Code, Copilot, Claude |
| `copilot-instructions.md` | GitHub Copilot-specific settings | GitHub Copilot |

**Key Principle:** Keep rules files concise. AI agents work best with clear, actionable instructions rather than verbose documentation.

---

### Module 2: Extensions (10 min)
**Location:** `02-extensions/`

Extensions fall into categories:
- **AI Assistants** - Claude Code, Copilot, Tabnine
- **Code Quality** - ESLint, Prettier, SonarLint
- **Git & Collaboration** - GitLens, Live Share
- **Language Support** - Python, Pylance, TypeScript
- **Productivity** - Docker, WakaTime, Code Spell Checker

**Pro Tip:** Don't install everything at once. Start with essentials and add as needed.

---

### Module 3: MCP - Model Context Protocol (15 min)
**Location:** `03-mcp-setup/`

MCP is how AI agents connect to external tools and data sources. Examples:
- GitHub API for PR reviews
- Database connections
- Slack integration
- File system access

**Key Commands:**
```bash
# List configured MCP servers
claude /mcp

# Add a new MCP server
# Via VS Code: Cmd+Shift+P → "MCP: Add Server"
```

---

### Module 4: Skills (10 min)
**Location:** `04-skills/`

Skills are reusable instruction sets that extend AI capabilities:
- **Project Skills** - Stored in `.github/skills/` or `.claude/skills/`
- **Personal Skills** - Stored in `~/.claude/skills/`

Skills can include:
- Domain knowledge (your company's coding standards)
- Workflow automation (how to deploy)
- Templates (PR descriptions, commit messages)

---

### Module 5: Markdown Conventions (5 min)
**Location:** `05-markdown/`

Markdown is the universal language for communicating with AI:
- Structure prompts with headers
- Use code blocks for examples
- Bullet points for lists of requirements
- XML-style tags for context boundaries

---

### Module 6: Daily Workflow (5 min)
**Location:** `06-workflows/`

A suggested workflow for maximum productivity:
1. **Start of day:** Review tasks, open relevant files
2. **Development:** Use agent mode for complex tasks, edit mode for focused changes
3. **Testing:** Let AI run and fix tests
4. **Code review:** Use AI for initial review, then human review
5. **End of day:** Clean context with `/clear`, commit changes

---

## 🔑 Key Takeaways

1. **Configuration is power** - Well-crafted rules files make AI 10x more useful
2. **Right tool for the job** - Use agent mode for exploration, edit mode for precision
3. **Keep context clean** - Run `/clear` between unrelated tasks
4. **Iterate and refine** - Update your CLAUDE.md as you learn what works
5. **Trust but verify** - AI is a collaborator, not a replacement for thinking

---

## 📖 Additional Resources

- [Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)
- [VS Code Agent Skills Documentation](https://code.visualstudio.com/docs/copilot/customization/agent-skills)
- [MCP Server Documentation](https://code.visualstudio.com/docs/copilot/customization/mcp-servers)
- [GitHub Copilot Overview](https://code.visualstudio.com/docs/copilot/overview)

---

## ❓ Questions?

During the session, don't hesitate to ask! After the session:
- Experiment with these files in a test project
- Try modifying CLAUDE.md and see how behavior changes
- Join the Claude Code community for tips and tricks

**Happy coding!** 🚀
