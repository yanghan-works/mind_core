---
tags:
  - python
  - pip
  - 工具
alias: pip,python包管理工具
date: 2025-08-30 07:53
---
## 1. pip 是什么？

`pip` 是 **Python 包管理工具**（**P**ackage **I**nstaller for **P**ython），它是官方推荐的用于安装和管理 Python 软件包的工具。

## 2. 常用命令速查

|命令|描述|示例|
|---|---|---|
|**`install`**|安装一个或多个包。|`pip install requests`|
|**`uninstall`**|卸载一个或多个包。|`pip uninstall requests`|
|**`list`**|列出所有已安装的包。|`pip list`|
|**`show`**|显示某个包的详细信息。|`pip show requests`|
|**`freeze`**|列出所有已安装的包及其版本，常用于生成 `requirements.txt` 文件。|`pip freeze > requirements.txt`|
|**`search`**|在 PyPI 上搜索包。|`pip search requests`|
|**`check`**|检查已安装的包是否存在不兼容的依赖。|`pip check`|

## 3. requirements.txt

`requirements.txt` 是一个文本文件，用于记录项目所依赖的所有 Python 包及其精确版本。

### 3.1 生成 requirements.txt

将当前环境中已安装的包列表输出到文件中。

```
pip freeze > requirements.txt
```

### 3.2 安装 requirements.txt 中的包

在新的环境中，根据 `requirements.txt` 文件一次性安装所有依赖。

```
pip install -r requirements.txt
```

## 4. 虚拟环境（Virtual Environment）

虚拟环境是一个独立于系统全局 Python 环境的目录。每个虚拟环境都可以拥有自己的 Python 解释器和独立的 `pip` 包集。

### 4.1 为什么要使用虚拟环境？

- **隔离性：** 防止不同项目之间的包依赖冲突。
    
- **可移植性：** 方便在不同机器上复现相同的项目环境。
    

### 4.2 使用 venv

Python 3.3 及以上版本内置了 `venv` 模块，是创建虚拟环境的推荐方式。

- **创建虚拟环境**
    

```
python3 -m venv myenv
```

- **激活虚拟环境**
    
    - 在 **macOS/Linux** 上：
        
        ```
        source myenv/bin/activate
        ```
        
    - 在 **Windows** 上：
        
        ```
        myenv\Scripts\activate
        ```
        
- **退出虚拟环境**
    

```
deactivate
```

## 5. 常见问题与技巧

### 5.1 更换国内镜像源

默认的 `pip` 源在国外，下载速度较慢。可以通过以下命令临时或永久更换为国内镜像源（如清华大学、阿里云等）。

- **临时使用**
    
```
pip install some-package -i [https://pypi.tuna.tsinghua.edu.cn/simple](https://pypi.tuna.tsinghua.edu.cn/simple)
```

- **永久配置**
    
    - **Windows:** 在用户目录下创建 `pip` 文件夹，再在该文件夹下创建 `pip.ini` 文件，并添加以下内容：
        
```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
```
        
    - **macOS/Linux:** 在用户目录下创建 `.pip` 文件夹，再在该文件夹下创建 `pip.conf` 文件，并添加以下内容：
		
```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
```
        

### 5.2 指定版本安装

可以通过 `==`、`>=`、`<=` 等符号指定包的版本。

- **安装精确版本**
    

```
pip install some-package==1.2.3
```

- **安装指定版本以上**
    

```
pip install some-package>=1.2.3
```

### 5.3 升级 pip

保持 `pip` 工具本身为最新版本是一个好习惯。

```
python3 -m pip install --upgrade pip
```