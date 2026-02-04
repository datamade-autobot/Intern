# Live VS Code Power Hour - Today's Session

**Session Type:** Understanding Agentic IDE Architecture
**Duration:** 60 minutes (1:00 PM - 2:00 PM)
**Format:** Conceptual overview with live configuration examples
**Prerequisites:** Computer with VS Code installed

---

## 🎯 Today's Goals

By the end of this session, you'll understand:
1. ✅ VS Code as an agentic development platform (not just an editor)
2. ✅ How AI agents work within VS Code and how to configure them
3. ✅ The extension ecosystem and how to choose the right tools
4. ✅ MCP (Model Context Protocol) and why it matters
5. ✅ Skills and how they extend AI capabilities
6. ✅ Rules files (CLAUDE.md, AGENTS.md) and their role in guiding AI behavior

---

## ⏱️ Session Timeline

### **Segment 1: VS Code as an Agentic Platform (15 mins) - 1:00-1:15**

#### 1.1 The Paradigm Shift (5 mins)

**Traditional IDE vs Agentic IDE:**

**Traditional IDE:**
- Code editor + debugging tools
- You write all the code
- Static extensions and features

**Agentic IDE:**
- AI-powered development platform
- AI collaborates with you to write code
- Dynamic, context-aware assistance
- Extensible through MCP, Skills, and Rules

**Key Concept:** VS Code becomes a platform where AI agents understand your project through configuration files and enhance your workflow through connected tools.

#### 1.2 The Architecture Stack (10 mins)

**Understanding the Layers:**

```
┌─────────────────────────────────────┐
│  YOUR PROJECT CODE                  │  ← What you're building
├─────────────────────────────────────┤
│  RULES FILES                        │  ← How AI should behave
│  (CLAUDE.md, AGENTS.md, etc.)      │
├─────────────────────────────────────┤
│  SKILLS                             │  ← Reusable AI capabilities
│  (Custom commands & workflows)      │
├─────────────────────────────────────┤
│  MCP SERVERS                        │  ← External tool connections
│  (GitHub, databases, APIs)          │
├─────────────────────────────────────┤
│  EXTENSIONS                         │  ← IDE capabilities
│  (Claude Code, Copilot, ESLint)    │
├─────────────────────────────────────┤
│  VS CODE                            │  ← Base platform
└─────────────────────────────────────┘
```

**What Each Layer Does:**
- **VS Code:** Foundation - editor, terminal, git integration
- **Extensions:** Add capabilities (AI assistants, linters, formatters)
- **MCP Servers:** Connect AI to external data (GitHub PRs, databases, file systems)
- **Skills:** Teach AI specialized workflows (deploy process, testing strategies)
- **Rules Files:** Guide AI behavior for your specific project
- **Your Code:** What you build with all these tools

**Checkpoint:** Understand the architecture layers ✓

---

### **Segment 2: Extensions - Building Your Toolkit (12 mins) - 1:15-1:27**

#### 2.1 Extension Categories & Selection (7 mins)

**The Five Categories:**

**1. AI Assistants** (Choose 1-2)
- **Claude Code** - Best for: Complex reasoning, refactoring, system design
- **GitHub Copilot** - Best for: Autocomplete, boilerplate, common patterns
- **Cursor** - Best for: Multi-file edits, codebase-wide changes

**When to use which:**
- Claude Code: "Explain this architecture" or "Refactor this class"
- Copilot: Inline suggestions while typing
- Both together: Copilot for speed, Claude for thinking

**2. Code Quality** (Essential)
- **Prettier** - Automatic code formatting
- **ESLint** - JavaScript/TypeScript linting
- **Error Lens** - See errors inline (not just in sidebar)

**Why they matter:** Maintain consistency without thinking about it.

**3. Language Support** (Based on your stack)
- **Python:** Python + Pylance
- **JavaScript/TypeScript:** Built-in
- **Go:** Official Go extension
- **Rust:** rust-analyzer

**4. Git & Collaboration**
- **GitLens** - See who changed what, when, why
- Visualize code history inline

**5. Productivity Enhancers**
- **Path Intellisense** - Autocomplete file paths
- **Auto Rename Tag** - Keep HTML/JSX tags in sync
- **Markdown Preview** - View markdown files rendered

#### 2.2 Extension Strategy (5 mins)

**The Progressive Installation Approach:**

