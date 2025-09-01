---
tags: 
alias: 
date: 2025-09-01 08:11
---


## 1. 基础概念

- **包 (Package)**：包含模块（`.py` 文件）的目录，通常含有 `__init__.py` 文件。
    
- **模块 (Module)**：一个 `.py` 文件，包含 Python 代码。
    
- **pip**：Python 的包安装程序，用于安装、升级和删除 Python 包。
    
- **PyPI (Python Package Index)**：官方的第三方 Python 包仓库。
    

## 2. 常用命令

### 2.1 包管理

- **安装包**
    
    - `pip install <包名>`：安装单个包。
        
    - `pip install <包名>==<版本号>`：安装指定版本的包。
        
    - `pip install -r requirements.txt`：从文件中批量安装包。
        
    - `pip install --upgrade <包名>`：升级包。
        
    - `pip install -e .`：以可编辑模式安装本地项目。
        
- **卸载包**
    
    - `pip uninstall <包名>`：卸载单个包。
        
- **查看包**
    
    - `pip list`：列出所有已安装的包。
        
    - `pip show <包名>`：显示包的详细信息。
        
    - `pip check`：检查已安装包的依赖关系。
        

### 2.2 搜索与文件

- **搜索包**
    
    - `pip search <关键词>`：在 PyPI 上搜索包（注意：此功能已在较新版本中移除）。
        
- **生成 requirements 文件**
    
    - `pip freeze > requirements.txt`：生成当前环境中所有包及其版本的列表。
        

## 3. 虚拟环境

- **概念**：独立的 Python 环境，可以为每个项目创建独立的依赖，避免包冲突。
    
- **创建**
    
    - `python -m venv <环境名>`：使用 `venv` 模块创建虚拟环境。
        
- **激活/进入**
    
    - **Windows**：`<环境名>\Scripts\activate`
        
    - **macOS/Linux**：`source <环境名>/bin/activate`
        
- **退出**
    
    - `deactivate`
        
- **使用**
    
    - 激活环境后，所有 `pip install` 和 `python` 命令都将作用于当前虚拟环境。
        

## 4. 进阶用法

- **镜像源 (Mirror)**
    
    - `pip install -i <镜像源地址> <包名>`：使用指定的镜像源安装包。
        
    - **配置国内镜像源**（例如清华源）：`pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`
        
- **离线安装**
    
    - **下载包**：`pip download <包名>`
        
    - **离线安装**：`pip install --no-index --find-links=<下载目录> <包名>`
        

## 5. 常见问题

- **版本冲突**：当不同的包需要同一依赖的不同版本时。使用虚拟环境是最佳解决方案。
    
- **权限问题**：在某些系统上，全局安装可能需要管理员权限。推荐使用虚拟环境或 `pip install --user`。
    
- **安装失败**：检查网络连接、镜像源、依赖包是否正确。