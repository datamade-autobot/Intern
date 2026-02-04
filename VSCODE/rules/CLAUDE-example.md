# CLAUDE.md - Project Configuration Template

This file tells Claude Code about your project conventions, build commands, and coding standards. Claude automatically reads this when starting a conversation.

---

## Project Overview

<!-- Replace with your project description -->
**Project Name:** [Your Project Name]
**Language(s):** [Python, JavaScript, TypeScript, etc.]
**Framework(s):** [React, FastAPI, Express, etc.]

---

## Build & Run Commands

```bash
# Install dependencies
npm install          # or: pip install -r requirements.txt

# Run development server
npm run dev          # or: python main.py

# Run tests
npm test             # or: pytest

# Build for production
npm run build        # or: python -m build

# Type checking
npm run typecheck    # or: mypy .

# Linting
npm run lint         # or: ruff check .
```

---

## Code Style Guidelines

### General
- Use descriptive variable names (no single letters except loop counters)
- Functions should do one thing well
- Keep functions under 50 lines when possible
- Add docstrings/comments for non-obvious logic

### JavaScript/TypeScript
- Use ES modules (`import/export`), not CommonJS (`require`)
- Prefer `const` over `let`, never use `var`
- Use async/await over raw promises
- Use TypeScript strict mode

### Python
- Follow PEP 8
- Use type hints for function signatures
- Prefer f-strings over `.format()` or `%`
- Use `pathlib` for file paths

---

## Project Structure

```
project-root/
├── src/              # Source code
│   ├── components/   # UI components (if applicable)
│   ├── utils/        # Helper functions
│   └── services/     # API/business logic
├── tests/            # Test files
├── docs/             # Documentation
└── scripts/          # Build/deploy scripts
```

---

## Testing Conventions

- Test files live in `tests/` directory
- Name test files `test_*.py` or `*.test.ts`
- Use descriptive test names: `test_user_can_login_with_valid_credentials`
- Aim for 80%+ coverage on critical paths
- Run tests before committing

---

## Git Workflow

- Branch naming: `feature/description`, `fix/description`, `chore/description`
- Commit messages: Use conventional commits (`feat:`, `fix:`, `docs:`, `test:`)
- Always create PRs for review (no direct pushes to main)
- Squash commits when merging

---

## Important Notes

<!-- Add project-specific warnings or context -->
- Database migrations must be reviewed before running
- API keys are stored in `.env` (never commit this file)
- The `legacy/` folder contains deprecated code - don't modify

---

## Frequently Asked Questions

**Q: How do I add a new API endpoint?**
A: Create a new file in `src/routes/`, follow the existing patterns, add tests.

**Q: How do I run the database locally?**
A: `docker-compose up -d db` then `npm run migrate`

---

## Tips for Claude

When working on this project:
1. Always run tests after making changes
2. Check TypeScript/linting errors before suggesting changes are complete
3. If unsure about architecture decisions, ask for clarification
4. Prefer small, focused changes over large refactors
