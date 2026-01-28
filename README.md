# Cyan Skills

这是一个技能集合项目，包含多个可重用的 Claude Code 技能。

## 项目结构

```
cyan-skills/
├── skills/                              # 技能目录
│   ├── cyan-claude-change-docs/         # 文档同步技能
│   │   └── SKILL.md
│   └── cyan-organizing-claude-docs/     # 文档组织技能
│       └── SKILL.md
├── claude/                              # 示例项目的 ./claude 目录
│   ├── CLAUDE.md
│   └── patterns/
│       └── button-component.md
└── src/                                 # 示例项目代码
    ├── components/
    │   └── Button.tsx
    └── utils/
        └── date.ts
```

## 技能列表

### cyan-claude-change-docs
分析代码变更并更新 `.claude/` 目录下的相关文档。

**使用场景：**
- 代码变更后需要同步更新文档
- 保持项目文档与代码一致
- 维护 .claude 目录中的 AI 上下文

**支持的文档结构：**
- `instructions.md` - Claude 身份和默认行为
- `rules/` - 不可协商的约束（编码标准、安全要求等）
- `project/` - 项目目标和架构
- `frame/` - 技术栈和框架约定

### cyan-organizing-claude-docs
标准化 `.claude/` 目录结构，提供清晰的文档分类规则。

**使用场景：**
- 创建或重构 .claude/ 目录
- 决定文档应该放在哪个位置
- 修复不一致的目录结构

**四层分类结构：**
1. `instructions.md` - 根节点，说明目录关系
2. `rules/` - 非协商性约束
3. `project/` - 目标/架构/路线图
4. `frame/` - 技术栈/框架/约定

## 开发说明

这是一个用于管理和开发 Claude Code 技能的项目。每个技能都遵循 TDD (Test-Driven Development) 方法论创建。

## 相关资源

- [Claude Code Documentation](https://github.com/anthropics/claude-code)
- [writing-skills](https://github.com/anthropics/claude-code/tree/main/skills/writing-skills) - 技能创作方法论

## License

MIT
