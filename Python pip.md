# Python pip

## 概念
Python 包管理工具，用于安装、升级和管理 Python 包。

## 核心命令

### 安装
```bash
pip install package_name
pip install package_name==1.2.3
pip install -r requirements.txt
```

### 查看
```bash
pip list
pip show package_name
pip freeze
```

### 升级
```bash
pip install --upgrade package_name
pip install --upgrade pip
```

### 卸载
```bash
pip uninstall package_name
```

## 配置文件

### requirements.txt
```
package_name==1.2.3
another_package>=2.0.0
```

### pip.conf / pip.ini
```ini
[global]
index-url = https://pypi.org/simple/
trusted-host = pypi.org
```

## 最佳实践

- **虚拟环境**：始终在虚拟环境中使用
- **版本锁定**：生产环境使用精确版本号
- **镜像源**：使用国内镜像提升下载速度
- **依赖管理**：定期更新 requirements.txt

## 常见问题

### 权限错误
```bash
pip install --user package_name
```

### 网络问题
```bash
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple/ package_name
```

---
*原子笔记 | 2025-09-02*
