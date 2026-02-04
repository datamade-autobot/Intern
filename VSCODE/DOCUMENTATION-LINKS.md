# Documentation & Resources

Complete reference guide to all tools, extensions, and concepts covered in this training.

---

## 📚 Official Documentation

### VS Code Core
- **[VS Code Official Docs](https://code.visualstudio.com/docs)** - Complete VS Code documentation
- **[VS Code API](https://code.visualstudio.com/api)** - Extension development
- **[VS Code Keyboard Shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings)** - Customize shortcuts
- **[VS Code Settings](https://code.visualstudio.com/docs/getstarted/settings)** - Configure VS Code
- **[VS Code Tips & Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)** - Productivity tips

### AI Assistants

#### Claude Code
- **[Claude Code Official Site](https://claude.com/claude-code)** - Product homepage
- **[Claude Code Documentation](https://code.claude.com/docs)** - Complete guide
- **[Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)** - Recommended patterns
- **[Anthropic API Docs](https://docs.anthropic.com/)** - API reference
- **[Claude Agent SDK](https://github.com/anthropics/anthropic-sdk-typescript)** - Build custom agents

#### GitHub Copilot
- **[GitHub Copilot Overview](https://code.visualstudio.com/docs/copilot/overview)** - Getting started
- **[GitHub Copilot Docs](https://docs.github.com/copilot)** - Official documentation
- **[Copilot Agent Skills](https://code.visualstudio.com/docs/copilot/agent-skills)** - Agent mode guide
- **[Copilot Custom Instructions](https://code.visualstudio.com/docs/copilot/customization)** - Configure behavior
- **[Copilot Workspace](https://code.visualstudio.com/docs/copilot/workspace-context)** - Context management

#### Cursor
- **[Cursor Official Site](https://cursor.sh/)** - Product homepage
- **[Cursor Documentation](https://docs.cursor.sh/)** - Official docs
- **[Cursor Rules Guide](https://cursor.directory/)** - Community rules repository

### MCP (Model Context Protocol)
- **[MCP Specification](https://modelcontextprotocol.io/)** - Official protocol spec
- **[MCP in VS Code](https://code.visualstudio.com/docs/copilot/customization/mcp-servers)** - VS Code integration
- **[MCP Server List](https://github.com/modelcontextprotocol/servers)** - Official MCP servers
- **[Building MCP Servers](https://modelcontextprotocol.io/docs/building-servers)** - Create custom servers

---

## 🛠️ VS Code Configuration Files

### `.vscode/` Folder
The `.vscode/` folder contains **workspace-specific** VS Code settings (not AI rules).

| File | Purpose | Documentation |
|------|---------|---------------|
| `settings.json` | Workspace settings | [Settings Docs](https://code.visualstudio.com/docs/getstarted/settings) |
| `extensions.json` | Recommended extensions | [Extensions Docs](https://code.visualstudio.com/docs/editor/extension-marketplace#_workspace-recommended-extensions) |
| `tasks.json` | Task automation | [Tasks Docs](https://code.visualstudio.com/docs/editor/tasks) |
| `launch.json` | Debug configurations | [Debugging Docs](https://code.visualstudio.com/docs/editor/debugging) |

**Example `.vscode/settings.json`:**
```json
{
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "files.exclude": {
    "**/.git": true,
    "**/node_modules": true
  }
}
```

### AI Rules Files (Project Root)
These files guide **AI assistant behavior** (place in project root, not `.vscode/`).

| File | For | Location | Documentation |
|------|-----|----------|---------------|
| `AGENTS.md` | All AI tools | Project root | [See rules/README.md](rules/README.md) |
| `CLAUDE.md` | Claude Code | Project root | [Claude Docs](https://code.claude.com/docs) |
| `.cursorrules` | Cursor | Project root | [Cursor Rules](https://docs.cursor.sh/) |
| `copilot-instructions.md` | GitHub Copilot | Project root | [Copilot Custom Instructions](https://code.visualstudio.com/docs/copilot/customization) |

**Key Difference:**
- `.vscode/` = VS Code editor settings
- `AGENTS.md` etc. = AI assistant instructions

---

## 📦 Extensions

### Essential Extensions

#### AI Assistants
- **[Claude Code](https://marketplace.visualstudio.com/items?itemName=anthropic.claude-code)** - Claude AI assistant
- **[GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)** - AI pair programmer
- **[GitHub Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)** - Chat interface

#### Code Quality
- **[Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)** - Code formatter
  - [Prettier Docs](https://prettier.io/docs/en/)
- **[ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)** - JavaScript linter
  - [ESLint Docs](https://eslint.org/docs/)
- **[Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)** - Inline errors

#### Git & Collaboration
- **[GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)** - Git supercharged
  - [GitLens Docs](https://help.gitkraken.com/gitlens/gitlens-home/)

#### Language Support
- **[Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)** - Python support
  - [Python in VS Code](https://code.visualstudio.com/docs/languages/python)
- **[Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)** - Python language server
- **[Go](https://marketplace.visualstudio.com/items?itemName=golang.go)** - Go support
  - [Go in VS Code](https://code.visualstudio.com/docs/languages/go)
- **[rust-analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)** - Rust support
  - [Rust in VS Code](https://code.visualstudio.com/docs/languages/rust)

#### Productivity
- **[Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)** - File path autocomplete
- **[Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)** - HTML/JSX tag sync
- **[Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)** - Markdown support

---

## 📖 Learning Resources

### Official Guides
- **[VS Code Getting Started](https://code.visualstudio.com/docs/getstarted/introvideos)** - Video tutorials
- **[VS Code Tips](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)** - Productivity tips
- **[Copilot Quickstart](https://docs.github.com/en/copilot/quickstart)** - Get started with Copilot
- **[Claude Code Quickstart](https://code.claude.com/docs/quickstart)** - Get started with Claude

### Best Practices
- **[Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)** - Recommended patterns
- **[GitHub Copilot Best Practices](https://github.blog/developer-skills/github/how-to-use-github-copilot-in-vs-code/)** - Usage tips
- **[Prompt Engineering Guide](https://www.promptingguide.ai/)** - Write better prompts
- **[VS Code Can Do That?](https://vscodecandothat.com/)** - Hidden features

### Community Resources
- **[r/vscode](https://reddit.com/r/vscode)** - VS Code subreddit
- **[VS Code Discord](https://discord.com/invite/vscode)** - Official Discord
- **[Cursor Community](https://forum.cursor.sh/)** - Cursor forum
- **[Claude Discord](https://discord.gg/anthropic)** - Claude community

---

## 🔧 Configuration Examples

### Complete Setup Example

**Project Structure:**
```
my-project/
├── .vscode/                        # VS Code workspace settings
│   ├── settings.json               # Editor preferences
│   ├── extensions.json             # Recommended extensions
│   └── tasks.json                  # Custom tasks
├── AGENTS.md                       # Universal AI rules
├── CLAUDE.md                       # Claude-specific rules
├── copilot-instructions.md         # Copilot rules
├── .cursorrules                    # Cursor rules
├── .editorconfig                   # Editor consistency
├── .prettierrc                     # Prettier config
├── .eslintrc.js                    # ESLint config
└── [your code...]
```

**`.vscode/settings.json` Example:**
```json
{
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "files.exclude": {
    "**/node_modules": true,
    "**/.git": true
  },
  "[python]": {
    "editor.defaultFormatter": "ms-python.black-formatter"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}
```

**`.vscode/extensions.json` Example:**
```json
{
  "recommendations": [
    "anthropic.claude-code",
    "github.copilot",
    "esbenp.prettier-vscode",
    "dbaeumer.vscode-eslint",
    "eamodio.gitlens"
  ]
}
```

---

## 🎓 Tutorials & Courses

### Official Tutorials
- **[VS Code Introductory Videos](https://code.visualstudio.com/docs/getstarted/introvideos)** - Official video series
- **[GitHub Copilot Tutorial](https://github.com/skills/copilot)** - Interactive tutorial
- **[Anthropic Prompt Engineering](https://docs.anthropic.com/claude/docs/prompt-engineering)** - Official guide

### YouTube Channels
- **[Visual Studio Code](https://www.youtube.com/@code)** - Official channel
- **[GitHub](https://www.youtube.com/@GitHub)** - Copilot demos
- **[Fireship](https://www.youtube.com/@Fireship)** - Quick VS Code tips

---

## 🔍 Quick Reference

### Keyboard Shortcuts
- **[Windows Shortcuts PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)**
- **[macOS Shortcuts PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)**
- **[Linux Shortcuts PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf)**

### Cheat Sheets
- **[VS Code Cheat Sheet](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)**
- **[Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)**
- **[Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)**

---

## 🆘 Troubleshooting

### Common Issues
- **[VS Code Troubleshooting](https://code.visualstudio.com/docs/supporting/troubleshoot)** - Official guide
- **[Extension Issues](https://code.visualstudio.com/docs/editor/extension-marketplace#_troubleshooting)** - Extension problems
- **[Copilot Troubleshooting](https://docs.github.com/en/copilot/troubleshooting-github-copilot)** - Copilot issues

### Getting Help
- **[VS Code Issues](https://github.com/microsoft/vscode/issues)** - Report bugs
- **[Stack Overflow](https://stackoverflow.com/questions/tagged/visual-studio-code)** - Q&A
- **[VS Code Discussions](https://github.com/microsoft/vscode-discussions)** - Community discussions

---

## 📱 Additional Tools

### Command Line
- **[VS Code CLI](https://code.visualstudio.com/docs/editor/command-line)** - Command line interface
- **[GitHub CLI (`gh`)](https://cli.github.com/)** - GitHub from terminal
- **[Git Documentation](https://git-scm.com/doc)** - Git reference

### Integrations
- **[GitHub Actions](https://docs.github.com/actions)** - CI/CD
- **[Docker Extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)** - Container support
- **[Remote Development](https://code.visualstudio.com/docs/remote/remote-overview)** - Remote coding

---

## 🌟 This Repository's Resources

### Training Materials
- **[README.md](README.md)** - Start here
- **[LIVE-SESSION-AGENDA.md](LIVE-SESSION-AGENDA.md)** - Today's session plan
- **[SESSION-OUTLINE.md](SESSION-OUTLINE.md)** - Full training outline
- **[EXERCISES.md](EXERCISES.md)** - Hands-on practice

### Configuration Guides
- **[rules/](rules/)** - Rules file templates
- **[01-rules-files/](01-rules-files/)** - Detailed rules examples
- **[MARKDOWN-GUIDE.md](MARKDOWN-GUIDE.md)** - Markdown best practices

### Reference Guides
- **[EXTENSIONS.md](EXTENSIONS.md)** - Extension recommendations
- **[KEYBOARD-SHORTCUTS.md](KEYBOARD-SHORTCUTS.md)** - Essential shortcuts
- **[SKILLS.md](SKILLS.md)** - Agent skills guide
- **[MCP-GUIDE.md](MCP-GUIDE.md)** - MCP setup guide

---

## 🔖 Bookmark These

**Most Important:**
1. [VS Code Docs](https://code.visualstudio.com/docs) - Your primary reference
2. [Claude Code Docs](https://code.claude.com/docs) - If using Claude Code
3. [GitHub Copilot Docs](https://docs.github.com/copilot) - If using Copilot
4. [This folder](.) - Your training materials

**For Daily Use:**
1. [Keyboard Shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings)
2. [Extension Marketplace](https://marketplace.visualstudio.com/vscode)
3. [Stack Overflow](https://stackoverflow.com/questions/tagged/visual-studio-code)

---

*Last updated: 2026-02-04*
*Maintained by: This repository*
