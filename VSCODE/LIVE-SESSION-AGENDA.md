# Live VS Code Power Hour - Today's Session

**Session Type:** Hands-On Dev Environment Setup
**Duration:** 60 minutes (1:00 PM - 2:00 PM)
**Format:** Live installation, configuration, and optimization
**Prerequisites:** Computer with internet connection

---

## 🎯 Today's Goals

By the end of this session, we'll have:
1. ✅ VS Code installed and configured
2. ✅ Essential extensions installed and working
3. ✅ AI assistants (Claude Code/Copilot) set up and authenticated
4. ✅ First AGENTS.md configuration file created
5. ✅ Hands-on practice with key shortcuts and workflows
6. ✅ A working, optimized development environment ready to use

---

## ⏱️ Session Timeline

### **Segment 1: Setup & Installation (15 mins) - 1:00-1:15**

#### 1.1 VS Code Installation (5 mins)
- Download VS Code if not already installed
- Quick tour of the interface
- Set up preferences (theme, font size, etc.)

**Checkpoint:** VS Code opens and looks good ✓

#### 1.2 Essential Extensions Installation (10 mins)

Install these extensions live:

**AI Assistants:**
- [ ] Claude Code (primary assistant)
- [ ] GitHub Copilot (if available)

**Code Quality:**
- [ ] Prettier (code formatter)
- [ ] ESLint (JavaScript/TypeScript linting)
- [ ] Error Lens (inline error display)

**Productivity:**
- [ ] GitLens (Git visualization)
- [ ] Path Intellisense (file path autocomplete)
- [ ] Auto Rename Tag (HTML/JSX tag sync)

