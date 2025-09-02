# pip

**pip** (Pip Installs Packages) 是 [[Python]] 的标准[[Python 包管理器]]，用于从 [[PyPI]] 安装和管理 Python 包。

## 基本概念

pip 是 Python 生态系统的核心工具，与 [[虚拟环境]] 配合使用可以有效管理项目依赖。

## 包安装

### 基本安装
```bash
# 安装最新版本
pip install package_name

# 安装指定版本
pip install package_name==1.2.3

# 版本范围
pip install "package_name>=1.0,<2.0"
pip install "package_name~=1.2.0"  # 兼容版本
```

### 安装源
```bash
# 从 Git 仓库
pip install git+https://github.com/user/repo.git

# 从本地路径
pip install ./local_package

# 从压缩包
pip install package.tar.gz
```

### 安装选项
```bash
# 用户级安装
pip install --user package_name

# 强制重新安装
pip install --force-reinstall package_name

# 不安装依赖
pip install --no-deps package_name
```

## 包管理

### 查看包信息
```bash
# 列出所有包
pip list

# 列出过时包
pip list --outdated

# 显示包详细信息
pip show package_name
```

### 包更新和卸载
```bash
# 升级包
pip install --upgrade package_name

# 卸载包
pip uninstall package_name

# 批量卸载
pip uninstall -r requirements.txt
```

## 依赖管理

### requirements.txt
```bash
# 生成依赖文件
pip freeze > requirements.txt

# 安装依赖
pip install -r requirements.txt

# 升级依赖
pip install -r requirements.txt --upgrade
```

### 文件格式
```text
# 精确版本
Django==4.2.0

# 版本范围
requests>=2.25.0,<3.0.0

# 兼容版本
numpy~=1.21.0
```

## 配置

### 配置文件位置
- **Windows**: `%APPDATA%\pip\pip.ini`
- **Linux/macOS**: `~/.pip/pip.conf`

### 配置示例
```ini
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
trusted-host = pypi.tuna.tsinghua.edu.cn
timeout = 60
```

### 镜像源
```bash
# 临时使用镜像源
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple package_name
```

## 与其他工具的关系

- 与 [[conda]] 的区别和配合使用
- 与 [[虚拟环境]] 的集成
- pipenv 和 poetry 等现代工具的基础

## 相关概念

- [[Python 包管理器]]
- [[PyPI]]
- [[虚拟环境]]
- [[依赖管理]]

#python #包管理 #pip #工具
