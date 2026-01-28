# Cyan Skills

这是一个技能集合项目，包含多个可重用的 Claude Code 技能。

## 项目结构

```
cyan-skills/
├── skills/                    # 技能目录
│   └── claude-change-documentation/  # 文档更新技能
│       └── SKILL.md
├── claude/                    # 示例项目的 ./claude 目录
│   ├── CLAUDE.md
│   └── patterns/
│       └── button-component.md
└── src/                       # 示例项目代码
    ├── components/
    │   └── Button.tsx
    └── utils/
        └── date.ts
```

## 技能列表

### claude-change-documentation
分析代码变更并更新 `./claude` 目录下的相关文档。

**使用场景：**
- 代码变更后需要同步更新文档
- 保持项目文档与代码一致
- 维护 ./claude 目录中的 AI 上下文

## 开发说明

这是一个用于管理和开发 Claude Code 技能的项目。每个技能都遵循 TDD (Test-Driven Development) 方法论创建。

## 相关资源

- [Claude Code Documentation](https://github.com/anthropics/claude-code)
- [writing-skills](https://github.com/anthropics/claude-code/tree/main/skills/writing-skills) - 技能创作方法论
