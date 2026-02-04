# VS Code Power Hour - Session Outline

**Date:** Wednesday, February 4th, 2026
**Time:** 1:00 PM - 2:00 PM
**Facilitator:** Taylor
**Participant:** Nate
**Level:** Beginner Foundation

---

## Session Goals

By the end of this hour, Nate will:
1. Understand VS Code as an agentic coding environment
2. Have a working setup with AI assistants configured
3. Know essential shortcuts and workflows
4. Understand configuration files (CLAUDE.md, AGENTS.md, etc.)
5. Be able to leverage AI effectively in daily work

---

## Pre-Session Checklist (5 mins before)

- [ ] Nate has VS Code installed
- [ ] Screen sharing setup and tested
- [ ] This repository cloned to Nate's machine
- [ ] Recording started (for reference)

---

## Session Agenda

### 1. Introduction & Context (5 mins) - 1:00-1:05

**Key Points:**
- VS Code is not just an editor, it's a platform for AI-assisted development
- We'll set up tools, not just learn features
- Focus on building good habits from day one
- This is a foundation - you'll discover more as you code

**Discussion:**
- What programming languages will you use most?
- Have you used any AI coding tools before?
- What's your biggest pain point when coding?

---

### 2. VS Code Fundamentals (10 mins) - 1:05-1:15

#### A. Interface Tour (3 mins)
- Activity Bar (left side)
- Side Bar (Explorer, Search, Source Control)
- Editor area (where code lives)
- Panel (Terminal, Problems, Output)
- Status Bar (bottom)

**Key Shortcuts to Demo:**
- `Cmd/Ctrl + P` - Quick Open
- `Cmd/Ctrl + Shift + P` - Command Palette
- `Cmd/Ctrl + B` - Toggle sidebar
- `Cmd/Ctrl + J` - Toggle panel

#### B. Essential Shortcuts (7 mins)

**Live Demo - "Follow Along":**

1. **File Navigation**
   ```
   Cmd/Ctrl + P → Type "AGENTS" → Open file
   ```

2. **Multi-Cursor Editing**
   ```
   1. Select "TODO"
   2. Cmd/Ctrl + D (multiple times)
   3. Type new text
   ```

3. **Line Manipulation**
   ```
   Alt + Up/Down → Move line
   Cmd/Ctrl + / → Comment/uncomment
   ```

4. **Search & Replace**
   ```
   Cmd/Ctrl + F → Find
   Cmd/Ctrl + H → Replace
   Cmd/Ctrl + Shift + F → Search all files
   ```

**Practice:** [EXERCISES.md](EXERCISES.md) - Exercise 1

---

### 3. Installing Essential Extensions (8 mins) - 1:15-1:23

#### Extensions to Install (Live Demo)

**AI Assistants:**
1. **Claude Code** or **Cursor**
   - Open Extensions (`Cmd/Ctrl + Shift + X`)
   - Search "Claude Code"
   - Click Install
   - Authenticate

2. **GitHub Copilot** (if available)
   - Search "GitHub Copilot"
   - Install
   - Sign in with GitHub

**Developer Productivity:**
3. **GitLens** - Git supercharged
4. **Prettier** - Code formatter
5. **ESLint** - Code linting
6. **Error Lens** - Inline error display
7. **Auto Rename Tag** - HTML/XML tag renaming
8. **Path Intellisense** - Autocomplete file paths

**Language Specific:**
- **Python:** Python + Pylance
- **JavaScript/TypeScript:** (built-in, no extension needed)
- **Go:** Go
- **Rust:** rust-analyzer
- **Java:** Extension Pack for Java

**Pro Tip:** Open [EXTENSIONS.md](EXTENSIONS.md) and install as needed.

---

### 4. Configuring AI Assistants (12 mins) - 1:23-1:35

#### A. Understanding Configuration Files (5 mins)

**Whiteboard/Discussion:**
```
Your Project
├── CLAUDE.md              ← Claude Code reads this
├── AGENTS.md              ← All AI agents read this
├── .cursorrules           ← Cursor reads this
├── copilot-instructions.md ← Copilot reads this
└── README.md              ← Humans & AI read this
```

**Key Concept:** These files guide AI behavior in your project.

#### B. Create Your First AGENTS.md (7 mins)

**Live Demo - "Code Along":**

1. Create new file: `AGENTS.md`
2. Add basic structure:

```markdown
# AI Agent Instructions

## Project Context
[Describe what you're building]

## Stack
[Your technologies]

## Code Style
[Your preferences]
```

3. Example for a Python project:

```markdown
# AI Agent Instructions

## Project Context
This is a Python CLI tool for file management.

## Stack
- Python 3.11
- Click for CLI
- pytest for testing

## Code Style
- Use type hints
- Follow PEP 8
- Write docstrings for all functions
- Prefer pathlib over os.path

## Testing
Run tests before committing: `pytest`
```

**Practice:** [EXERCISES.md](EXERCISES.md) - Exercise 2

---

### 5. Using AI Assistants Effectively (12 mins) - 1:35-1:47

#### A. Chat vs Inline Chat (3 mins)

**Demo:**

1. **Chat Panel** (`Cmd/Ctrl + Shift + I`)
   - For questions
   - For planning
   - For research

2. **Inline Chat** (`Cmd/Ctrl + I`)
   - For editing specific code
   - For quick changes
   - Context-aware

#### B. Writing Good Prompts (4 mins)

**Good vs Bad Examples:**

❌ **Bad:** "fix this"
✅ **Good:** "This function throws a KeyError. Can you add error handling to return None if the key doesn't exist?"

❌ **Bad:** "make it better"
✅ **Good:** "Refactor this function to use list comprehension instead of a for loop for better readability"

