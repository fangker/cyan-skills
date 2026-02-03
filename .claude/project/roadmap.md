# Roadmap

## Completed ✅

### Phase 1: Foundation
- [x] Initial project structure
- [x] `cyan-claude-change-docs` skill for documentation updates
- [x] `cyan-organizing-claude-docs` skill for directory organization
- [x] Example project with test fixtures
- [x] TDD methodology documentation

### Phase 2: Expansion
- [x] `cyan-nonsense-style` skill for creative text transformation
- [x] Four-layer .claude/ structure implementation
- [x] Comprehensive documentation

## Planned 📋

### Phase 3: Skill Ecosystem

#### Testing Skills
- [ ] `cyan-test-generator` - Generate unit tests from code
- [ ] `cyan-test-runner` - Run tests and suggest fixes
- [ ] `cyan-tdd-guide` - Interactive TDD coaching

#### Documentation Skills
- [ ] `cyan-readme-writer` - Generate README.md from code
- [ ] `cyan-api-docs` - Generate API documentation
- [ ] `cyan-changelog-generator` - Generate CHANGELOG.md from commits

#### Code Quality Skills
- [ ] `cyan-refactor-suggester` - Suggest code refactoring
- [ ] `cyan-code-reviewer` - Automated code review
- [ ] `cyan-security-audit` - Security vulnerability scanner

#### Git Skills
- [ ] `cyan-commit-helper` - Write conventional commit messages
- [ ] `cyan-pr-reviewer` - Review pull requests
- [ ] `cyan-release-manager` - Manage releases and versioning

### Phase 4: Tooling

- [ ] Skill validation tool (check SKILL.md format)
- [ ] Skill testing framework (automated skill testing)
- [ ] Skill dependency graph (visualize skill relationships)
- [ ] CI/CD pipeline for skill development

### Phase 5: Community

- [ ] Contribution guidelines
- [ ] Skill submission process
- [ ] Community skill showcase
- [ ] Skill rating and feedback system

## Future Considerations

### Potential Skills
- **Debugging**: Stack trace analysis, bug hunting
- **Performance**: Profiling, optimization suggestions
- **Migration**: Codebase migration helpers (e.g., JS → TS)
- **Integration**: CI/CD setup, deployment automation

### Architectural Improvements
- Skill marketplace/discovery mechanism
- Skill versioning and deprecation policy
- Inter-skill communication patterns
- Skill composition primitives

## Timeline Notes

- **No deadlines**: This is a passion project, timeline is flexible
- **Priority driven**: Skills are added based on need and interest
- **Quality over quantity**: Better to have fewer high-quality skills
- **Community welcome**: Contributions accelerate the roadmap

## Contributing

See `/rules/skills.md` for skill development guidelines. To add a skill:
1. Create `/skills/<name>/SKILL.md`
2. Add test fixtures to `/src/`
3. Update this roadmap
4. Submit PR following `/rules/git.md` conventions
