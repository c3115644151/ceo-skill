# CEO Skill

CEO架构思维Skill - 4-Phase执行流程管理多Agent团队

## 概述

CEO Skill 是一个架构级项目管理技能，定义了 **4-Phase 执行流程**：

1. **想清楚** - 需求分析、目标明确、风险评估
2. **拆清楚** - 任务分解、子目标设定、资源分配
3. **验清楚** - 中间验证、迭代优化、质量把控
4. **收干净** - 成果交付、文档完善、复盘总结

## 版本

| 版本 | 路径 | 适用平台 | 核心特性 |
|---|---|---|---|
| **通用版** | `generic/SKILL.md` | Coze / Claude Code / 任意平台 | 审查发现问题→重开Agent描述问题修复 |
| **OpenCode 增强版** | `opencode/SKILL.md` | OpenCode | **task_id 召回原Agent精准修复**，保留完整上下文 |

### 两个版本的核心差异

通用版在修复阶段只能"新开Agent + 描述问题"，新Agent不知道原Agent做了什么、为什么那么做。OpenCode 增强版利用 OpenCode 独有的 `task_id` 持久化子Agent会话机制，在审查发现问题后**召回原Agent**，原Agent带着完整开发记忆精准修正，将审查-修复循环从"重做"变为"迭代"。

详见 `opencode/references/task-id-mechanism.md`。

## 目录结构

```
ceo-skill/
├── README.md
├── generic/
│   ├── SKILL.md                          # 通用版Skill定义
│   └── references/
│       └── dispatch-template.md          # 任务分发模板
├── opencode/
│   ├── SKILL.md                          # OpenCode增强版Skill定义
│   └── references/
│       ├── dispatch-template.md          # 任务分发模板
│       └── task-id-mechanism.md          # task_id持久化机制说明
├── SKILL.md                              # [旧] 通用版入口（将在后续版本移除）
└── references/
    └── dispatch-template.md              # [旧] 模板（将在后续版本移除）
```

## 适用场景

- 复杂系统架构设计
- 多团队协作项目管理
- Agent团队协调
