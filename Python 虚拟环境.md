# Python 虚拟环境

## 核心概念

**虚拟环境** 为 [[Python]] 项目创建隔离的运行空间，避免包依赖冲突。

## 创建与激活

### venv (内置)
```bash
# 创建
python -m venv myenv

# 激活
myenv\Scripts\activate     # Windows
source myenv/bin/activate  # Linux/Mac

# 退出
deactivate
```

### virtualenv
```bash
pip install virtualenv
virtualenv myenv
```

## 包管理集成

### 与 pip 配合
- 环境内使用 [[Python pip]]
- 独立的包安装空间
- 生成专属 `requirements.txt`

### 依赖导出
```bash
pip freeze > requirements.txt
pip install -r requirements.txt
```

## 工作流程

### 项目初始化
1. 创建虚拟环境
2. 激活环境
3. 安装依赖
4. 开发代码

### 部署准备
1. 导出依赖列表
2. 测试环境一致性
3. 打包分发

## 最佳实践

### 命名规范
- `venv` - 通用名称
- `env` - 简短别名
- `.venv` - 隐藏目录

### 目录结构
```
project/
├── .venv/          # 虚拟环境
├── src/            # 源代码
├── requirements.txt
└── README.md
```

## 相关链接

- [[Python]]
- [[Python pip]]
- [[Python 包管理]]

---
*创建时间: 2025-09-02*  
*标签: #python #虚拟环境 #隔离*
