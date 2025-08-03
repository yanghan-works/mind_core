---
tags: 
alias: 
date: 2025-08-03 19:43
---


find'需要通过管道符标准输出变成输入，传递给grep

```shell
find documents \(-name "*.pdf" -o -name ".doc"\) |xargs grep -i 'important'
```

