---
tags:
  - Linux
  - 命令
  - grep
aliases: 
date: 2025-08-03 19:55
---

## 基本正则

搜索模式使用[[正则表达式]]即可

正则表达式解决了模糊匹配

```shell
grep [选项] '搜索模式' [文件名]
```



## `grep -E` 开启扩展正则

```
grep -E 'error|warning' log.txt
```