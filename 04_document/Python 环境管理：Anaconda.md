---
tags: 
alias: 
date: 2025-09-01 08:53
---
## 1. 基础概念

- **Anaconda**：一个包含 Conda、Python 和大量科学计算包（如 NumPy、Pandas）的发行版。
    
- **Miniconda**：Anaconda 的精简版，只包含 Conda 和 Python，用户可按需安装其他包。
    
- **Conda**：Anaconda 的核心包和环境管理器。
    
- **环境 (Environment)**：一个独立的、隔离的 Conda 目录，包含特定版本的 Python 和包。
    

## 2. Conda 常用命令

### 2.1 环境管理

- **创建环境**
    
    - `conda create --name <环境名>`：创建一个新环境，默认不包含任何包。
        
    - `conda create -n <环境名> python=3.9`：创建一个包含指定 Python 版本的环境。
        
    - `conda create -n <环境名> python=3.9 numpy pandas`：创建并安装指定包。
        
- **激活/进入环境**
    
    - `conda activate <环境名>`
        
- **退出环境**
    
    - `conda deactivate`
        
- **查看环境**
    
    - `conda env list`：列出所有已创建的环境。
        
- **复制环境**
    
    - `conda create -n <新环境名> --clone <旧环境名>`
        
- **删除环境**
    
    - `conda remove -n <环境名> --all`
        

### 2.2 包管理

- **安装包**
    
    - `conda install <包名>`
        
    - `conda install <包名>==<版本号>`
        
    - `conda install -c <频道名> <包名>`：从指定频道安装包。
        
- **更新包**
    
    - `conda update <包名>`：更新指定包。
        
    - `conda update --all`：更新环境中所有包。
        
- **移除包**
    
    - `conda remove <包名>`
        
- **查看包**
    
    - `conda list`：列出当前环境中已安装的包。
        
- **搜索包**
    
    - `conda search <包名>`：在 Conda 频道中搜索包。
        

## 3. Conda 与 pip 的关系

- **区别**：
    
    - **Conda**：跨语言的包和环境管理器，可以处理非 Python 依赖（如 CUDA）。
        
    - **pip**：Python 语言的包管理器，专注于 Python 包的安装。
        
- **最佳实践**：
    
    - 优先使用 `conda install` 来安装主流的科学计算包（如 NumPy, SciPy, Pandas）。
        
    - 如果 Conda 频道没有需要的包，再使用 `pip install`。
        
    - 避免在 Conda 环境中混用 `conda` 和 `pip` 来安装相同的包，以防止版本冲突。
        

## 4. 为什么使用 Anaconda

- **环境隔离**：为每个项目创建独立的沙箱，避免依赖冲突。
    
- **科学计算支持**：预装了大量用于数据分析、机器学习的库，开箱即用。
    
- **二进制兼容性**：提供预编译的二进制包，可以解决在不同操作系统上编译依赖库的难题。
    
- **频道管理**：可以通过添加不同的频道（如 `conda-forge`）来获取更丰富的包资源。