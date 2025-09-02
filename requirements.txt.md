# requirements.txt

[[pip]] 的依赖文件，用于记录和管理项目的 [[Python 包]] 依赖。

## 基本操作

```bash
# 生成依赖文件
pip freeze > requirements.txt

# 安装依赖文件中的包
pip install -r requirements.txt

# 升级依赖文件中的包
pip install -r requirements.txt --upgrade
```

## 文件格式

```text
# 精确版本
Django==4.2.0

# 版本范围
requests>=2.25.0,<3.0.0

# 兼容版本
numpy~=1.21.0

# 最小版本
matplotlib>=3.0

# Git 仓库
git+https://github.com/user/repo.git@v1.0

# 本地包
-e ./local_package

# 注释
# 这是一个注释行
```

## 最佳实践

### 文件组织
- `requirements.txt` - 生产依赖
- `requirements-dev.txt` - 开发依赖
- `requirements-test.txt` - 测试依赖

### 版本固定策略
- 生产环境：固定精确版本
- 开发环境：允许兼容版本更新

## 相关概念

- [[pip install]]
- [[pip freeze]]
- [[依赖管理]]
- [[虚拟环境]]
- [[包版本控制]]

#pip #依赖管理 #配置文件
