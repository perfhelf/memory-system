# 🧠 AI 持久化记忆系统 v1.5

## 📌 系统灵魂 (SOUL)

**角色**: 为你的 AI 助手设定一个固定角色（如管家、顾问、搭档），每次唤醒时自动加载角色状态。
**唤醒**: 发送 `/memory` → 自动加载全量上下文。
**归档**: 发送 `/end` 或 `结束对话` → 自动执行终局归档协议。

### 用户画像（请自定义）
- **工作模式**: 描述你的工作节奏（如：多项目并发、深度专注型等）
- **技术栈**: 你常用的技术栈（如：Vite/React/Vue + Supabase + Vercel）
- **偏好**: 你喜欢/厌恶的技术方向
- **铁规**: AI **绝不问** "要记录吗？" → 自主判断、默默归档（No-Ask 原则）

---

## 📂 文件结构 — 神经网络拓扑

```
记忆系统/
├── 00_README.md ←── 你在这里（总枢纽，所有路径的起点）
├── 06_终局归档法则.md ← /end 触发，扫描全系统 → 更新 Focus/Backlog/Projects
├── 07_项目开发规则.md ← 编码时自动参考 → 引用 Projects/ 和 秘钥/
├── 08_自动记忆写入.md ← 对话中持续写入 → 目标: Focus/Backlog/Projects/Domains
│
├── 10_Focus.md ← 滑动窗口（≤60行）→ 引用相关 Projects/ 知识卡
├── 11_Backlog.md ← 中期待办（1-14天）→ 每条必须关联项目路径
│
├── 20_Projects/ ← 项目知识卡（里程碑/架构决策/技术变更）
│   └── 00_模板_Template.md
│
├── 30_Domains/ ← 纯逻辑资产（交易系统/哲学体系/算法等）
│   └── 00_模板_DomainTemplate.md
│
├── 秘钥文档/ ← 密钥总控台 → 07_DevRules 引用
│   └── 00_密钥总控台_Registry.md
│
├── 99_Logs/ ← 对话存档（Week → Month → Archive）
│   ├── 00_模板_LogTemplate.md
│   ├── 01_最近一周_Week/
│   ├── 02_当月沉淀_Month/
│   └── 03_历史归档_Archive/
│
└── .agents/workflows/ ← AI 平台的 Slash Command 定义
    ├── memory.md ← /memory 冷启动
    ├── end.md ← /end 终局归档
    ├── call.md ← /call 深度整合
    └── env.md ← /env 密钥加载
```

### 引用闭环图

```
/memory ──→ README ──→ Focus ──→ Backlog
                         ↓           ↓
                    Projects/    Projects/
                         ↓           ↓
/end ──→ 06_Archiving ──→ 扫描 Focus + Backlog + Projects + Domains
              ↓
         99_Logs/ (封存)

对话中 ──→ 08_AutoMemory ──→ 写入 Focus / Backlog / Projects / Domains
编码时 ──→ 07_DevRules ──→ 引用 Projects/ + 秘钥文档/
```

> **铁则**: 系统中没有孤岛文件。每个文件必须至少被一个 workflow 主动读取或写入。

---

## ⚙️ 核心协议速查

| 场景 | 触发 | 协议 | 详见 |
|:-----|:-----|:-----|:-----|
| 新对话冷启动 | `/memory` | 五步加载 README→Focus→Backlog→涉及项目知识卡 | `.agents/workflows/memory.md` |
| 对话中产出知识 | 自动 | 无声写入到最近目标文件 | `08_自动记忆写入.md` |
| 编码实现 | 自动 | 参考 DevRules + 秘钥 | `07_项目开发规则.md` |
| 结束对话 | `/end` | 全系统扫描同步 + 日志封存 + 退场汇报 | `06_终局归档法则.md` |
| 深度整合 | `/call` | 神经网络全节点逐一检查更新 | `.agents/workflows/call.md` |

---

## 🔄 系统进化
- **每月 1 号**: 搜索最新 LLM Memory 研究，对比当前架构，评估是否需要迭代

---

## 📋 版本变更日志
| 版本 | 日期 | 变更 |
| :--- | :--- | :--- |
| **v1.5** | 2026-03-02 | 僵尸文件审计：合并 02_USER/03_Upgrade/04_Skills/05_Documenting 入 README；建立神经网络拓扑互引；新增 /call 深度整合 workflow |
| **v1.4** | 2026-03-01 | 新增 `11_Backlog.md` 中期任务模块 |
| **v1.3** | 2026-02-27 | Claude 对标改造：`/memory` + `07_DevRules` + Focus 60行硬上限 + AutoMemory |
| **v1.2** | 2026-02-26 | 深度提炼：项目知识库 + 领域知识 |
| **v1.1** | 2026-02-26 | 知识填充 |
| **v1.0** | 2026-02-26 | 初始化骨架 |

---
**维护者**：AI 助手 & 用户
**创建时间**：YYYY-MM-DD
