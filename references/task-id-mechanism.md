# task_id 召回机制

OpenCode 子Agent的 `task_id` 即持久化子会话ID，完成后不销毁。

## 用法

```
# 创建
Task(description="...", subagent_type="general") → 返回结果含 task_id

# 召回（原Agent带完整上下文继续）
Task(description="修正指令...", task_id="<之前返回的>", subagent_type="general")
```

## 规则

- 规格偏差/实现错误/遗漏边界/追加需求 → **task_id 召回**
- 方向性完全错误 / 同一Agent修正≥3次仍不达标 → **新开Agent**
- 几行代码的小问题 → **自己缝补**