**Week 1: Core Setup**
```
✓ Claude Code or Copilot
✓ Language support for your primary language
✓ GitLens
```

**Week 2: Code Quality**
```
✓ Prettier
✓ ESLint (if using JS/TS)
✓ Error Lens
```

**Week 3+: Optimize**
```
✓ Productivity tools as needed
✓ Language-specific tools as you use them
```

**Key Principle:** Don't install everything at once. Add extensions when you feel friction without them.

**Live Demo:** Quick tour of installed extensions and what they do.

**Checkpoint:** Understand extension categories and selection strategy ✓

---

### **Segment 3: Rules Files - Teaching AI About Your Project (15 mins) - 1:27-1:42**

#### 3.1 The Rules File Hierarchy (5 mins)

**Understanding the Files:**

| File | Scope | Read By | Purpose |
|------|-------|---------|---------|
| `CLAUDE.md` | Project | Claude Code | Claude-specific rules |
| `AGENTS.md` | Project | All AI agents | Universal instructions |
| `.cursorrules` | Project | Cursor | Cursor-specific rules |
| `copilot-instructions.md` | Project | GitHub Copilot | Copilot guidance |
| `README.md` | Project | Humans & AI | Project overview |

**Key Insight:** These files are like onboarding documents for your AI pair programmer.

#### 3.2 Anatomy of an Effective Rules File (10 mins)

**What to Include:**

**1. Project Context** (Essential)
```markdown
## Project Context
This is a REST API for e-commerce order management.
Built for internal use by the warehouse team.
Handles ~10k orders per day.
```

**Why:** AI needs to know WHAT this is and WHO uses it.

**2. Tech Stack** (Essential)
```markdown
## Stack
- Node.js 20 LTS
- Express.js 4.x
- PostgreSQL 15
- Redis for caching
- Deployed on AWS ECS
```

**Why:** AI makes better suggestions when it knows your exact versions and constraints.

**3. Code Style** (Important)
```markdown
## Code Style
- Use async/await, no callbacks
- Prefer functional programming patterns
- All functions must have JSDoc comments
- Use TypeScript strict mode
```

**Why:** Consistency matters. AI will follow your preferences.

**4. Common Commands** (Helpful)
```markdown
## Commands
- Run tests: `npm test`
- Start dev: `npm run dev`
- Build: `npm run build`
- Deploy: `npm run deploy:staging`
```

**Why:** AI can help you run the right commands at the right time.

**5. Important Gotchas** (Critical)
```markdown
## Important Notes
- Never commit .env files
- Database migrations must be reversible
- API has rate limits: 100 req/min
- Use transactions for multi-table updates
```

**Why:** Prevent common mistakes and violations of your constraints.

**Live Example:** We'll look at a real AGENTS.md file together.

**Checkpoint:** Understand what makes a good rules file ✓

---

### **Segment 4: MCP & Skills - Extending AI Capabilities (13 mins) - 1:42-1:55**

#### 4.1 MCP (Model Context Protocol) Explained (7 mins)

**What is MCP?**

MCP lets AI agents connect to external tools and data sources. Think of it as "API access for AI."

**Without MCP:**
```
You: "What's the status of PR #123?"
AI: "I don't have access to GitHub. You'll need to check manually."
```

**With MCP:**
```
You: "What's the status of PR #123?"
AI: *connects to GitHub via MCP*
AI: "PR #123 is approved by 2 reviewers, has 3 passing checks,
     ready to merge. Last updated 2 hours ago."
```

**Common MCP Servers:**

**1. GitHub MCP**
- Read/write PRs and issues
- Check CI/CD status
- Review code changes

**2. Filesystem MCP**
- Search across large codebases
- Read files outside current workspace
- Find patterns across multiple projects

**3. Database MCP**
- Query database schema
- Run safe SELECT queries
- Understand data models

**4. Slack/Discord MCP**
- Search team discussions
- Post updates
- Get context from conversations

**When to Use MCP:**
- Your project spans multiple repositories
- You need to query databases or APIs
- You want AI to access external documentation
- You have custom internal tools

**Configuration Example:**
```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_TOKEN": "your-token"
      }
    }
  }
}
```

**Live Demo:** Show MCP configuration and what it looks like in action.

**Checkpoint:** Understand what MCP is and when to use it ✓

#### 4.2 Skills - Reusable AI Workflows (6 mins)

**What are Skills?**

