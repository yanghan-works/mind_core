---
tags: 
alias: 
date: 2025-08-30 07:53
---
`pip` 是 Python 的包管理工具，负责安装、升级、卸载和管理软件包。把它看作是你管理项目依赖的“工具采购和清单管理”助理。

## 核心命令与实践

- **安装包**：从 PyPI（Python Package Index）这个“巨大零件仓库”下载并安装包。
    
    - `pip install <包名>`
        
        - **案例**：想让你的程序拥有人脸识别能力？安装 `opencv-python` 这个“智能芯片”，命令是 `pip install opencv-python`。
            
    - **💡 我的实践**：我喜欢在虚拟环境中安装包，这样可以保持项目依赖的隔离，避免版本冲突。
        
- **管理已安装的包**：
    
    - `pip list`：列出所有已安装的包，就像你的助理在清点你的工具箱。
        
    - `pip show <包名>`：显示特定包的详细信息，如版本、作者、许可证等。
        
- **升级和卸载**：
    
    - `pip install --upgrade <包名>`：升级包到最新版本。
        
        - **案例**：如果你的 `requests` 包有了新功能，用这个命令来将它“升级”到最新版本。
            
    - `pip uninstall <包名>`：卸载包。
        

## 项目依赖管理：`requirements.txt`

`requirements.txt` 是项目的“零件清单”，记录了所有依赖及其版本。这对于在不同环境中复现项目至关重要。

- **创建清单**：使用 `pip freeze > [[requirements.txt]]` 命令，将当前环境中的所有包及其版本“冻结”并保存到文件中。
    
- **安装清单**：使用 `pip install -r [[requirements.txt]]`，根据清单一键安装所有依赖。
    
    - **💡 我的实践**：当我需要将项目分享给同事或部署到服务器上时，这两条命令是我的“黄金搭档”，确保了环境的一致性。
        

## 高效配置：加速 `pip`

默认的 PyPI 仓库在某些地区可能访问缓慢，配置一个镜像仓库可以大幅提升下载速度。

- **临时使用**：`pip install <包名> -i <镜像地址>`
    
- **永久配置**：创建或修改 `pip` 配置文件（`pip.ini` 或 `pip.conf`），在其中指定默认镜像地址。
    

**配置文件的具体内容**

```
[global]
index-url = [https://pypi.tuna.tsinghua.edu.cn/simple](https://pypi.tuna.tsinghua.edu.cn/simple)
trusted-host = pypi.tuna.tsinghua.edu.cn
```

**不同操作系统下的配置步骤**

1. **Windows**
    
    - 在文件管理器地址栏输入 `%APPDATA%` 并回车。
        
    - 在打开的文件夹中，创建一个名为 `pip` 的新文件夹。
        
    - 在 `pip` 文件夹中，创建一个名为 `pip.ini` 的新文件。
        
    - 用记事本或其他文本编辑器打开 `pip.ini`，将上面的配置文件内容复制进去并保存。
        
2. **macOS 和 Linux**
    
    - 打开终端。
        
    - 执行以下命令创建所需的文件夹和文件：
        
        ```
        mkdir -p ~/.config/pip/
        touch ~/.config/pip/pip.conf
        ```
        
    - 用你喜欢的文本编辑器（如 `vim`、`nano` 或 `code`）打开 `pip.conf` 文件，并将上面的配置文件内容复制进去并保存。
        

**常用镜像地址示例**：

- **清华大学**：`https://pypi.tuna.tsinghua.edu.cn/simple`
    
- **阿里云**：`https://mirrors.aliyun.com/pypi/simple`
    
- **豆瓣**：`https://pypi.doubanio.com/simple`
    

## 核心工具依赖

`pip` 本身也依赖一些工具才能顺利工作。

- `[[setuptools]]`：用于处理源代码包的安装，就像你的“螺丝刀”。
    
- `[[wheel]]`：一种预编译的包格式，能让安装更快速、更稳定，就像一个“预组装的乐高积木”。
    

## 终极心智模型

**`pip` = 工具采购 + 项目清单管理**。掌握它，你就掌握了 Python 开发协作的基础。