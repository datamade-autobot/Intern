# AI Agent Instructions

## Project Context
### What
[Describe what this project is - its purpose and main functionality]

### Who
[Who uses this? Internal team? External customers? Scale?]

### Why
[Why was this built? What problem does it solve?]

### Current State
- Version: [e.g., 2.1.0]
- Status: [e.g., Production, Beta, Active Development]
- Team Size: [e.g., 3 developers]

## Architecture
### Overview
[High-level architecture - monolith, microservices, etc.]

### Key Components
- **[Component 1]**: [Description]
- **[Component 2]**: [Description]
- **[Component 3]**: [Description]

### Data Flow
[How data moves through the system]

## Stack
### Runtime & Language
- [Language] [Version] - [Why this version]
- [Runtime] [Version]

### Framework
- [Main Framework] [Version]
- [Why this framework]

### Database
- [Database Type] [Version]
- [ORM/Client if applicable]

### Caching
- [If applicable]

### Infrastructure
- Hosted on: [Platform]
- CI/CD: [Tools]
- Monitoring: [Tools]

### Key Dependencies
- [Dependency 1] - [Purpose]
- [Dependency 2] - [Purpose]
- [Dependency 3] - [Purpose]

## Code Style & Standards

### General Principles
- [e.g., "Prefer explicit over implicit"]
- [e.g., "Write self-documenting code"]
- [e.g., "Optimize for readability"]

### Naming Conventions
- **Variables**: [e.g., camelCase, descriptive names]
- **Functions**: [e.g., verbNoun format like getUserById]
- **Classes**: [e.g., PascalCase]
- **Constants**: [e.g., SCREAMING_SNAKE_CASE]
- **Files**: [e.g., kebab-case.ts]

### File Structure
```
[Show typical file organization]
```

### Code Organization
- [e.g., "One class per file"]
- [e.g., "Group related functions"]
- [e.g., "Separate business logic from framework code"]

### Language-Specific
- [e.g., "Use async/await, never callbacks"]
- [e.g., "Prefer composition over inheritance"]
- [e.g., "Use const by default, let when needed, never var"]

### Comments & Documentation
- [e.g., "JSDoc for all public APIs"]
- [e.g., "Explain why, not what"]
- [e.g., "Keep comments up to date"]

### Error Handling
- [e.g., "Use custom error classes"]
- [e.g., "Always log errors"]
- [e.g., "Return errors, don't throw"]

## Testing Standards

### Coverage Requirements
- Minimum: [e.g., 80% code coverage]
- Critical paths: [e.g., 100% coverage]

### Test Types
- **Unit Tests**: [Requirements and tools]
- **Integration Tests**: [When and how]
- **E2E Tests**: [For what scenarios]

### Test Organization
[How tests should be structured and named]

### Running Tests
```bash
# All tests
[command]

# Unit tests only
[command]

# Integration tests only
[command]

# With coverage
[command]

# Watch mode
[command]
```

## API Design (if applicable)

### REST Conventions
- [e.g., "Use plural nouns for resources"]
- [e.g., "Version all endpoints: /api/v1/..."]
- [e.g., "Use HTTP status codes correctly"]

### Request/Response Format
[Standard formats and patterns]

### Authentication
[How auth works in this project]

### Rate Limiting
[Any rate limits or throttling]

## Database Guidelines

### Schema Design
- [e.g., "Always use UUIDs for primary keys"]
- [e.g., "Include created_at/updated_at on all tables"]

### Queries
- [e.g., "Use prepared statements always"]
- [e.g., "Add indexes for foreign keys"]

### Migrations
- [e.g., "All migrations must be reversible"]
- [e.g., "Test migrations on staging first"]

## Security Guidelines

### Authentication & Authorization
[How these work in this project]

### Secrets Management
- [e.g., "Never commit secrets"]
- [e.g., "Use environment variables"]
- [e.g., "Rotate keys quarterly"]

### Input Validation
- [e.g., "Validate all user input"]
- [e.g., "Sanitize before database queries"]

### Common Vulnerabilities
- [e.g., "Watch for SQL injection"]
- [e.g., "Prevent XSS"]
- [e.g., "Use CSRF tokens"]

## Performance Guidelines

### Optimization Priorities
1. [e.g., "Readability first"]
2. [e.g., "Optimize only when measured"]
3. [e.g., "Cache at appropriate layers"]

### Known Bottlenecks
- [Document any known performance issues]

### Caching Strategy
[How and when to cache]

## Common Commands

### Development
```bash
# Install dependencies
[command]

# Start dev server
[command]

# Build
[command]

# Format code
[command]

# Lint
[command]
```

### Testing
```bash
# Run all tests
[command]

# Run specific test
[command]

# Test with coverage
[command]
```

### Deployment
```bash
# Deploy to staging
[command]

# Deploy to production
[command]

# Rollback
[command]
```

### Database
```bash
# Run migrations
[command]

# Create migration
[command]

# Seed database
[command]
```

### Debugging
```bash
# View logs
[command]

# Debug mode
[command]
```

## Important Notes & Gotchas

### Known Issues
1. [Issue description and workaround]
2. [Issue description and workaround]

### Edge Cases
- [Edge case 1]
- [Edge case 2]

### Common Mistakes
- ❌ [Common mistake]: Instead, do [correct approach]
- ❌ [Common mistake]: Instead, do [correct approach]

### Configuration
- [Important config settings]
- [Environment-specific settings]

### Third-Party Integrations
- [API 1]: [Key info and gotchas]
- [API 2]: [Key info and gotchas]

## Workflows

### Adding a New Feature
1. [Step 1]
2. [Step 2]
3. [Step 3]

### Bug Fix Process
1. [Step 1]
2. [Step 2]
3. [Step 3]

### Code Review Checklist
- [ ] [Checkpoint 1]
- [ ] [Checkpoint 2]
- [ ] [Checkpoint 3]

## Resources

### Documentation
- [Internal docs link]
- [API docs]
- [Architecture diagrams]

### Team Communication
- Slack: [Channel]
- Stand-ups: [Schedule]
- Code reviews: [Process]

### External Resources
- [Framework docs]
- [Library docs]
- [Design system]

## Changelog
### Recent Major Changes
- **[Date]**: [Change description]
- **[Date]**: [Change description]

---

*Last updated: [Date]*
*Maintained by: [Team/Person]*
