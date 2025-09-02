# Python 包管理

## 核心概念

**包管理** 是 [[Python]] 生态系统的基础设施，负责软件包的分发、安装和依赖解析。

## 管理工具

### pip
- [[Python pip]] - 标准包管理器
- 从 [[PyPI]] 安装包
- 依赖自动解析

### 其他工具
```bash
conda     # Anaconda 包管理器
poetry    # 现代依赖管理
pipenv    # 虚拟环境 + 包管理
```

## 依赖管理

### requirements.txt
```text
# 生产依赖
requests>=2.25.0
numpy==1.21.0

# 开发依赖  
pytest>=6.0.0
black>=21.0.0
```

### setup.py
```python
from setuptools import setup

setup(
    name="my-package",
    install_requires=[
        "requests>=2.25.0",
        "numpy>=1.20.0"
    ]
)
```

## 最佳实践

### 版本固定
- **精确版本** (`==1.2.3`) - 生产环境
- **兼容版本** (`~=1.2.0`) - 开发环境
- **最小版本** (`>=1.2.0`) - 库开发

### 环境隔离
- 使用 [[Python 虚拟环境]]
- 避免全局包冲突
- 项目独立依赖

## 相关链接

- [[Python pip]]
- [[Python 虚拟环境]]
- [[PyPI]]
- [[Python]]

---
*创建时间: 2025-09-02*  
*标签: #python #包管理 #依赖*
