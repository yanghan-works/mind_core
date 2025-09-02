# Python pip

## 核心概念

**pip** 是 [[Python]] 的标准包管理器，用于安装和管理 Python 包。

## 基本操作

### 安装包
```bash
pip install package_name
pip install package_name==1.2.3  # 指定版本
pip install -r requirements.txt   # 批量安装
```

### 查看包信息
```bash
pip list                 # 列出已安装包
pip show package_name    # 显示包详情
pip freeze              # 输出依赖列表
```

### 升级与卸载
```bash
pip install --upgrade package_name
pip uninstall package_name
```

## 高级用法

### 虚拟环境配合
- 与 [[Python 虚拟环境]] 结合使用
- 避免全局包污染

### 镜像源配置
```bash
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple/ package_name
```

### requirements.txt
```text
requests>=2.25.0
numpy==1.21.0
pandas~=1.3.0
```

## 常见问题

### 权限问题
```bash
pip install --user package_name  # 用户级安装
```

### 缓存清理
```bash
pip cache purge
```

## 相关链接

- [[Python 包管理]]
- [[Python 虚拟环境]]
- [[PyPI]]

---
*创建时间: 2025-09-02*  
*标签: #python #包管理 #工具*
