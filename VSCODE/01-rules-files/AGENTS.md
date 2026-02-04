# AGENTS.md - Universal AI Agent Instructions

This file provides instructions for ANY AI coding agent (Claude Code, GitHub Copilot, Cursor, etc.). VS Code applies these instructions automatically to all chat requests.

---

## Core Principles

### Code Quality
- Write clean, readable, maintainable code over clever one-liners
- Every change must pass typechecking, linting, and tests
- Add or update tests when modifying functionality
- Follow existing patterns in the codebase

### Communication
- Explain your reasoning for non-obvious decisions
- Ask clarifying questions when requirements are ambiguous
- Break complex tasks into smaller, reviewable steps
- Summarize what you changed after completing a task

### Safety
- Never delete files without explicit confirmation
- Don't modify environment variables or secrets
- Preserve existing functionality when refactoring
- Create backups before destructive operations

---

## Behavioral Guidelines

### DO
- ✅ Run tests after making changes
- ✅ Use existing utilities and helpers in the codebase
- ✅ Follow the project's established patterns
- ✅ Add helpful code comments for complex logic
- ✅ Consider edge cases and error handling
- ✅ Keep commits atomic and well-described

### DON'T
- ❌ Install new dependencies without asking
- ❌ Make assumptions about missing requirements
- ❌ Skip tests to save time
- ❌ Refactor unrelated code during a focused task
- ❌ Use deprecated APIs or patterns
- ❌ Leave console.log/print statements in production code

---

## Task Handling

### For New Features
1. Understand the requirement fully before coding
2. Check if similar functionality exists
3. Plan the implementation approach
4. Write tests first (TDD when appropriate)
5. Implement in small, testable increments
6. Document public APIs

### For Bug Fixes
1. Reproduce the bug first
2. Write a failing test that captures the bug
3. Fix the bug with minimal changes
4. Verify the test passes
5. Check for similar bugs elsewhere

### For Refactoring
1. Ensure comprehensive test coverage first
2. Make one type of change at a time
3. Verify tests pass after each change
4. Don't change behavior during refactoring

---

## Language-Specific Guidelines

### JavaScript/TypeScript
- Use strict TypeScript settings
- Prefer functional patterns over classes
- Use meaningful variable names
- Handle promises properly (no unhandled rejections)

### Python
- Use type hints consistently
- Follow PEP 8 naming conventions
- Use context managers for resources
- Prefer pathlib over os.path

### General
- Match the style of surrounding code
- Use consistent formatting (run Prettier/Black)
- Keep functions focused and testable
- Avoid magic numbers - use named constants

---

## Error Handling

- Always handle potential errors gracefully
- Provide meaningful error messages
- Log errors with appropriate context
- Don't swallow exceptions silently
- Use custom error types for domain-specific errors

---

## Performance Considerations

- Consider performance for frequently called code
- Avoid N+1 queries in database operations
- Cache expensive computations when appropriate
- Profile before optimizing - don't guess

---

## Security Reminders

- Never log sensitive data (passwords, tokens, PII)
- Validate all user input
- Use parameterized queries for databases
- Keep dependencies updated
- Follow the principle of least privilege

---

## When Uncertain

If you're unsure about:
- **Architecture decisions:** Ask before implementing
- **Breaking changes:** Highlight the impact clearly
- **Third-party services:** Confirm integration approach
- **Data migrations:** Get explicit approval
- **Security implications:** Flag for human review
