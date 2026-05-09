# CEO Skill — 架构级 Agent 团队调度

面对架构级复杂项目时，以 CEO 视角梳理全貌、拆分模块、调度 Agent Teams 开发、审核验收。

## 适用场景

- 项目涉及 3 个以上模块需要协调（重构、多子系统搭建）
- 需要将复杂任务拆解为可并行开发的子任务
- 需要统一的数据契约和接缝定义来避免 Agent 间心智模型不一致

## 工作流程

```
Phase 1: 想清楚 → 数据流图 + 接缝定义 + 不可变约束
Phase 2: 拆清楚 → 写 DISPATCH.md → 按依赖调度 Agent Teams
Phase 3: 验清楚 → 端到端链路 + 测试质量审查 → 召回修复
Phase 4: 收干净 → 清理临时文件 → 重置 DISPATCH.md
```

## 核心原则

- **接缝比模块危险**：调度重心放在模块间的数据流，不是模块内部实现
- **测试纪律是项目基线，不是 CEO 逐任务指定的**：不可变约束里写明"所有实现必须包含测试"，Agent 自觉执行
- **测试全绿不等于功能正确**：审查先看测了什么边界、覆盖了什么错误场景，再看绿不绿
- **描述需求，不规定做法**：给 Agent 说"要达成什么"，不说"怎么做"

## 文件结构

```
SKILL.md                         — CEO skill 核心规则
references/dispatch-template.md  — 调度文档模板
references/task-id-mechanism.md  — Agent 召回机制说明
```

## 安装

通过 CC Switch 安装。Skill 名称：`ceo-skill-opencode`
