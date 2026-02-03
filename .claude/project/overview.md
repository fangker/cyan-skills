# Project Overview

## What is cyan-skills?

A collection of reusable Claude Code skills that extend Claude's capabilities. Each skill is a self-contained prompt that can be invoked via slash commands or by Claude automatically based on context.

## Who is this for?

- **Claude Code users** who want to extend Claude with custom behaviors
- **Developers** building skills for their teams
- **Contributors** adding new skills to the collection

## Project Goals

1. **Create reusable skills** that solve common development tasks
2. **Demonstrate best practices** for skill development
3. **Maintain high quality** through TDD and documentation
4. **Share knowledge** about Claude Code's extensibility

## Current Skills

### cyan-claude-change-docs
Analyzes code changes and updates `.claude/` documentation to maintain consistency between code and AI context.

### cyan-organizing-claude-docs
Standardizes `.claude/` directory structure using a four-layer classification system to prevent ambiguous file placement.

### cyan-nonsense-style
Transforms text into verbose, circular pseudo-profound nonsense literature style (for creative tasks).

## Success Criteria

A skill is successful when:
- It has a clear, specific use case
- Documentation explains when to use and when NOT to use it
- It works reliably in isolation
- Examples demonstrate real-world usage
- Tests validate core functionality

## Non-Goals

- Building a general-purpose AI assistant
- Creating skills for every possible task
- Maintaining backward compatibility forever (skills evolve)

## Related Projects

- [Claude Code](https://github.com/anthropics/claude-code) - The main Claude Code repository
- [writing-skills](https://github.com/anthropics/claude-code/tree/main/skills/writing-skills) - Official skill development guide
