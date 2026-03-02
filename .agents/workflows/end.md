---
description: 终局归档 — 一条命令触发对话结束归档协议
---

# /end — 终局归档协议

当用户输入 `/end` 或 `结束对话` 时，执行以下步骤：

// turbo-all

## 步骤

1. 读取归档法则（确认 SOP）
```
view_file /path/to/记忆系统/06_终局归档法则_Archiving.md
```

2. 读取当前焦点（确认哪些任务需标记完成）
```
view_file /path/to/记忆系统/10_当前焦点_Focus.md
```

3. 读取中期待办（确认哪些 Backlog 项需标记完成或新增）
```
view_file /path/to/记忆系统/11_待办事项_Backlog.md
```

4. 读取本次涉及的项目知识卡（根据对话内容判断）
   - 如果涉及项目A → `view_file 20_Projects/项目A.md` → 检查里程碑是否需更新
   - 以此类推

5. 执行归档 SOP（按 06_终局归档法则）：
   - **Step 1 缓存扫描**: 回顾本次对话产生的临时决议和新规则
   - **Step 2 全系统智能同步**: 
     - 更新 `10_Focus.md` → 标记完成/写入新任务
     - 更新 `11_Backlog.md` → 标记完成/写入新中期任务
     - 更新 `20_Projects/相关项目.md` → 里程碑/架构决策变更
     - 更新 `30_Domains/相关领域.md` → 新的领域知识固化
   - **Step 3 提纯入库**: 紧急→Focus, 不急→Backlog, 共识→Projects/Domains
   - **Step 4 日志封存**: 在 `99_Logs/01_Week/` 生成 `YYYY-MM-DD_主题.md`
   - **Step 5 汇报退场**: 向用户汇报归档结果并正式结束

6. 汇报格式：
   - ✅ 哪些 Focus/Backlog 任务被标记完成
   - ➕ 哪些新任务被写入
   - 🔄 哪些 Projects/Domains 文件被更新
   - 📝 日志封存路径
