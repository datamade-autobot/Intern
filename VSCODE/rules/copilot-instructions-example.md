# GitHub Copilot Custom Instructions

This file configures GitHub Copilot's behavior for this project. Place it at `.github/copilot-instructions.md` in your repository.

---

## Code Generation Preferences

### Style
- Generate code that matches the existing codebase style
- Use TypeScript over JavaScript when both are present
- Prefer async/await over callbacks or raw promises
- Include JSDoc/docstrings for public functions

### Quality
- Always include error handling in generated code
- Add type annotations for function parameters and returns
- Generate meaningful variable names, not single letters
- Include input validation where appropriate

### Testing
- When generating functions, suggest corresponding test cases
- Use the project's existing test framework
- Generate descriptive test names that explain the scenario

---

## Language-Specific Instructions

### TypeScript
```
- Use strict mode typing
- Prefer interfaces over type aliases for objects
- Use enums for fixed sets of values
- Avoid `any` type - use `unknown` if necessary
```

### Python
```
- Use type hints (Python 3.10+ syntax when possible)
- Follow PEP 8 conventions
- Use f-strings for string formatting
- Prefer `pathlib.Path` over `os.path`
```

### React
```
- Use functional components with hooks
- Prefer named exports over default exports
- Use TypeScript for all component files
- Include prop type definitions
```

---

## Context Awareness

When generating code, consider:
- The file's location in the project structure
- Imports already present in the file
- Patterns used in adjacent files
- The project's established conventions

---

## What NOT to Generate

- Don't generate code with hardcoded secrets or credentials
- Don't generate code that disables security features
- Don't generate overly complex one-liners
- Don't generate code with console.log in production paths
- Don't generate deprecated API usage

---

## Inline Suggestions

When providing inline completions:
- Complete the current logical unit (function, statement, block)
- Match indentation and formatting
- Consider the context from comments above the cursor
- Suggest meaningful names based on surrounding code

---

## Chat Interactions

When responding to chat questions:
- Be concise but complete
- Provide working code examples
- Explain the "why" not just the "what"
- Suggest alternatives when appropriate
- Flag potential issues or edge cases
