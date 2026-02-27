---
description: 唤醒记忆系统 — 一条命令冷启动 AI 助手全量上下文
---

# /memory — 记忆唤醒协议

当用户输入 `/memory` 或 `载入记忆` 时，执行以下步骤：

// turbo-all

## 步骤

1. 读取系统说明 (SOUL 协议)
```
view_file <YOUR_MEMORY_SYSTEM_PATH>/00_系统说明_README.md
```

2. 读取用户画像
```
view_file <YOUR_MEMORY_SYSTEM_PATH>/02_用户画像_USER.md
```

3. 读取核心索引 (全局导航)
```
view_file <YOUR_MEMORY_SYSTEM_PATH>/01_核心索引_Index.md
```

4. 读取当前焦点 (滑动窗口)
```
view_file <YOUR_MEMORY_SYSTEM_PATH>/10_当前焦点_Focus.md
```

5. 完成唤醒后，向用户汇报：
   - 当前推理状态（从 Focus 摘要）
   - 最高优先级任务
   - 等待用户指令
