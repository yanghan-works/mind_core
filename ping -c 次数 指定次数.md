---
tags:
  - Ping
  - Linux
  - 网络故障排查
  - 命令
aliases: 
date: 2025-08-03 17:54
---

`-c` 选项可以让你指定要发送多少个 `ping` 数据包。`c` 就是 count (数量) 的意思

**语法：** `ping -c [数量] [目标地址]`


```shell
ping -c 5 8.8.8.8
```