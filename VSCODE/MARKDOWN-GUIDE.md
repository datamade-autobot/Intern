# Markdown in Agentic Coding

## Why Markdown Matters for AI Assistants

Markdown is the universal language for communicating with AI coding agents. It provides structure, clarity, and context that helps agents understand your intent better.

## Configuration Files

### CLAUDE.md vs AGENTS.md vs README.md

| File | Purpose | Read By | Scope |
|------|---------|---------|-------|
| `CLAUDE.md` | Claude-specific rules | Claude Code | Project-wide |
| `AGENTS.md` | Universal agent rules | All AI agents | Project-wide |
| `.cursorrules` | Cursor-specific rules | Cursor IDE | Project-wide |
| `copilot-instructions.md` | Copilot guidance | GitHub Copilot | Project-wide |
| `README.md` | Human documentation | Developers & AI | Project overview |

### When to Use Each

**CLAUDE.md:** Claude Code specific instructions
```markdown
# Project Rules for Claude

## Code Style
- Use TypeScript strict mode
- Prefer functional components in React
- Always add JSDoc comments to public APIs

## Testing
- Run `npm test` before committing
- Maintain 80% code coverage
```

**AGENTS.md:** Universal instructions for all AI agents
```markdown
# AI Agent Instructions

## Project Context
This is a Node.js REST API for user management.

## Stack
- Runtime: Node.js 20
- Framework: Express
- Database: PostgreSQL
- ORM: Prisma

## Guidelines
- Follow REST conventions
- Use async/await, no callbacks
- Validate all inputs
```

**.cursorrules:** Cursor IDE specific
```markdown
# Cursor Rules

Always use the workspace's ESLint configuration.
Prefer shorter, more focused functions.
Use descriptive variable names.
```

## Markdown Best Practices

### 1. **Use Hierarchical Headers**

```markdown
# Main Topic (H1)
## Subtopic (H2)
### Details (H3)
```

AI agents use headers to understand document structure.

### 2. **Code Blocks with Language Tags**

```markdown
```typescript
const greet = (name: string): string => {
  return `Hello, ${name}!`;
};
```
```

This helps agents understand context and provide better suggestions.

### 3. **Lists for Instructions**

```markdown
## Deployment Steps
1. Run tests
2. Build the project
3. Deploy to staging
4. Verify health checks
5. Deploy to production
```

Numbered lists = sequential steps. Bulleted lists = unordered items.

### 4. **Tables for Structured Data**

```markdown
| Environment | URL | Database |
|-------------|-----|----------|
| Development | localhost:3000 | dev_db |
| Staging | staging.example.com | staging_db |
| Production | example.com | prod_db |
```

### 5. **Emphasis for Importance**

```markdown
**IMPORTANT:** Never commit `.env` files
*Note:* This applies to all environments
```

## Document Structure for AI Agents

### Optimal Structure

```markdown
# Project Name

## Overview
Brief description of what this is

## Context
Who, what, why this project exists

## Architecture
High-level system design

## Stack & Dependencies
Technologies used

## Development Guidelines
Coding standards and practices

## Common Tasks
Frequently performed operations

## Gotchas & Known Issues
Things to watch out for

## Resources
Links to docs, wikis, etc.
```

### Real Example

```markdown
# E-Commerce API

## Overview
RESTful API for managing products, orders, and customers.

## Context
This API serves our mobile app and web storefront. Built by the Platform team.
Current version: 2.3.0

## Architecture
- Microservices architecture
- Event-driven with RabbitMQ
- Redis for caching
- PostgreSQL for persistence

## Stack & Dependencies
- **Runtime:** Node.js 20 LTS
- **Framework:** NestJS 10
- **Database:** PostgreSQL 15
- **Cache:** Redis 7
- **Queue:** RabbitMQ 3.12

## Development Guidelines

### Code Style
- Use TypeScript strict mode
- Follow NestJS conventions
- DTOs for all API inputs/outputs
- Use dependency injection

### Testing
- Unit tests for business logic
- Integration tests for APIs
- E2E tests for critical paths
- Minimum 80% coverage

### API Design
- RESTful conventions
- Versioned endpoints (`/api/v2/...`)
- Consistent error responses
- Paginate list endpoints

## Common Tasks

### Run Tests
```bash
npm test                 # Unit tests
npm run test:e2e        # E2E tests
npm run test:cov        # Coverage report
```

### Database Migrations
```bash
npm run migration:generate -- <name>
npm run migration:run
```

### Start Development Server
```bash
npm run start:dev
```

## Gotchas & Known Issues

- **Rate Limiting:** API has rate limits (100 req/min per IP)
- **Database Transactions:** Use Prisma's interactive transactions, not sequential
- **Caching:** Redis keys expire after 1 hour by default
- **Authentication:** JWT tokens expire in 24 hours

## Resources

- [API Documentation](https://docs.example.com)
- [Architecture Diagrams](https://wiki.example.com/arch)
- [Runbook](https://wiki.example.com/runbook)
```

