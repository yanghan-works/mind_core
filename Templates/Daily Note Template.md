---
# --- 元数据区：你的第二大脑引擎 ---
# 本区域为 Dataview 和 Obsidian 提供动力，请勿轻易修改。
type: daily-note
tags: [daily, dn]
date: <% tp.file.title %>
aliases: 
  - "<% tp.date.now("MMMM Do", 0, tp.file.title, "YYYY-MM-DD") %>"
  - "<% tp.date.now("YYYY年M月D日", 0, tp.file.title, "YYYY-MM-DD") %>"
week: <% tp.date.now("YYYY-[W]ww", 0, tp.file.title, "YYYY-MM-DD") %>
month: <% tp.date.now("YYYY-MM", 0, tp.file.title, "YYYY-MM-DD") %>

---

# 🗓️ <% tp.file.title %> | <% tp.date.now("dddd", 0, tp.file.title, "YYYY-MM-DD") %>

> [!quote] 真正重要的不是你写了多少，而是你连接了多少。

---

## 🌊 意识流 & 速记 <!-- 记录任何想法，用快捷键生成新时间戳 -->
- <% tp.date.now("HH:mm") %> <% tp.file.cursor() %>

---

## ✅ 今日要务 <!-- 你的三件要事，可链接至 [[项目]] 或 [[会议]] -->
- [ ] 
- [ ] 
- [ ] 

---

## 🌱 今日复盘 <!-- 每日反思，是明日成长的燃料 -->
- **一件完成得不错的事：**
- **学到的新知识/想法（建议链接）：** [[ ]]
- **一个可以改进的地方：**

---

## 🤖 自动连接中心 <!-- 本区域由 Dataview 插件自动更新！-->

### 今天的足迹 (Notes created/edited today)

```dataview
LIST
FROM ""
WHERE file.cday = this.file.day OR file.mday = this.file.day
SORT file.mtime desc
````

### 谁在呼唤我 (Backlinks to this note)

```dataview
LIST FROM [[]]
WHERE file.name != this.file.name
SORT file.mtime desc
```

[[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|⬅️ 昨日]] | [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|明日 ➡️]]