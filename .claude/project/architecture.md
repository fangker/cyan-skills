# Architecture

## System Design

The cyan-skills project follows a modular architecture where each skill is independent and self-contained.

```
cyan-skills/
├── skills/                    # Skill definitions
│   ├── <skill-name>/          # One directory per skill
│   │   └── SKILL.md           # Skill documentation and logic
├── .claude/                   # AI context for this project
│   ├── instructions.md        # Directory relationships
│   ├── rules/                 # Non-negotiable constraints
│   ├── project/               # Goals and architecture
│   └── frame/                 # Framework-specific patterns
├── src/                       # Test fixtures and examples
│   ├── components/            # Example React components
│   └── utils/                 # Example utility functions
└── claude/                    # Legacy documentation (for examples)
    ├── CLAUDE.md              # Example project docs
    └── patterns/              # Example patterns
```

## Skill Independence

Each skill MUST be:
- **Invocable independently** via `/skill-name` command
- **Testable in isolation** without other skills
- **Self-documenting** with clear usage examples
- **Version-controlled** in its own commit

## Skill Interactions

Skills MAY reference each other:
- Using the `Skill` tool to invoke other skills
- Documenting dependencies in `SKILL.md`
- Following each other's constraints

**Example:** `cyan-organizing-claude-docs` creates structure that `cyan-claude-change-docs` maintains.

## Technology Choices

### Why Skills?

Skills are the native extension mechanism for Claude Code:
- First-class support in Claude Code
- Simple markdown-based format
- Automatic invocation based on context
- Composable and reusable

### Why Four-Layer .claude/ Structure?

Prevents common problems:
- **Ambiguity**: Clear rules for where content belongs
- **Duplication**: Single source of truth for each type of content
- **Bloat**: instructions.md explains relationships, doesn't repeat content
- **Confusion**: Framework-specific vs. project-specific is explicit

### Why TDD?

Skills are prompt-based and hard to test traditionally:
- TDD forces clear requirements before writing prompts
- Test fixtures validate skill behavior
- Example-driven development ensures clarity

## Data Flow

```
User invokes skill (e.g., /cyan-organizing-claude-docs)
         ↓
Claude loads SKILL.md
         ↓
Skill instructions execute
         ↓
Claude uses tools (Read, Write, Edit, etc.)
         ↓
Skill produces output
```

## Extension Points

1. **Adding a new skill**: Create `/skills/<name>/SKILL.md`
2. **Adding test fixtures**: Add files to `/src/`
3. **Updating project rules**: Edit `/rules/*.md`
4. **Documenting architecture**: Update `/project/architecture.md`
