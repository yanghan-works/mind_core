---
tags: 
alias: 
date: 2025-08-30 07:53
---
### `pip`：你的Python项目管家

`pip` 是 Python 的包管理工具，负责安装、升级、卸载和管理软件包。把它看作是你管理项目依赖的“工具采购和清单管理”助理。

#### 核心命令速查

1. **安装包**：从 PyPI（Python Package Index）仓库下载并安装包。
    
    - `pip install <包名>`
        
    - `pip install <包名>==<版本号>` （安装特定版本）
        
    - `pip install <包名>>=<版本号>` （安装不低于某个版本的包）
        
2. **管理已安装的包**：
    
    - `pip list`：列出所有已安装的包。
        
    - `pip show <包名>`：显示特定包的详细信息，如版本、作者、许可证等。
        
3. **升级和卸载**：
    
    - `pip install --upgrade <包名>`：升级包到最新版本。
        
    - `pip uninstall <包名>`：卸载包。
        

#### 项目依赖管理

为了确保你的项目在不同环境中都能正常运行，你需要管理依赖关系。

- **`requirements.txt`**：一个文本文件，用于记录项目的所有依赖及其版本。
    
- `pip freeze > requirements.txt`：将当前环境中的所有包及其版本“冻结”并保存到 `requirements.txt` 文件中。
    
- `pip install -r requirements.txt`：根据 `requirements.txt` 文件中的清单，一键安装所有依赖。
    

#### 高效配置

默认的 PyPI 仓库在某些地区可能访问缓慢。配置一个镜像仓库可以大幅提升下载速度。

- **临时使用**：`pip install <包名> -i <镜像地址>`
    
- **永久配置**：创建或修改 `pip` 配置文件（`pip.ini` 或 `pip.conf`），在其中指定默认镜像地址。
    

**配置文件的具体内容**

```
[global]
index-url = <镜像地址>
trusted-host = <镜像地址的主机名，不含http(s)://>
```

**常用镜像地址示例**

- **清华大学**：
    
    - `https://pypi.tuna.tsinghua.edu.cn/simple`
        
    - `trusted-host = pypi.tuna.tsinghua.edu.cn`
        
- **阿里云**：
    
    - `https://mirrors.aliyun.com/pypi/simple`
        
    - `trusted-host = mirrors.aliyun.com`
        
- **豆瓣**：
    
    - `https://pypi.doubanio.com/simple`
        
    - `trusted-host = pypi.doubanio.com`
        

#### 常见工具依赖

`pip` 本身也依赖一些工具才能顺利工作。

- **`setuptools`**：用于处理源代码包的安装。
    
- **`wheel`**：一种预编译的包格式，能让安装过程更快速、更稳定。
    

#### 终极心智模型

**`pip` = 工具采购 + 项目清单管理**。掌握它，你就掌握了 Python 开发协作的基础。