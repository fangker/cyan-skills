# Claude's Identity & Purpose

Claude is an AI assistant helping to develop and maintain a collection of reusable Claude Code skills. This project focuses on creating, testing, and documenting skills that extend Claude Code's capabilities.

**Default behaviors:**
- Follow TDD methodology when creating new skills
- Maintain clear separation between skill logic and project-specific code
- Prioritize documentation and usability
- Use TypeScript for skill implementations
- Test skills thoroughly before deployment

---

## Directory Structure

This project uses a four-layer `.claude/` structure to organize context and constraints for skills development.

### /rules/

Contains non-negotiable constraints that all agents must follow, including coding standards, documentation requirements, and skill development conventions. These are hard rules, not guidelines.

### /project/

Contains project planning documents: overview (what this skills collection is), architecture (how skills relate to each other and to Claude Code), and roadmap (planned skills and improvements). Focuses on WHY and WHAT, not HOW.

### /frame/

Contains framework-specific conventions: how to develop skills for Claude Code, skill API patterns, testing frameworks, and development environment setup. Content here is specific to the Claude Code skills ecosystem.

---

## How Directories Relate

These directories are peers, not a hierarchy. Priority depends on context:
- Rules from `/rules/` always apply (e.g., "all skills must have SKILL.md")
- `/project/` explains goals and architecture (e.g., "why we chose this skill structure")
- `/frame/` provides Claude Code-specific implementation guidance (e.g., "how to use the Skill tool")
- Claude dynamically judges which takes precedence based on context

**Example:** When creating a new skill, Claude must:
1. Follow the skill development rules in `/rules/skills.md`
2. Understand the project architecture in `/project/architecture.md`
3. Apply Claude Code-specific patterns from `/frame/skill-development.md`

---

## Quick Reference

| Directory | Purpose | Example Content |
|-----------|---------|-----------------|
| `/rules/` | Non-negotiable constraints | "Every skill must have a SKILL.md file" |
| `/project/` | Goals and architecture | "This is a collection of reusable Claude Code skills" |
| `/frame/` | Framework-specific guides | "How to invoke skills using the Skill tool" |
| `instructions.md` | You are here | Explains the directory relationships |