Skills are pre-defined workflows or knowledge sets you teach AI agents.

**Think of Skills as:**
- Specialized training for common tasks
- Shortcuts for complex operations
- Domain-specific knowledge

**Types of Skills:**

**1. Workflow Skills**
```yaml
name: deploy-staging
description: Deploy to staging environment
steps:
  - Run tests
  - Build production bundle
  - Deploy to staging
  - Run smoke tests
  - Post to Slack
```

**Use case:** Complex multi-step processes you do often.

**2. Knowledge Skills**
```yaml
name: company-api-conventions
description: Our REST API design standards
knowledge:
  - Always version endpoints (/api/v1/...)
  - Use plural nouns for resources
  - Return 422 for validation errors
  - Include request ID in all responses
```

**Use case:** Company-specific conventions and standards.

**3. Analysis Skills**
```yaml
name: security-review
description: Check code for security issues
checks:
  - SQL injection vulnerabilities
  - XSS vulnerabilities
  - Exposed secrets
  - Missing authentication
```

**Use case:** Domain-specific code review checklists.

**How to Use Skills:**

In Claude Code: `/deploy-staging`
In Copilot: `@workspace deploy to staging`

**When to Create Skills:**
- You do the same workflow 3+ times
- You have company-specific knowledge to encode
- You want consistency across your team

**Checkpoint:** Understand what Skills are and when to create them ✓

---

### **Segment 5: Putting It All Together (5 mins) - 1:55-2:00**

#### 5.1 The Agentic IDE Workflow (3 mins)

**Your Daily Workflow:**

**Morning:**
1. Open VS Code
2. AI reads your AGENTS.md and understands the project
3. Connected to external tools via MCP
4. Skills available for common tasks

**During Development:**
1. Write code with AI autocomplete (Copilot)
2. Ask architectural questions (Claude Code)
3. Use skills for deployments: `/deploy-staging`
4. AI accesses GitHub PRs via MCP
5. AI follows your code style from AGENTS.md

**Benefits:**
- AI understands YOUR project, not generic code
- Connected to YOUR tools (GitHub, databases, etc.)
- Follows YOUR conventions and standards
- Automates YOUR workflows

#### 5.2 Next Steps & Resources (2 mins)

**Immediate Actions:**
1. Review the extension list: [EXTENSIONS.md](EXTENSIONS.md)
2. Study rules file examples: [01-rules-files/](01-rules-files/)
3. Read MCP guide when ready: [MCP-GUIDE.md](MCP-GUIDE.md)
4. Explore skills: [SKILLS.md](SKILLS.md)

**This Week:**
- Create an AGENTS.md for your current project
- Install 3-5 essential extensions
- Experiment with AI assistants using your rules file

**This Month:**
- Set up one MCP server (GitHub recommended)
- Create your first custom skill
- Optimize your configuration based on what works

**Advanced Resources:**
- [MARKDOWN-GUIDE.md](MARKDOWN-GUIDE.md) - Effective AI prompting
- [KEYBOARD-SHORTCUTS.md](KEYBOARD-SHORTCUTS.md) - Productivity shortcuts
- [EXERCISES.md](EXERCISES.md) - Hands-on practice

**Checkpoint:** Ready to build your agentic IDE ✓

---

## 📝 Understanding Checklist

Use this during the session to track comprehension:

**Architecture:**
- [ ] Understand the agentic IDE concept
- [ ] Can explain the architecture layers
- [ ] Know how AI agents read configuration

**Extensions:**
- [ ] Understand the 5 extension categories
- [ ] Know when to use Claude Code vs Copilot
- [ ] Have a progressive installation strategy

**Rules Files:**
- [ ] Understand what rules files do
- [ ] Know what to include in AGENTS.md
- [ ] Can explain why rules files matter

**Advanced Concepts:**
- [ ] Understand what MCP is and its purpose
- [ ] Know when to use MCP servers
- [ ] Understand Skills and their use cases

**Ready to Configure:**
- [ ] Can create an effective AGENTS.md
- [ ] Know which extensions to install first
- [ ] Understand the path to advanced features

---

## 💡 Tips for Today

### For the Facilitator:
- **Focus on concepts** - Understanding > Installation
- **Use analogies** - Relate to familiar concepts (APIs, configuration files, etc.)
- **Show examples** - Real AGENTS.md files, actual MCP configs
- **Check understanding** - "Can you explain this back to me?"
- **Connect the dots** - Show how pieces work together

