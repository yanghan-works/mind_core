---
tags:
  - Linux
  - 命令
  - grep
aliases: 
date: 2025-08-04 07:56
---
## 基本思想 

其核心逻辑是：**前一个命令产生输出 -> 管道将输出传递 -> `grep` 对接收到的输出进行过滤**。

## 常见用例

- 查找当前目录下所有的 `.md` Markdown 文件

```shell
ls -l | grep "\.md$"
```

- 查找进程

```shell
ps aux | grep "nginx"
```

- 在命令历史中搜索

```shell
history | grep "docker"
```

- 分析日志文件

```shell
cat /var/log/syslog | grep "error"
```

- 