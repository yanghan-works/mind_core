---
# 如何定义 Rust 结构体

tags:
  - rust
alias:
date: 2025-08-26 10:26
---
```mermaid
graph TD subgraph "输入" Pattern["模式<br>(正则表达式)"] Files["文件"] Options["选项"] end subgraph "grep 工作流" ReadInput[读取文件内容] --> ApplyPattern[应用模式] ApplyPattern --> Filter[过滤不匹配行] Filter --> PrintOutput[打印匹配行] end subgraph "常见选项" Options --> CaseInsensitive["-i<br>(忽略大小写)"] Options --> Recursive["-r<br>(递归搜索)"] Options --> InvertMatch["-v<br>(反向匹配)"] Options --> LineNumber["-n<br>(显示行号)"] end grep["grep"] -- 组合 --> Pattern grep -- 组合 --> Files grep -- 组合 --> Options grep -- 执行 --> ReadInput PrintOutput -- 产生 --> Output["匹配结果"]
```