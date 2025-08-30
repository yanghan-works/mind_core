---
tags: 
alias: 
date: 2025-08-30 13:47
---
**核心原则**: **永远先用 `conda`，不行再用 `pip`**。

### 常用命令

1. **安装包**: _必须先用 `conda activate` 进入指定环境再操作。_
    
```
# 优先使用 conda，可以一次安装多个
conda install pandas numpy matplotlib jupyterlab
    
# 当 conda 官方渠道找不到某个包时，才轮到 pip
pip install some-small-package
```
    
2. **查看当前环境已安装的包**: 盘点厨房里的工具。
    
```
conda list
```
    

### 为什么优先 `conda`?

- `conda` 会在安装前检查所有包（包括非 Python 包）之间的依赖关系，进行全局规划，避免冲突。
    
- `pip` 只关心 Python 包的依赖，它鲁莽的安装行为可能会破坏 `conda` 辛辛苦苦维护好的依赖平衡。
    