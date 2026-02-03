# Claude Code Skills Development

Framework-specific guide for developing skills for Claude Code.

## What is a Skill?

A skill is a markdown file (`SKILL.md`) that extends Claude Code's behavior. Skills are:
- Invoked via slash commands (e.g., `/my-skill`)
- Automatically invoked based on context triggers
- Composable (skills can invoke other skills)
- Self-documenting

## Skill File Format

Every `SKILL.md` MUST follow this structure:

```markdown
# Human-Readable Skill Name

Brief one-line description.

## Overview

Detailed description of what the skill does (2-3 sentences).

## When to Use

**Use when:**
- Specific condition 1
- Specific condition 2

**Don't use when:**
- Condition where skill shouldn't be used
- Alternative approach condition

## How It Works

[Optional] Explanation of the skill's approach or methodology.

## Examples

### Example 1
**User:** [Example user input]
**Claude:** [Expected behavior]

## Configuration

[Optional] Any configuration options or parameters.

## Related Skills

- [Other skill name](/path/to/other/skill)
```

## Invoking Skills

### Via Slash Command

Users can invoke skills directly:
```
/user/cyan-organizing-claude-docs
```

### Programmatically (Within Skills)

Skills can invoke other skills using the `Skill` tool:

```text
Use Skill tool to invoke: claude-change-documentation
```

### Automatic Invocation

Claude Code automatically suggests skills based on:
- User input matching "When to use" conditions
- File path patterns (e.g., working in `.claude/` directory)
- Context clues (e.g., "I need to organize documentation")

## Skill Development Patterns

### 1. State-Snapshot-Exit Pattern

For multi-step operations:
1. **State**: Capture current state (read files, check git status)
2. **Snapshot**: Show user what will change
3. **Exit**: Let user confirm before making changes

### 2. Question-First Pattern

When requirements are ambiguous:
1. Use `AskUserQuestion` tool immediately
2. Gather preferences before starting work
3. Avoid making assumptions

### 3. Tool-Usage Pattern

Always use the right tool:
- `Read` instead of `bash cat`
- `Edit` instead of `bash sed`
- `Glob` instead of `bash find`
- `Grep` instead of `bash grep`

### 4. Context-Aware Pattern

Check context before acting:
1. Use `Glob` to find relevant files
2. Use `Grep` to search content
3. Use `Read` to understand current state
4. Only then make changes

## Common Skill Patterns

### File Organization Skills

```markdown
## When to Use
- Creating or reorganizing .claude/ directories
- Deciding where to place documentation
- Fixing inconsistent directory structure
```

### Code Generation Skills

```markdown
## When to Use
- Creating new components with clear specifications
- Generating boilerplate from templates
- Implementing well-defined patterns

## Don't Use When
- Requirements are ambiguous (use brainstorming skill first)
- User needs exploration, not generation
```

### Documentation Skills

```markdown
## When to Use
- Code has changed and docs need updating
- User explicitly requests documentation updates
- Maintaining .claude/ directory consistency
```

## Testing Skills

### Manual Testing Process

1. **Create test scenario**: Define input and expected output
2. **Invoke skill**: Use `/skill-name` command
3. **Verify behavior**: Check output matches expectations
4. **Test edge cases**: Try unusual inputs
5. **Document examples**: Add real examples to SKILL.md

### Test Fixtures

Place example code in `/src/` for testing:
```
src/
├── components/     # Test components
├── utils/          # Test utilities
└── test-project/   # Isolated test environment
```

## Skill Permissions

Some skills require special permissions. Configure in `.claude/settings.local.json`:

```json
{
  "permissions": {
    "allow": [
      "Bash(git:*)",
      "WebSearch",
      "Skill(*)"
    ]
  }
}
```

**Warning:** Only request permissions that are essential for the skill's purpose.

## Skill Distribution

### Local Development

Skills in `~/.claude/skills/` are available globally.

### Project-Specific Skills

Skills in `<project>/.claude/skills/` are available only for that project.

### Sharing Skills

1. Create a repository with skills in `/skills/` directory
2. Document installation instructions
3. Users copy skills to their `~/.claude/skills/` directory

## Debugging Skills

### Common Issues

**Skill not invoked:**
- Check "When to Use" conditions are clear
- Verify skill is in correct directory
- Check permissions in settings.local.json

**Skill behaves incorrectly:**
- Review instructions in SKILL.md
- Check for ambiguous requirements
- Add more examples to clarify

**Skill invokes wrong tools:**
- Review tool usage patterns
- Use specialized tools (Read, Edit) over bash
- Check tool permissions

### Debugging Tips

1. **Start fresh**: Clear conversation context and retry
2. **Simplify**: Reduce skill to minimal example
3. **Add logging**: Use text output to show progress
4. **Test incrementally**: Test each step separately

## Related Resources

- [writing-skills](https://github.com/anthropics/claude-code/tree/main/skills/writing-skills) - Official skill development methodology
- [claude-code-docs](https://github.com/anthropics/claude-code) - Claude Code documentation
- `/rules/skills.md` - Project-specific skill development rules
