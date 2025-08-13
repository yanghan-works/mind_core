---
excalidraw-plugin: parsed
tags:
  - excalidraw
  - Linux
  - 命令
---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'



# grep

·```shel

```

# Code Block

```shell
https://github.com/yanghan-works/Obsidian-Vault.git
```


# Code Block

```shell
grep 
```


# Code Block 1

```shell
#!/bin/bash
# GREP CORE USAGE CHEATSHEET
# 复制粘贴到你的终端或脚本中使用

# ----------------------------------------------------
# 剧本一：基础查找 (大海捞针)
# 场景：检查系统日志文件 system.log 中是否包含任何 "Error" 记录。
grep "Error" system.log

# ----------------------------------------------------
# 剧本二：忽略大小写 (-i)
# 场景：在配置文件 config.ini 中查找 "user" 相关的设置，不确定它是 user, User, 还是 USER。
grep -i "user" config.ini

# ----------------------------------------------------
# 剧本三：反向匹配 (-v)
# 场景：查看当前所有正在运行的进程，但过滤掉由 grep 自己产生的那个进程，让输出更干净。
ps aux | grep -v "grep"

# ----------------------------------------------------
# 剧本四：递归搜索 (-r)
# 场景：在一个巨大的代码项目 /path/to/project 中，查找数据库URL是在哪个文件里定义的。
grep -r "DATABASE_URL" /path/to/project

# ----------------------------------------------------
# 剧本五：显示行号 (-n)
# 场景：程序构建日志 build.log 提示有 "Invalid syntax" 错误，需要快速定位到具体是哪一行。
grep -n "Invalid syntax" build.log

# ----------------------------------------------------
# 剧本六：统计数量 (-c)
# 场景：怀疑网站被攻击，需要快速统计 access.log 中，某个恶意IP "123.45.67.89" 的访问次数。
grep -c "123.45.67.89" access.log

# ----------------------------------------------------
# 剧本七：扩展正则 - 或逻辑 (-E)
# 场景：需要同时检查系统日志 messages 中所有 "Error" (错误) 和 "Warning" (警告) 的记录。
grep -E "Error|Warning" /var/log/messages

# ----------------------------------------------------
# 组合技一：列出文件 + 查找特定权限
# 场景：在当前目录下，找出所有权限为 "rwx" (可读可写可执行) 的文件或目录。
ls -l | grep "rwx"

# ----------------------------------------------------
# 组合技二：只关心文件名 (-l)
# 场景：在项目 src/ 目录下，找出所有导入了 "import requests" 这个库的Python文件名。
grep -r -l "import requests" ./src
```


# Code Block 2

```shell
#!/bin/bash
# GREP CORE USAGE CHEATSHEET
# 复制粘贴到你的终端或脚本中使用

# ----------------------------------------------------
# 剧本一：基础查找 (大海捞针)
# 场景：检查系统日志文件 system.log 中是否包含任何 "Error" 记录。
grep "Error" system.log

# ----------------------------------------------------
# 剧本二：忽略大小写 (-i)
# 场景：在配置文件 config.ini 中查找 "user" 相关的设置，不确定它是 user, User, 还是 USER。
grep -i "user" config.ini

# ----------------------------------------------------
# 剧本三：反向匹配 (-v)
# 场景：查看当前所有正在运行的进程，但过滤掉由 grep 自己产生的那个进程，让输出更干净。
ps aux | grep -v "grep"

# ----------------------------------------------------
# 剧本四：递归搜索 (-r)
# 场景：在一个巨大的代码项目 /path/to/project 中，查找数据库URL是在哪个文件里定义的。
grep -r "DATABASE_URL" /path/to/project

# ----------------------------------------------------
# 剧本五：显示行号 (-n)
# 场景：程序构建日志 build.log 提示有 "Invalid syntax" 错误，需要快速定位到具体是哪一行。
grep -n "Invalid syntax" build.log

# ----------------------------------------------------
# 剧本六：统计数量 (-c)
# 场景：怀疑网站被攻击，需要快速统计 access.log 中，某个恶意IP "123.45.67.89" 的访问次数。
grep -c "123.45.67.89" access.log

# ----------------------------------------------------
# 剧本七：扩展正则 - 或逻辑 (-E)
# 场景：需要同时检查系统日志 messages 中所有 "Error" (错误) 和 "Warning" (警告) 的记录。
grep -E "Error|Warning" /var/log/messages

# ----------------------------------------------------
# 组合技一：列出文件 + 查找特定权限
# 场景：在当前目录下，找出所有权限为 "rwx" (可读可写可执行) 的文件或目录。
ls -l | grep "rwx"

# ----------------------------------------------------
# 组合技二：只关心文件名 (-l)
# 场景：在项目 src/ 目录下，找出所有导入了 "import requests" 这个库的Python文件名。
grep -r -l "import requests" ./src
```

# Excalidraw Data

## Text Elements
匹配的行 ^e3hl5to4

输入 ^hALf224y

过滤 ^03GVNoHx

[[管道]] ^DlA9P6VJ

输入 ^DvjqeXAa

上个命令的结果 ^mFyV21Up

输出 ^OJ81JpaJ

-v 反向匹配
-i 忽略大小写
-r 递归搜索，整个文件夹中查找
-n 显示行号
-c 显示匹配到的行数总和 ^tdsv2cEG

"匹配模式" ^bYyl8owV

! ^Z8cJrSl5

文件A ^zld1TcRz

文件B ^tcl2Kbr5

输入 ^J1nVqTay

[[正则表达式]] ^fc9sUE8L

-E 开启拓展正则表达式 ^cW3WpZuV

文本内容 ^7PywISbm

## Element Links
oZXnGSdZ: [[grep Drawing 2025-08-04 15.25.10.excalidraw.md#Code Block 2]]

## Embedded Files
5a9baa39cd389e3ac7407f63824e244cbfd9cef3: [[Pasted Image 20250804152605_792.png]]

%%
## Drawing
```compressed-json
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
```
%%