# Documentation Standards

Non-negotiable documentation requirements for this project.

## Language

- Project documentation MUST be in English
- Code comments SHOULD be in English
- Example content MAY use other languages for demonstration (e.g., the Chinese example in `/claude/`)

## Markdown Format

All documentation files MUST:
- Use proper markdown syntax
- Include frontmatter if required by the file type
- Use code blocks with language specification
- Link references using relative paths

## File Naming

- Use kebab-case for all filenames (e.g., `skill-development.md`)
- Use `.md` extension for markdown files
- Names should be descriptive and concise

## Documentation Updates

When code changes:
- Update related documentation immediately
- Use the `claude-change-documentation` skill for .claude/ updates
- Document breaking changes clearly

## .claude/ Documentation

The `.claude/` directory is for Claude's context, NOT human-readable docs:
- `instructions.md` explains directory relationships
- `/rules/` contains non-negotiable constraints
- `/project/` contains goals and architecture
- `/frame/` contains framework-specific guides

Human-facing documentation goes in `/README.md` or `/docs/`.
