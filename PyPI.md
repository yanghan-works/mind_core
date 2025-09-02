# PyPI

## 核心概念

**PyPI** (Python Package Index) 是 [[Python]] 官方包仓库，托管开源 Python 包。

## 基本信息

### 访问方式
- **网站**: pypi.org
- **命令行**: [[Python pip]]
- **API**: JSON API 接口

### 包结构
```
package/
├── setup.py        # 包配置
├── README.md       # 说明文档
├── LICENSE         # 许可证
└── src/           # 源代码
```

## 包发布

### 准备工作
```bash
pip install twine build
```

### 构建包
```bash
python -m build
```

### 上传包
```bash
twine upload dist/*
```

## 包搜索

### 命令行搜索
```bash
pip search package_name  # 已废弃
```

### 网站搜索
- 分类浏览
- 关键词搜索
- 热门排行

## 镜像源

### 国内镜像
```bash
# 清华源
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple/

# 阿里源  
pip install -i https://mirrors.aliyun.com/pypi/simple/
```

### 配置永久镜像
```ini
# ~/.pip/pip.conf
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple/
```

## 相关链接

- [[Python]]
- [[Python pip]]
- [[Python 包管理]]

---
*创建时间: 2025-09-02*  
*标签: #python #pypi #仓库*
