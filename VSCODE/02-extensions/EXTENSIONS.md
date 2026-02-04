# VS Code Extensions Guide

A curated list of extensions organized by category. Install only what you need - too many extensions can slow down VS Code.

---

## 🤖 AI Assistants (Pick Your Stack)

### Primary Recommendation
| Extension | Publisher | Description |
|-----------|-----------|-------------|
| **Claude Code** | Anthropic | Agentic coding assistant with multi-file editing, terminal access |
| **GitHub Copilot** | GitHub | AI pair programmer with inline suggestions |

### Alternatives
| Extension | Publisher | Description |
|-----------|-----------|-------------|
| Tabnine | Tabnine | AI completions with local/cloud models |
| Codeium | Codeium | Free AI code completion |
| Amazon Q | AWS | AWS-focused AI assistant |

**💡 Pro Tip:** Many developers run Claude Code for complex tasks and Copilot for inline suggestions. They complement each other well.

---

## 🔍 Code Quality & Linting

### Essential
| Extension | ID | Description |
|-----------|-----------|-------------|
| **ESLint** | `dbaeumer.vscode-eslint` | JavaScript/TypeScript linting |
| **Prettier** | `esbenp.prettier-vscode` | Code formatting for multiple languages |
| **Error Lens** | `usernamehw.errorlens` | Inline display of errors/warnings |

### Language-Specific
| Extension | ID | Description |
|-----------|-----------|-------------|
| Pylint | `ms-python.pylint` | Python linting |
| Ruff | `charliermarsh.ruff` | Fast Python linter (alternative to Pylint) |
| SonarLint | `sonarsource.sonarlint-vscode` | Multi-language code quality |

**Configuration tip:** Add to your `settings.json`:
```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```

---

## 🐙 Git & Version Control

| Extension | ID | Description |
|-----------|-----------|-------------|
| **GitLens** | `eamodio.gitlens` | Git blame, history, comparison (essential!) |
| Git Graph | `mhutchie.git-graph` | Visual git history graph |
| GitHub Pull Requests | `github.vscode-pull-request-github` | Review PRs without leaving VS Code |

**💡 GitLens is a game-changer.** See who changed any line, when, and why - directly in your editor.

---

## 🐍 Python Development

| Extension | ID | Description |
|-----------|-----------|-------------|
| **Python** | `ms-python.python` | Core Python support (required) |
| **Pylance** | `ms-python.vscode-pylance` | Fast, feature-rich language support |
| Jupyter | `ms-toolsai.jupyter` | Notebook support |
| Python Debugger | `ms-python.debugpy` | Debugging support |

**Configuration tip:**
```json
{
  "python.analysis.typeCheckingMode": "basic",
  "python.formatting.provider": "black",
  "[python]": {
    "editor.defaultFormatter": "ms-python.black-formatter"
  }
}
```

---

## 🌐 JavaScript/TypeScript Development

| Extension | ID | Description |
|-----------|-----------|-------------|
| **TypeScript** | Built-in | TypeScript support |
| ES7+ Snippets | `dsznajder.es7-react-js-snippets` | React/JS snippets |
| Import Cost | `wix.vscode-import-cost` | Show size of imported packages |
| Auto Rename Tag | `formulahendry.auto-rename-tag` | Rename paired HTML/JSX tags |

---

## 🧪 Testing & Debugging

| Extension | ID | Description |
|-----------|-----------|-------------|
| **Test Explorer UI** | `hbenl.vscode-test-explorer` | Universal test runner UI |
| Jest | `orta.vscode-jest` | Jest test integration |
| Playwright | `ms-playwright.playwright` | E2E testing support |
| Thunder Client | `rangav.vscode-thunder-client` | API testing (like Postman) |

---

## 🐳 DevOps & Infrastructure

| Extension | ID | Description |
|-----------|-----------|-------------|
| **Docker** | `ms-azuretools.vscode-docker` | Container management |
| YAML | `redhat.vscode-yaml` | YAML support with validation |
| Remote - SSH | `ms-vscode-remote.remote-ssh` | Develop on remote machines |
| Dev Containers | `ms-vscode-remote.remote-containers` | Develop in containers |

---

## 👥 Collaboration

| Extension | ID | Description |
|-----------|-----------|-------------|
| **Live Share** | `ms-vsliveshare.vsliveshare` | Real-time collaborative editing |
| CodeTour | `vsls-contrib.codetour` | Guided code walkthroughs |

---

## 📝 Productivity & Quality of Life

| Extension | ID | Description |
|-----------|-----------|-------------|
| **Code Spell Checker** | `streetsidesoftware.code-spell-checker` | Catch typos in code/comments |
| Todo Tree | `gruntfuggly.todo-tree` | Find and organize TODOs |
| Bookmarks | `alefragnani.bookmarks` | Mark and navigate code locations |
| Project Manager | `alefragnani.project-manager` | Switch between projects easily |
| WakaTime | `wakatime.vscode-wakatime` | Track coding time |

---

## 🎨 Themes & Appearance

| Extension | Description |
|-----------|-------------|
| **One Dark Pro** | Popular dark theme |
| **GitHub Theme** | GitHub's official themes |
| Material Icon Theme | Better file icons |
| Peacock | Color different workspaces |

---

## 🚀 Installation Script

Run this in VS Code terminal to install essentials:

```bash
# Core AI & Quality
code --install-extension anthropic.claude-code
code --install-extension github.copilot
code --install-extension dbaeumer.vscode-eslint
code --install-extension esbenp.prettier-vscode

# Git
code --install-extension eamodio.gitlens

# Python
code --install-extension ms-python.python
code --install-extension ms-python.vscode-pylance

# Productivity
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension usernamehw.errorlens
```

---

## ⚙️ Recommended Settings

Add to your user `settings.json` (`Cmd+Shift+P` → "Preferences: Open User Settings (JSON)"):

```json
{
  // Editor
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.minimap.enabled": false,
  "editor.formatOnSave": true,
  "editor.bracketPairColorization.enabled": true,

  // Files
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "files.trimTrailingWhitespace": true,

  // Terminal
  "terminal.integrated.fontSize": 13,

  // Git
  "git.autofetch": true,
  "git.confirmSync": false,

  // AI
  "chat.useAgentsMdFile": true
}
```

---

## 📊 Extension Management Tips

1. **Disable per-workspace:** Right-click extension → "Disable (Workspace)" for project-specific needs
2. **Check performance:** `Cmd+Shift+P` → "Developer: Show Running Extensions"
3. **Sync settings:** Sign in to sync extensions across machines
4. **Regular cleanup:** Uninstall extensions you haven't used in months
