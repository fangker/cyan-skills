# Skills Development Rules

Non-negotiable constraints for developing Claude Code skills in this project.

## Skill Structure

Every skill MUST have:
- `SKILL.md` - Main skill documentation following Claude Code skill format
- Clear purpose and use cases
- Trigger conditions (when to invoke)
- Examples of usage

## File Organization

- Skills live in `/skills/<skill-name>/SKILL.md`
- Skill names use kebab-case (e.g., `cyan-claude-change-docs`)
- Test fixtures live in `/src/` for demonstration purposes

## Documentation Requirements

All skills MUST document:
- **Overview**: What does this skill do?
- **When to use**: Clear trigger conditions
- **When NOT to use**: Anti-patterns to avoid
- **Examples**: Concrete usage scenarios
- **Dependencies**: Other skills or tools required

## Code Quality

- Use TypeScript for any code implementations
- Follow TDD: Write tests before implementation
- All skills must be testable in isolation
- No circular dependencies between skills

## Git Conventions

- Commit messages MUST follow conventional commit format
- Skills MUST be committed in working state before being referenced
- Test fixtures MUST be included in commits

## Skill Metadata

Every `SKILL.md` MUST include:
- Base directory path
- Human-readable name
- Overview section
- When to use / Don't use sections
