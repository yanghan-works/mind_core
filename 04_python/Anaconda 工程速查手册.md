---
tags:
  - python
  - 工具
alias:
date: 2025-08-30 13:58
---
## 1. 核心原则：环境隔离 (The Core Principle)

Anaconda 的唯一价值在于为每个项目创建一个**独立、干净、互不干扰**的虚拟环境。这能从根源上避免不同项目间的依赖冲突。

- **`conda` vs `pip` 定位**:
    
    - `conda`：**系统级总管**。负责管理**环境**（包含特定Python版本）与**跨语言包**。
        
    - `pip`：**环境内助理**。只负责管理当前激活环境下的 **Python 专用包**。
        

## 2. 日常工作流命令 (Daily Workflow)

这是你为任何新项目启动的标准操作程序（SOP）。

```shell
# 步骤 1: 创建一个全新的、隔离的环境
# 格式: conda create --name <环境名> python=<版本号>
conda create --name project_x python=3.10

# 步骤 2: 激活并进入该环境
# 格式: conda activate <环境名>
conda activate project_x
# 成功后，命令行提示符前缀会变为 (project_x)

# 步骤 3: 在新环境中安装必要的库
# 格式: conda install <库1> <库2> ...
conda install pandas numpy jupyterlab

# 步骤 4: 启动开发工具并开始工作
jupyter lab

# 步骤 5: 工作完成，离开环境
conda deactivate
```

## 3. 环境与包管理速查 (Cheatsheet)

### 3.1 环境管理 (Environments)

|功能|命令|
|---|---|
|**创建**新环境|`conda create --name <env_name> python=x.x`|
|**激活**环境|`conda activate <env_name>`|
|**离开**环境|`conda deactivate`|
|**列出**所有环境|`conda env list`|
|**删除**指定环境|`conda remove --name <env_name> --all`|

### 3.2 包管理 (Packages)

|功能|命令|
|---|---|
|**安装包 (conda)**|`conda install <pkg_name>` **(首选)**|
|**安装包 (pip)**|`pip install <pkg_name>` **(备选)**|
|**列出**当前环境的包|`conda list`|
|**搜索**可用的包|`conda search <pkg_name>`|

## 4. 一次性环境配置 (One-Time Setup)

为了获得最佳的下载速度和最全的软件包，建议对 `conda` 进行一次性全局配置。

```shell
# 步骤 1: 添加社区维护的最全渠道 conda-forge
conda config --add channels conda-forge

# 步骤 2: 设置渠道优先级为“严格”，确保优先使用 conda-forge
conda config --set channel_priority strict
```

## 5. 紧急排错手册 (Troubleshooting)

| 问题症状                                     | 核心原因与解决方案                                                                                 |
| ---------------------------------------- | ----------------------------------------------------------------------------------------- |
| **`conda` 命令无效**                         | **原因**: 环境变量缺失。<br>**方案**: **使用 "Anaconda Prompt"** 而不是系统自带的 `cmd`。                       |
| **安装时卡在 `Solving...`**                   | **原因**: 网络连接下载源缓慢。<br>**方案**: **执行第4点的“一次性环境配置”**，更换为更快的渠道。                               |
| **`jupyter lab` 能运行，但 `conda list` 中没有** | **原因**: “幽灵依赖”，调用了 `base` 环境的程序。<br>**方案**: **激活正确的环境后，重新执行** `conda install jupyterlab`。 |