❌ **Bad:** "add tests"
✅ **Good:** "Add pytest tests for the parse_config function, covering valid input, missing keys, and invalid JSON"

**Key Principles:**
1. Be specific
2. Provide context
3. Explain the "why"
4. Mention constraints

#### C. Live Coding Demo (5 mins)

**Scenario:** "Let's write a simple function together using AI"

1. Open chat
2. Prompt: "Write a Python function that takes a list of numbers and returns the sum of even numbers only. Include type hints and a docstring."
3. Review generated code
4. Ask for tests: "Now write pytest tests for this function"
5. Ask for improvement: "Can you add error handling for non-numeric inputs?"

**Key Takeaway:** Iterate with AI, don't accept first output blindly.

---

### 6. Terminal & Git Basics (8 mins) - 1:47-1:55

#### A. Integrated Terminal (3 mins)

**Demo:**
- `` Ctrl + ` `` - Toggle terminal
- `Cmd/Ctrl + Shift + `` - New terminal
- Split terminal
- Multiple shell types (bash, zsh, powershell)

**Common Commands:**
```bash
# Navigate
cd projects/my-app

# List files
ls -la

# Run code
python main.py
npm start

# Install dependencies
pip install requests
npm install express
```

#### B. Git in VS Code (5 mins)

**Demo:**

1. **Source Control View** (`Cmd/Ctrl + Shift + G`)

2. **Make a change:**
   - Edit a file
   - See changes in Source Control
   - Stage changes (+ icon)
   - Write commit message
   - Commit

3. **Using GitLens:**
   - Line blame
   - File history
   - Compare changes

4. **AI-Assisted Commits:**
   ```
   Claude: "Review my changes and suggest a commit message"
   ```

**Practice:** [EXERCISES.md](EXERCISES.md) - Exercise 3

---

### 7. MCP Servers (Optional Advanced Topic) (5 mins) - 1:55-2:00

**Quick Overview:**

MCP (Model Context Protocol) gives AI agents superpowers:
- File system access
- Database queries
- API calls
- Tool execution

**Example Use Cases:**
- Read project files beyond chat context
- Query your database schema
- Interact with GitHub APIs
- Execute custom scripts

**For Later:** See [MCP-GUIDE.md](MCP-GUIDE.md) when you're ready to explore.

**When to revisit:**
- When you need AI to access external data
- When you have repetitive workflows
- When building custom tooling

---

### 8. Wrap-Up & Next Steps (5 mins) - 2:00-2:05

#### Quick Recap
- [ ] VS Code interface & shortcuts
- [ ] Essential extensions installed
- [ ] AI assistants configured
- [ ] Created AGENTS.md
- [ ] Know how to prompt AI effectively
- [ ] Comfortable with terminal & git

#### Immediate Action Items for Nate

**Today:**
1. Review [KEYBOARD-SHORTCUTS.md](KEYBOARD-SHORTCUTS.md)
2. Pick 3 shortcuts to master this week
3. Complete remaining exercises in [EXERCISES.md](EXERCISES.md)

**This Week:**
1. Create AGENTS.md for your first project
2. Use AI for at least one task per day
3. Try inline chat vs panel chat
4. Experiment with different prompting styles

**This Month:**
1. Explore [EXTENSIONS.md](EXTENSIONS.md) for your stack
2. Customize keyboard shortcuts
3. Read [MARKDOWN-GUIDE.md](MARKDOWN-GUIDE.md) for documentation
4. When ready: Setup MCP servers [MCP-GUIDE.md](MCP-GUIDE.md)

#### Resources

**Bookmarks:**
- [VS Code Docs](https://code.visualstudio.com/docs)
- [Claude Code Docs](https://code.claude.com)
- [GitHub Copilot Docs](https://docs.github.com/copilot)
- This VSCODE folder (reference guide)

#### Questions?

Open floor for any questions or topics to revisit.

---

## Facilitator Notes

### Timing Tips
- Stay flexible - adjust based on Nate's pace
- Skip MCP section if running late
- Prioritize hands-on over theory
- Use exercises to reinforce learning

### Common Questions

**"Which AI assistant should I use?"**
- All have strengths
- Try Claude Code for starting out
- Use Copilot for autocomplete
- Switch based on task

**"Do I need to memorize all shortcuts?"**
- No! Learn 2-3 per week
- Focus on what you use most
- Muscle memory takes time

**"What if AI generates wrong code?"**
- Always review before accepting
- Test the code
- Ask AI to explain its reasoning
- Use AI as a partner, not oracle

### Troubleshooting

**Extensions won't install:**
- Check internet connection
- Restart VS Code
- Check extension marketplace status

**AI assistant not responding:**
- Check authentication
- Verify API keys
- Check network/firewall
- Restart VS Code

**Terminal not working:**
- Check default shell settings
- Verify PATH environment
- Try different shell (bash/zsh/powershell)

### Follow-Up

**After Session:**
- Send recording link
- Share this repository
- Schedule 30-min check-in next week
- Create Slack/Discord channel for questions

**One Week Check-In Questions:**
- What shortcuts are you using?
- How often are you using AI?
- What's been most helpful?
- What's still confusing?
- Any workflow pain points?

---

## Success Metrics

Nate should be able to:
- [ ] Open files quickly with Cmd/Ctrl + P
- [ ] Use Command Palette for any action
- [ ] Chat with AI assistant to solve problems
- [ ] Make commits through VS Code
- [ ] Know where to find documentation (this folder)
- [ ] Feel confident to start coding with AI assistance

---

**Remember:** This is a foundation. The goal is confidence, not mastery. Nate will learn more by doing than by watching. Keep it interactive!
