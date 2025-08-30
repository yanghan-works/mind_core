---
tags: 
alias: 
date: 2025-08-30 13:44
---
**核心目的**: 为每个项目创建隔离的“厨房”。这是 Anaconda 最核心的功能。

### 常用命令 (三板斧)

1. **创建环境**: 新建一个厨房，并指定 Python 版本。
    
```
# 模板: conda create --name <环境名> python=x.x
conda create --name data_analysis python=3.10
```
    
2. **激活/进入环境**: 走进厨房。
    
```
conda activate <环境名>
```
    
    _激活后，命令行提示符会变为 `(<环境名>)`，这是你的路标。_
    
3. **离开环境**:
    
```
conda deactivate
```
    
4. **删除环境**: 彻底拆掉没用的厨房。
    
```
# --all 参数会删除环境下的所有东西
conda remove --name <环境名> --all
```
    
5. **查看所有环境**:
    
```
conda env list
```
    

**关联**: [[Conda 常见问题排查]]