## Agent-Friendly Patterns

### ✅ DO: Be Explicit

```markdown
## Authentication
This project uses JWT tokens. Tokens are issued by the AuthService
and validated by the AuthMiddleware. Token expiry is 24 hours.
Refresh tokens last 7 days.
```

### ❌ DON'T: Be Vague

```markdown
## Auth
Uses JWT
```

### ✅ DO: Provide Examples

```markdown
## Error Handling

All errors should use our custom ErrorResponse format:

```typescript
throw new AppError({
  code: 'USER_NOT_FOUND',
  message: 'User with ID 123 does not exist',
  statusCode: 404
});
```
```

### ❌ DON'T: Just State Rules

```markdown
## Error Handling
Use proper error codes
```

### ✅ DO: Link to Resources

```markdown
See the [API Documentation](./docs/api.md) for endpoint details.
```

### ❌ DON'T: Leave Agents Searching

```markdown
Check the API docs
```

## Markdown Everywhere

### Code Comments
```typescript
/**
 * Calculates the total price including tax
 *
 * @param subtotal - The pre-tax amount
 * @param taxRate - Tax rate as decimal (0.08 = 8%)
 * @returns Total price with tax included
 */
function calculateTotal(subtotal: number, taxRate: number): number {
  return subtotal * (1 + taxRate);
}
```

### Commit Messages
```
feat: add user authentication

Implements JWT-based authentication with:
- Login endpoint
- Token validation middleware
- Refresh token support

Closes #123
```

### Pull Requests
```markdown
## Summary
Adds Redis caching layer to product API

## Changes
- Added Redis client configuration
- Implemented cache-aside pattern
- Added cache invalidation on updates

## Testing
- Unit tests for cache service
- Integration tests with Redis
- Load tested with 1000 req/s

## Performance Impact
- Reduced average response time from 200ms to 50ms
- 75% reduction in database queries
```

## VS Code Markdown Features

### Preview
- `Cmd/Ctrl + Shift + V` - Open markdown preview
- `Cmd/Ctrl + K V` - Preview side-by-side

### Navigation
- `Cmd/Ctrl + Click` on header - Jump to section
- Outline view shows document structure

### Extensions
- **Markdown All in One** - Shortcuts and formatting
- **Markdown Preview Enhanced** - Advanced preview
- **markdownlint** - Linting and style checking

## Quick Reference

### Headers
```markdown
# H1
## H2
### H3
```

### Emphasis
```markdown
**bold**
*italic*
***bold italic***
`code`
~~strikethrough~~
```

### Lists
```markdown
- Bullet
- List

1. Numbered
2. List

- [ ] Task list
- [x] Completed task
```

### Links & Images
```markdown
[Link text](https://example.com)
![Alt text](image.png)
```

### Code
```markdown
Inline `code`

```language
Code block
```
```

### Blockquotes
```markdown
> Quote
> Multiple lines
```

### Tables
```markdown
| Header 1 | Header 2 |
|----------|----------|
| Cell 1   | Cell 2   |
```

## Resources

- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Flavored Markdown](https://github.github.com/gfm/)
- [VS Code Markdown Docs](https://code.visualstudio.com/docs/languages/markdown)

---

**Remember:** Good markdown documentation is an investment. It helps both humans and AI agents understand your project, leading to better code suggestions and fewer mistakes.
