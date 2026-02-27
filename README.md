# 🧠 AI Persistent Memory System

A **physical-file-based, version-controllable, structured** persistent memory system designed for AI assistants (Claude, GPT, Gemini, etc.) that lack built-in long-term memory.

## 🤔 Why This Exists

Every AI conversation starts from zero. Chat history gets lost, context windows overflow, and institutional knowledge evaporates. This system solves that by maintaining a **Markdown-based memory vault** on your local filesystem that your AI can read and write to across sessions.

**Core philosophy**: If the AI can read files, it can remember everything.

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| **One-Command Cold Boot** | Single `/memory` command loads full context in seconds |
| **Hot/Warm/Cold Tiering** | Automatic memory aging: Focus → Weekly → Monthly → Archive |
| **High Compression** | Every chunk ≤ 400 tokens for precise retrieval |
| **Auto-Memory Write** | AI silently archives valuable info during conversations |
| **End-of-Session Archiving** | Forced knowledge distillation on conversation close |
| **Monthly Self-Upgrade** | Built-in protocol for structural evolution |
| **Skill Retrieval** | Index of technical skills the AI must consult before coding |
| **Key Management** | Centralized secret/token registry (AI reads keys, never asks you) |
| **Project Dev Rules** | Centralized coding conventions per project |

## 📂 Directory Structure

```
记忆系统/
├── 00_系统说明_README.md          # System rules & SOUL protocol
├── 01_核心索引_Index.md           # Global navigation hub
├── 02_用户画像_USER.md            # Your profile & preferences
├── 03_记忆系统升级_Upgrade.md     # Monthly upgrade protocol
├── 04_技能记忆检索系统_Skills.md  # Skill retrieval index
├── 05_文档整理_Documenting.md     # Formatting & style rules
├── 06_终局归档法则_Archiving.md   # End-of-session archiving SOP
├── 07_项目开发规则_DevRules.md    # Per-project coding rules
├── 08_自动记忆写入_AutoMemory.md  # Auto-write protocol
├── 10_当前焦点_Focus.md           # Current tasks & priorities
├── 20_项目知识库_Projects/        # Project knowledge cards
├── 30_核心领域_Domains/           # Domain expertise vault
├── 99_对话存档_Logs/              # Conversation logs (hot/warm/cold)
├── 秘钥文档/                      # Secret & key registry
└── .agents/workflows/memory.md    # Cold-boot workflow
```

## 🚀 Quick Start

### 1. Clone this repo
```bash
git clone https://github.com/bigfishmarquis/memory-system.git
```

### 2. Customize your profile
Edit `02_用户画像_USER.md` with your identity, interests, and tech preferences.

### 3. Register the `/memory` workflow
Point your AI's workflow/slash-command system to `.agents/workflows/memory.md`. Update the file paths inside to match your local clone location.

### 4. Boot it up
Type `/memory` in your AI conversation. The system will cold-boot and load your full context.

### 5. Start building knowledge
As you work with your AI, it will automatically populate:
- `10_当前焦点_Focus.md` — active tasks
- `20_项目知识库_Projects/` — project-specific knowledge
- `30_核心领域_Domains/` — domain expertise
- `99_对话存档_Logs/` — conversation summaries

## 🏗️ Design Principles

1. **Physical Storage > Chat History** — Files on disk survive any platform migration
2. **High Compression** — Every section ≤ 400 tokens for surgical retrieval
3. **Hot/Cold Tiering** — Recent = Focus, Aging = Logs, Permanent = Domains
4. **No-Ask Archiving** — AI writes silently, never interrupts to ask "should I save this?"
5. **Monthly Evolution** — System reviews itself on the 1st of every month

## 🌐 Language

This system was originally designed in **Chinese (中文)** and the file names use Chinese for the author's personal workflow. The framework is fully functional in any language — simply translate the templates to your preferred language.

## 📄 License

MIT License — See [LICENSE](./LICENSE)

## 🤝 Contributing

Issues and PRs welcome. If you've adapted this system for a different AI platform, share your workflow!
