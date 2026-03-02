# 🧠 AI Persistent Memory System

**English** | [中文](./README_CN.md)

A **physical-file-based, version-controllable, structured** persistent memory system designed for AI assistants (Claude, GPT, Gemini, etc.) that lack built-in long-term memory.

## 🤔 Why This Exists

Every AI conversation starts from zero. Chat history gets lost, context windows overflow, and institutional knowledge evaporates. This system solves that by maintaining a **Markdown-based memory vault** on your local filesystem that your AI can read and write to across sessions.

**Core philosophy**: If the AI can read files, it can remember everything.

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| **One-Command Cold Boot** | `/memory` → loads full context in seconds |
| **Hot/Warm/Cold Tiering** | Focus → Weekly → Monthly → Archive |
| **Mid-Term Backlog** | Separate `11_Backlog.md` for 1-14 day tasks |
| **High Compression** | Every chunk ≤ 400 tokens for precise retrieval |
| **Auto-Memory Write** | AI silently archives valuable info during conversations |
| **End-of-Session Archiving** | `/end` → forced knowledge distillation on conversation close |
| **Deep Integration** | `/call` → full neural network node-by-node sync |
| **Key Management** | Centralized secret/token registry (AI reads keys, never asks you) |
| **Project Dev Rules** | Centralized coding conventions per project |
| **Neural Network Topology** | Every file has bidirectional references — no orphan files |

## 📂 Directory Structure (v1.5)

```
记忆系统/
├── 00_系统说明_README.md          # System rules & SOUL protocol
├── 01_核心索引_Index.md           # Global navigation hub
├── 06_终局归档法则_Archiving.md   # End-of-session archiving SOP
├── 07_项目开发规则_DevRules.md    # Per-project coding rules
├── 08_自动记忆写入_AutoMemory.md  # Auto-write protocol
│
├── 10_当前焦点_Focus.md           # Current tasks (≤60 lines)
├── 11_待办事项_Backlog.md         # Mid-term backlog (1-14 days)
│
├── 20_项目知识库_Projects/        # Project knowledge cards
├── 30_核心领域_Domains/           # Domain expertise vault
├── 99_对话存档_Logs/              # Conversation logs (hot/warm/cold)
├── 秘钥文档/                      # Secret & key registry
│
└── .agents/workflows/
    ├── memory.md                   # /memory — cold boot
    ├── end.md                      # /end — end-of-session archiving
    ├── call.md                     # /call — deep integration
    └── env.md                      # /env — key & deploy management
```

> **v1.5 Change**: Files `02_USER`, `03_Upgrade`, `04_Skills`, `05_Documenting` have been **merged into `00_README`** to eliminate zombie files. `11_Backlog` added for mid-term task management.

## 🚀 Quick Start

### 1. Clone this repo
```bash
git clone https://github.com/perfhelf/memory-system.git
```

### 2. Customize the system
- Edit `00_系统说明_README.md` → set your AI persona, user profile, and preferences
- Edit `07_项目开发规则_DevRules.md` → add your project-specific coding rules

### 3. Update file paths
Replace all `/path/to/记忆系统/` in workflow files (`.agents/workflows/*.md`) with your actual local clone path.

### 4. Register workflows
Point your AI platform's slash-command system to the `.agents/workflows/` directory:
- `/memory` → `memory.md` (cold boot)
- `/end` → `end.md` (archiving)
- `/call` → `call.md` (deep integration)
- `/env` → `env.md` (key management)

### 5. Boot it up
Type `/memory` in your AI conversation. The system will cold-boot and load your full context.

### 6. Start building knowledge
As you work with your AI, it will automatically populate:
- `10_当前焦点_Focus.md` — active tasks
- `11_待办事项_Backlog.md` — mid-term backlog
- `20_项目知识库_Projects/` — project-specific knowledge
- `30_核心领域_Domains/` — domain expertise
- `99_对话存档_Logs/` — conversation summaries

## 🏗️ Design Principles

1. **Physical Storage > Chat History** — Files on disk survive any platform migration
2. **High Compression** — Every section ≤ 400 tokens for surgical retrieval
3. **Hot/Cold Tiering** — Recent = Focus, Aging = Logs, Permanent = Domains
4. **No-Ask Archiving** — AI writes silently, never interrupts to ask "should I save this?"
5. **No Orphan Files** — Every file must be read or written by at least one workflow
6. **Monthly Evolution** — System reviews itself on the 1st of every month

## 🌐 Language

This system was designed in **Chinese (中文)**. The framework is fully functional in any language — simply translate the templates to your preferred language.

## 📋 Changelog

| Version | Date | Changes |
| :--- | :--- | :--- |
| **v1.5** | 2026-03-02 | Zombie audit: merged 02-05 into README; neural network topology with bidirectional refs; `/call` deep integration workflow |
| **v1.4** | 2026-03-01 | Added `11_Backlog.md` for mid-term tasks |
| **v1.3** | 2026-02-27 | Claude benchmark: `/memory` + DevRules + Focus 60-line cap + AutoMemory |
| **v1.2** | 2026-02-26 | Deep distillation: project knowledge base + domain knowledge |
| **v1.0** | 2026-02-26 | Initial skeleton |

## 📄 License

MIT License — See [LICENSE](./LICENSE)

## 🤝 Contributing

Issues and PRs welcome. If you've adapted this system for a different AI platform, share your workflow!
