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