---
tags: 
alias: 
date: 2025-08-03 19:43
---


[[find how]]'需要通过[[管道符]],标准输出变成输入

```shell
find documents \(-name "*.pdf" -o -name ".doc"\) |xargs grep -i 'important'
```

