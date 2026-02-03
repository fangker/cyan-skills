# Git and Version Control

Non-negotiable git practices for this project.

## Commit Messages

All commit messages MUST follow this format:
```
type(scope): description

optional body
```

**Types:**
- `feat`: New skill or feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

**Examples:**
- `feat(cyan-nonsense): Add dual-mode support for text transformation`
- `docs(readme): Update project overview`
- `test(button): Add unit tests for Button component`

## Branch Protection

- NEVER force push to `main`
- ALWAYS create a branch for new skills
- MUST ensure tests pass before pushing

## .gitignore

The following MUST be ignored:
- `node_modules/`
- `.DS_Store`
- `*.log`
- Coverage reports
- Build artifacts

## Commit Safety

- NEVER use `git commit --amend` after hook failure
- ALWAYS stage files explicitly (avoid `git add .`)
- NEVER skip pre-commit hooks unless explicitly requested