### For the Participant:
- **Think architecturally** - How do these pieces connect?
- **Ask "why"** - Don't just accept "what" and "how"
- **Take notes** - Draw diagrams if it helps
- **Think about your projects** - How would you configure YOUR code?
- **Save this folder** - Reference when you're ready to implement

---

## 🧠 Key Mental Models

### The Onboarding Metaphor
Think of rules files (AGENTS.md, CLAUDE.md) as onboarding documents for a new team member. You wouldn't just say "figure it out" - you'd explain:
- What we're building
- Our tech stack
- Our coding standards
- Common commands
- Things to watch out for

AI agents need the same context.

### The Platform Metaphor
VS Code isn't just an editor - it's a platform:
- **Extensions** = Apps on your phone
- **MCP Servers** = APIs your apps can call
- **Skills** = Custom shortcuts/workflows
- **Rules Files** = User preferences/settings

### The Collaboration Metaphor
Traditional IDE: You're working alone
Agentic IDE: You have a pair programmer who:
- Knows your codebase (via rules files)
- Can access your tools (via MCP)
- Has specialized skills (via Skills)
- Adapts to your style (via configuration)

---

## 📊 Success Criteria

**By the end of this hour, you should be able to:**
- [ ] Explain what makes an IDE "agentic"
- [ ] Describe the architecture layers and how they interact
- [ ] Identify which extensions you need and why
- [ ] Explain what MCP is and when you'd use it
- [ ] Understand the role of rules files in guiding AI
- [ ] Know when to create a Skill vs write a rules file

**Most importantly:**
- [ ] Have a mental model of how agentic IDEs work
- [ ] Know what to configure first, second, and later
- [ ] Understand the path from basic to advanced usage
- [ ] Can create an effective AGENTS.md for your projects

---

## 🎉 After the Session

**Immediate Actions (Today):**
1. Create your first AGENTS.md for an actual project
2. Install 3-5 essential extensions based on your stack
3. Review the architecture diagram and make sure it clicks

**This Week:**
1. **Day 1-2:** Get comfortable with rules files
   - Create AGENTS.md for 2-3 projects
   - Experiment with what works

2. **Day 3-4:** Explore extensions
   - Install language-specific extensions
   - Try different AI assistants (Claude vs Copilot)
   - Find your preferred workflow

3. **Day 5-7:** Start using advanced features
   - Read [MCP-GUIDE.md](MCP-GUIDE.md) when you feel limited
   - Consider your first MCP server (GitHub recommended)
   - Think about Skills you'd want to create

**This Month:**
- Set up at least one MCP server
- Create your first custom Skill
- Refine your AGENTS.md based on what actually helps
- Share your learnings with your team

**Resources for Your Journey:**

**Immediate (This Week):**
- [EXTENSIONS.md](EXTENSIONS.md) - Choose your tools
- [01-rules-files/](01-rules-files/) - Study examples
- [KEYBOARD-SHORTCUTS.md](KEYBOARD-SHORTCUTS.md) - Get efficient

**Intermediate (This Month):**
- [MCP-GUIDE.md](MCP-GUIDE.md) - Connect external tools
- [SKILLS.md](SKILLS.md) - Create workflows
- [MARKDOWN-GUIDE.md](MARKDOWN-GUIDE.md) - Better prompting

**Advanced (Ongoing):**
- [SESSION-OUTLINE.md](SESSION-OUTLINE.md) - Deep dive reference
- [EXERCISES.md](EXERCISES.md) - Hands-on practice
- Community forums and docs for each tool

---

## 🎓 Final Thoughts

**The Progressive Journey:**

```
Week 1: Understanding
→ You are here after today's session
→ Know the concepts, see the architecture

Week 2-3: Basic Usage
→ Rules files working
→ Extensions installed
→ AI assistance in daily workflow

Month 2: Intermediate
→ MCP servers connected
→ Custom shortcuts and workflows
→ Optimized for your style

Month 3+: Advanced
→ Custom Skills created
→ Team-wide configurations
→ Teaching others
```

**Remember:**
- Understanding comes before implementation
- Start simple, add complexity as needed
- Every project might need different configuration
- The best setup is the one that matches YOUR workflow

**You now understand the architecture.** The rest is implementation and iteration.

**Go build amazing things!** 🚀
