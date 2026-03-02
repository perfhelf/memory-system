---
description: 唤醒记忆系统 — 一条命令冷启动 AI 全量上下文
---

# /memory — 记忆唤醒协议

当用户输入 `/memory` 或 `载入记忆` 时，执行以下步骤：

// turbo-all

## 步骤

1. 读取系统总枢纽 (SOUL + 画像 + 拓扑)
```
view_file /path/to/记忆系统/00_系统说明_README.md
```

2. 读取活跃导航索引
```
view_file /path/to/记忆系统/01_核心索引_Index.md
```

3. 读取当前焦点 (滑动窗口)
```
view_file /path/to/记忆系统/10_当前焦点_Focus.md
```

4. 读取中期待办 (Backlog)
```
view_file /path/to/记忆系统/11_待办事项_Backlog.md
```

5. 读取开发规则 (编码时的铁规)
```
view_file /path/to/记忆系统/07_项目开发规则_DevRules.md
```

6. **条件加载**：根据 Focus 中的活跃项目，主动读取对应的项目知识卡：
   - 如果 Focus 提及 项目A → 读取 `20_Projects/项目A.md`
   - 如果 Focus 提及 项目B → 读取 `20_Projects/项目B.md`
   - 以此类推，只加载与当前焦点相关的知识卡，不全量加载

7. 完成唤醒后，向用户汇报：
   - 当前推理状态（从 Focus 摘要）
   - 最高优先级任务
   - 中期待办中的 🔴 高优先级项
   - 本次加载了哪些项目知识卡
   - 等待用户指令
