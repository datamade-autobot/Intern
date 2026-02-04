# `.vscode/` Folder Guide

Understanding the difference between `.vscode/` and AI rules files.

---

## What is `.vscode/`?

The `.vscode/` folder contains **workspace-specific VS Code editor settings**. It's completely separate from AI assistant rules files.

### Location
```
your-project/
├── .vscode/           ← VS Code workspace settings (this guide)
│   ├── settings.json
│   ├── extensions.json
│   ├── tasks.json
│   └── launch.json
├── AGENTS.md          ← AI rules (separate)
└── your-code/
```

---

## `.vscode/` vs AI Rules Files

| Aspect | `.vscode/` Folder | AI Rules Files |
|--------|-------------------|----------------|
| **Purpose** | Configure VS Code editor | Guide AI assistant behavior |
| **Location** | `.vscode/` folder | Project root |
| **Read By** | VS Code | AI assistants (Claude, Copilot, etc.) |
| **Examples** | Tab size, formatting, themes | Code style, tech stack, commands |

---

## `.vscode/` Files

### 1. `settings.json` - Workspace Settings

**Purpose:** Override user settings for this workspace.

**Common Settings:**
```json
{
  // Editor behavior
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,

  // File handling
  "files.autoSave": "afterDelay",
  "files.trimTrailingWhitespace": true,
  "files.exclude": {
    "**/node_modules": true,
    "**/.git": true,
    "**/dist": true
  },

  // Language-specific
  "[python]": {
    "editor.defaultFormatter": "ms-python.black-formatter",
    "editor.formatOnSave": true
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },

  // Terminal
  "terminal.integrated.defaultProfile.osx": "zsh"
}
```

**Documentation:** [VS Code Settings](https://code.visualstudio.com/docs/getstarted/settings)

---

### 2. `extensions.json` - Recommended Extensions

**Purpose:** Suggest extensions to teammates.

**Example:**
```json
{
  "recommendations": [
    "anthropic.claude-code",
    "github.copilot",
    "esbenp.prettier-vscode",
    "dbaeumer.vscode-eslint",
    "eamodio.gitlens",
    "ms-python.python",
    "ms-python.vscode-pylance"
  ],
  "unwantedRecommendations": [
    "ms-vscode.vscode-typescript-tslint-plugin"
  ]
}
```

**What happens:**
- When teammates open the project, VS Code suggests installing these extensions
- They see: "This workspace recommends extensions"

**Documentation:** [Extension Recommendations](https://code.visualstudio.com/docs/editor/extension-marketplace#_workspace-recommended-extensions)

---

### 3. `tasks.json` - Task Automation

**Purpose:** Define custom tasks (build, test, deploy, etc.)

**Example:**
```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Run Tests",
      "type": "shell",
      "command": "npm test",
      "group": {
        "kind": "test",
        "isDefault": true
      },
      "presentation": {
        "reveal": "always",
        "panel": "new"
      }
    },
    {
      "label": "Build",
      "type": "shell",
      "command": "npm run build",
      "group": {
        "kind": "build",
        "isDefault": true
      }
    },
    {
      "label": "Start Dev Server",
      "type": "shell",
      "command": "npm run dev",
      "isBackground": true
    }
  ]
}
```

**How to use:**
- `Cmd/Ctrl + Shift + P` → "Tasks: Run Task"
- Or `Cmd/Ctrl + Shift + B` for build

**Documentation:** [VS Code Tasks](https://code.visualstudio.com/docs/editor/tasks)

---

### 4. `launch.json` - Debug Configuration

**Purpose:** Configure debugger settings.

**Example for Node.js:**
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "skipFiles": ["<node_internals>/**"],
      "program": "${workspaceFolder}/src/index.js"
    },
    {
      "type": "node",
      "request": "attach",
      "name": "Attach to Process",
      "port": 9229
    }
  ]
}
```

**Example for Python:**
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Python: Current File",
      "type": "python",
      "request": "launch",
      "program": "${file}",
      "console": "integratedTerminal"
    },
    {
      "name": "Python: Flask",
      "type": "python",
      "request": "launch",
      "module": "flask",
      "env": {
        "FLASK_APP": "app.py",
        "FLASK_ENV": "development"
      },
      "args": ["run", "--no-debugger"],
      "jinja": true
    }
  ]
}
```

**How to use:**
- Press `F5` to start debugging
- Or click the play button in the Debug panel

