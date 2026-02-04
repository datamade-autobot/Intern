# MCP (Model Context Protocol) Guide

MCP is how AI agents connect to external tools, databases, and APIs. Think of it as "plugins for AI."

---

## 🧠 What is MCP?

**Model Context Protocol (MCP)** is an open standard that lets AI models:
- Access external data (files, databases, APIs)
- Execute tools (run commands, query services)
- Interact with your development environment

Without MCP, AI can only see what you paste into the chat. With MCP, AI can:
- Read your GitHub PRs directly
- Query your database
- Access your company's internal tools
- Interact with Slack, Notion, Linear, etc.

---

## 🔌 How MCP Works

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   VS Code   │────▶│ MCP Server  │────▶│  External   │
│  (AI Agent) │◀────│  (Bridge)   │◀────│   Service   │
└─────────────┘     └─────────────┘     └─────────────┘
```

1. **AI Agent** (Claude Code, Copilot) needs external data
2. **MCP Server** translates the request
3. **External Service** (GitHub, database, etc.) provides data
4. Response flows back to the AI

---

## 🚀 Setting Up MCP in VS Code

### Method 1: Via Command Palette
```
Cmd+Shift+P → "MCP: Add Server"
```
Follow the prompts to configure.

### Method 2: Via settings.json
Add to your VS Code `settings.json`:

```json
{
  "mcp.servers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "${env:GITHUB_TOKEN}"
      }
    }
  }
}
```

### Method 3: Claude Code CLI
```bash
# List current MCP servers
claude /mcp

# Add a server via Claude Code
claude mcp add github
```

---

## 📦 Popular MCP Servers

### Development Tools
| Server | Purpose | Install |
|--------|---------|---------|
| **GitHub** | PRs, issues, repos | `npx @modelcontextprotocol/server-github` |
| **GitLab** | GitLab integration | `npx @modelcontextprotocol/server-gitlab` |
| **Filesystem** | Local file access | `npx @modelcontextprotocol/server-filesystem` |

### Databases
| Server | Purpose | Install |
|--------|---------|---------|
| **PostgreSQL** | Query Postgres | `npx @modelcontextprotocol/server-postgres` |
| **SQLite** | Local SQLite DBs | `npx @modelcontextprotocol/server-sqlite` |

### Productivity
| Server | Purpose | Install |
|--------|---------|---------|
| **Slack** | Slack messages | `npx @modelcontextprotocol/server-slack` |
| **Google Drive** | Doc access | `npx @modelcontextprotocol/server-gdrive` |
| **Notion** | Notion pages | `npx @modelcontextprotocol/server-notion` |

### Documentation
| Server | Purpose | Install |
|--------|---------|---------|
| **Fetch** | Web page content | `npx @modelcontextprotocol/server-fetch` |
| **Brave Search** | Web search | `npx @modelcontextprotocol/server-brave-search` |

---

## 📝 Example Configuration

Here's a complete `mcp-config.json` for common development workflows:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/path/to/allowed/directory"
      ]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_xxxxxxxxxxxx"
      }
    },
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres"],
      "env": {
        "DATABASE_URL": "postgresql://user:pass@localhost:5432/mydb"
      }
    }
  }
}
```

---

## 🔐 Security Best Practices

### DO
- ✅ Use environment variables for secrets
- ✅ Limit filesystem access to specific directories
- ✅ Use read-only tokens when possible
- ✅ Audit which MCP servers you have installed
- ✅ Only install servers from trusted sources

### DON'T
- ❌ Hardcode API keys in config files
- ❌ Give filesystem access to your entire drive
- ❌ Install random MCP servers from the internet
- ❌ Share config files containing secrets

---

## 🔧 Troubleshooting

### Check Server Status
```bash
# In VS Code
Cmd+Shift+P → "MCP: List Servers" → Select server → "Show Output"
```

### Common Issues

**"Server not found"**
- Check the package name is correct
- Ensure Node.js/npx is installed
- Try running the npx command directly in terminal

**"Authentication failed"**
- Verify your token is correct
- Check token has required permissions
- Ensure environment variable is set

**"Connection timeout"**
- Check if external service is reachable
- Verify firewall isn't blocking
- Try restarting VS Code

---

## 🎯 Practical Examples

### Example 1: Review a GitHub PR
With GitHub MCP configured:
```
You: Review PR #456 in my-repo
Claude: [Fetches PR via MCP, analyzes code, provides review]
```

### Example 2: Query Database
With PostgreSQL MCP configured:
```
You: Show me users who signed up last week
Claude: [Runs SELECT query, returns results]
```

### Example 3: Search Codebase
With Filesystem MCP configured:
```
You: Find all uses of the deprecated `oldFunction`
Claude: [Searches files, reports locations]
```

---

## 📚 Resources

- [Official MCP Documentation](https://modelcontextprotocol.io/)
- [VS Code MCP Guide](https://code.visualstudio.com/docs/copilot/customization/mcp-servers)
- [MCP Server Registry](https://github.com/modelcontextprotocol/servers)
- [Claude Code MCP Docs](https://code.claude.com/docs/en/mcp)

---

## 🏃 Quick Start Checklist

1. [ ] Install Node.js if not already installed
2. [ ] Create a GitHub Personal Access Token
3. [ ] Add GitHub MCP server to VS Code
4. [ ] Test with "List open PRs in [repo]"
5. [ ] Explore other servers based on your workflow