**Language-Specific:** (based on what you'll use)
- [ ] Python + Pylance (if Python)
- [ ] Go extension (if Go)
- [ ] rust-analyzer (if Rust)

**Checkpoint:** All extensions installed and enabled ✓

---

### **Segment 2: AI Assistant Configuration (15 mins) - 1:15-1:30**

#### 2.1 Authenticate AI Tools (5 mins)
- Sign into Claude Code
- Authenticate GitHub Copilot (if using)
- Verify both are working with a test prompt

**Test Prompt:**
```
Write a Python function that returns "Hello World"
```

**Checkpoint:** AI assistants respond and generate code ✓

#### 2.2 Create Your First AGENTS.md (10 mins)

We'll create a real AGENTS.md file together for your actual project.

**Live Exercise:**
1. Create `AGENTS.md` in your project root
2. Fill in these sections together:

```markdown
# AI Agent Instructions

## Project Context
[We'll fill this in based on your actual project]

## Stack
[Your actual tech stack]

## Code Style Preferences
[Your preferences - we'll discuss]

## Common Commands
[Commands you use frequently]

## Important Notes
[Any gotchas or conventions]
```

**Checkpoint:** AGENTS.md created and saved ✓

---

### **Segment 3: Hands-On Practice (20 mins) - 1:30-1:50**

#### 3.1 Essential Shortcuts Drill (7 mins)

**Follow along - we'll practice these together:**

1. **Quick Open:** `Cmd/Ctrl + P`
   - Open any file instantly
   - Try: Type "agents" to open AGENTS.md

2. **Command Palette:** `Cmd/Ctrl + Shift + P`
   - Access any VS Code command
   - Try: "Format Document"

3. **Multi-Cursor:** `Cmd/Ctrl + D`
   - Select word
   - Press `Cmd/Ctrl + D` to select next occurrence
   - Type to change all at once

4. **Move Lines:** `Alt + Up/Down`
   - Select a line
   - Move it up or down

5. **Toggle Comment:** `Cmd/Ctrl + /`
   - Comment/uncomment code instantly

**Checkpoint:** Comfortable with these 5 shortcuts ✓

#### 3.2 AI-Assisted Coding Exercise (8 mins)

**Live Coding Together:**

We'll write a simple function using AI assistance:

**Challenge:** Create a temperature converter
- Ask AI to write a function that converts Celsius to Fahrenheit
- Ask AI to add error handling
- Ask AI to write tests
- Run the tests together

**What we'll learn:**
- How to prompt AI effectively
- When to use chat vs inline editing
- How to iterate with AI

**Checkpoint:** Successfully wrote and tested code with AI ✓

#### 3.3 Git Workflow in VS Code (5 mins)

**Live Demo:**
1. Make a change to a file
2. Open Source Control (`Cmd/Ctrl + Shift + G`)
3. Review the diff
4. Stage the change
5. Ask AI to suggest a commit message
6. Commit (don't push yet)

**Checkpoint:** Made first commit in VS Code ✓

---

### **Segment 4: Optimization & Next Steps (10 mins) - 1:50-2:00**

#### 4.1 Settings Optimization (5 mins)

We'll configure these settings together:

**Open Settings:** `Cmd/Ctrl + ,`

**Key Settings to Configure:**
- `editor.formatOnSave: true` - Auto-format when saving
- `editor.tabSize: 2 or 4` - Based on your preference
- `files.autoSave: afterDelay` - Auto-save files
- `editor.minimap.enabled: false` - (optional) Disable minimap
- `editor.fontSize: [your preference]` - Comfortable reading size

**Checkpoint:** Settings optimized for your workflow ✓

#### 4.2 Terminal Setup (3 mins)

- Open integrated terminal: `` Ctrl + ` ``
- Verify your shell (bash/zsh/powershell)
- Test a few commands:
  ```bash
  pwd
  ls
  python --version  # or node --version, etc.
  ```

**Checkpoint:** Terminal works and feels good ✓

#### 4.3 Quick Wins & Next Steps (2 mins)

**Quick Wins You Just Got:**
- Professional dev environment setup
- AI pair programmer ready to use
- Git workflow integrated
- Key shortcuts in muscle memory

**Next Steps After Today:**
1. **This Week:**
   - Use the 5 shortcuts we practiced daily
   - Write code with AI assistance at least once per day
   - Update your AGENTS.md as you learn what works

2. **Reference Materials:**
   - [KEYBOARD-SHORTCUTS.md](KEYBOARD-SHORTCUTS.md) - Master more shortcuts
   - [EXTENSIONS.md](EXTENSIONS.md) - Explore more extensions
   - [EXERCISES.md](EXERCISES.md) - Practice exercises
   - [SESSION-OUTLINE.md](SESSION-OUTLINE.md) - Full training outline

3. **Advanced Topics (Later):**
   - [MCP-GUIDE.md](MCP-GUIDE.md) - Connect AI to external tools
   - [SKILLS.md](SKILLS.md) - Create custom agent skills
   - [MARKDOWN-GUIDE.md](MARKDOWN-GUIDE.md) - Advanced AI prompting

---

## 📝 Session Checklist

Use this during the session to track progress:

**Setup:**
- [ ] VS Code installed
- [ ] Extensions installed
- [ ] AI assistants authenticated

**Configuration:**
- [ ] AGENTS.md created
- [ ] Settings optimized
- [ ] Terminal configured

**Practice:**
- [ ] Shortcuts practiced
- [ ] AI coding exercise completed
- [ ] Git commit made

**Ready to Code:**
- [ ] Environment feels comfortable
- [ ] AI assistants respond correctly
- [ ] Know where to find help (this folder)

---

## 💡 Tips for Today

### For the Facilitator:
- **Go slow** - Better to master basics than rush through everything
- **Screen share** - Show each step clearly
- **Practice together** - Do exercises in real-time, not just demo
- **Check in frequently** - "Does this work for you?" "Any questions?"
- **Adapt** - If something isn't working, troubleshoot together

### For the Participant:
- **Ask questions** - No question is too basic
- **Follow along** - Do each step on your machine
- **Take notes** - Jot down useful shortcuts or tips
- **Experiment** - Try variations of what we show
- **Save this folder** - Reference it after the session

---

## 🔧 Troubleshooting Guide

### If Extensions Won't Install:
1. Check internet connection
2. Restart VS Code
3. Try installing from command line: `code --install-extension <extension-id>`

### If AI Assistants Won't Authenticate:
1. Check you're signed into the right account
2. Verify API access/permissions
3. Try signing out and back in
4. Restart VS Code

### If Terminal Doesn't Work:
1. Check default shell settings
2. Restart VS Code
3. Try a different shell type

### If Shortcuts Don't Work:
1. Check for keyboard shortcut conflicts
2. On Mac: Cmd vs Ctrl
3. Open Keyboard Shortcuts: `Cmd/Ctrl + K, Cmd/Ctrl + S`

---

## 📊 Success Criteria

**By the end of this hour, you should be able to:**
- [ ] Open files quickly without using the mouse
- [ ] Ask AI assistants to help write code
- [ ] Format and edit code efficiently
- [ ] Make commits through VS Code
- [ ] Know where to find answers (this folder)

**Most importantly:**
- [ ] Feel confident to start coding in VS Code today
- [ ] Know how to get unstuck if something doesn't work
- [ ] Have a foundation to build on

---

## 🎉 After the Session

**Immediate Actions:**
1. Try writing a simple program using what we learned
2. Create AGENTS.md for another project
3. Practice the 5 shortcuts we covered

**This Week:**
- Code for at least 30 minutes with your new setup
- Try asking AI to help with a real task
- Explore one more extension from [EXTENSIONS.md](EXTENSIONS.md)

**Stay Connected:**
- This repo is your reference - come back anytime
- Try the exercises in [EXERCISES.md](EXERCISES.md)
- Share what you learn!

---

**Remember:** This is just the beginning. You now have a professional dev environment. The more you use it, the more powerful it becomes. Don't try to learn everything today - just get comfortable with the basics and build from there.

**Let's build something great!** 🚀