**Documentation:** [VS Code Debugging](https://code.visualstudio.com/docs/editor/debugging)

---

## Complete Example Setup

### Directory Structure
```
my-project/
├── .vscode/
│   ├── settings.json
│   ├── extensions.json
│   ├── tasks.json
│   └── launch.json
├── AGENTS.md                    # AI rules (not in .vscode!)
├── CLAUDE.md                    # AI rules
├── .editorconfig                # Editor consistency
├── .prettierrc                  # Prettier config
├── .eslintrc.js                 # ESLint config
├── package.json
└── src/
    └── index.js
```

### `.vscode/settings.json`
```json
{
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "files.exclude": {
    "**/node_modules": true,
    "**/.git": true,
    "**/dist": true
  }
}
```

### `.vscode/extensions.json`
```json
{
  "recommendations": [
    "anthropic.claude-code",
    "esbenp.prettier-vscode",
    "dbaeumer.vscode-eslint"
  ]
}
```

### `.vscode/tasks.json`
```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Test",
      "type": "shell",
      "command": "npm test",
      "group": {
        "kind": "test",
        "isDefault": true
      }
    }
  ]
}
```

---

## Common Use Cases

### 1. Enforce Code Style
```json
// .vscode/settings.json
{
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}
```

### 2. Standardize Tab Size
```json
{
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.detectIndentation": false
}
```

### 3. Hide Generated Files
```json
{
  "files.exclude": {
    "**/node_modules": true,
    "**/.git": true,
    "**/dist": true,
    "**/__pycache__": true,
    "**/*.pyc": true
  }
}
```

### 4. Python Project Setup
```json
{
  "python.defaultInterpreterPath": "${workspaceFolder}/venv/bin/python",
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "python.formatting.provider": "black",
  "[python]": {
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
      "source.organizeImports": true
    }
  }
}
```

---

## Should You Commit `.vscode/`?

### ✅ Commit These:
- `extensions.json` - Team should use same extensions
- `settings.json` - Enforce consistent formatting
- `tasks.json` - Shared build/test tasks
- `launch.json` - Shared debug configurations

### ❌ Don't Commit:
- Personal preferences (theme, font size)
- Local paths
- Credentials or tokens

### How to Handle:
```gitignore
# In .gitignore
.vscode/*
!.vscode/settings.json
!.vscode/tasks.json
!.vscode/launch.json
!.vscode/extensions.json
```

This commits shared configs but ignores personal stuff.

---

## Quick Reference

### Creating `.vscode/` Files

**Method 1: Manually**
```bash
mkdir .vscode
touch .vscode/settings.json
touch .vscode/extensions.json
```

**Method 2: VS Code UI**
- `Cmd/Ctrl + ,` → Click folder icon → Workspace settings
- This creates `settings.json` automatically

### Editing Settings

**Visual Editor:**
- `Cmd/Ctrl + ,` → Search for setting → Change value

**JSON Editor:**
- `Cmd/Ctrl + Shift + P` → "Preferences: Open Workspace Settings (JSON)"

---

## FAQs

### Q: Do I need both `.vscode/settings.json` and `AGENTS.md`?
**A:** Yes! They serve different purposes:
- `.vscode/settings.json` - How VS Code behaves (formatting, themes, etc.)
- `AGENTS.md` - How AI assistants code (style, patterns, commands)

### Q: Can AI read `.vscode/settings.json`?
**A:** AI can read it, but it's not designed for AI instructions. Use `AGENTS.md` instead.

### Q: What if settings conflict?
**A:** VS Code uses this order:
1. Default settings
2. User settings (`~/.config/Code/User/settings.json`)
3. Workspace settings (`.vscode/settings.json`) ← Wins

### Q: Can I share these with my team?
**A:** Yes! Commit `.vscode/` to git. Everyone gets the same setup.

---

## Resources

- **[VS Code Settings](https://code.visualstudio.com/docs/getstarted/settings)**
- **[Extension Recommendations](https://code.visualstudio.com/docs/editor/extension-marketplace#_workspace-recommended-extensions)**
- **[Tasks](https://code.visualstudio.com/docs/editor/tasks)**
- **[Debugging](https://code.visualstudio.com/docs/editor/debugging)**
- **[Settings Reference](https://code.visualstudio.com/docs/getstarted/settings#_settings-file-locations)**

---

**Remember:**
- `.vscode/` = Editor configuration
- `AGENTS.md` = AI instructions
- Both are useful, different purposes!
