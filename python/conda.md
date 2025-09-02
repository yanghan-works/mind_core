# conda

[[Anaconda]] 的包和环境管理器，比 [[pip]] 更强大的依赖解析能力。

## 核心功能

- [[conda 环境管理]] - 创建和管理隔离环境
- [[conda 包管理]] - 安装和管理包
- [[conda channels]] - 包源管理
- [[conda 配置]] - 系统配置

## 与 pip 的区别

| 功能 | conda | [[pip]] |
|------|-------|---------|
| 包管理 | ✓ | ✓ |
| 环境管理 | ✓ | 需要 [[虚拟环境]] |
| 依赖解析 | 强 | 弱 |
| 二进制包 | ✓ | 部分 |
| 非 Python 包 | ✓ | ✗ |

## 混合使用

```bash
# 优先使用 conda
conda install package_name

# conda 没有时使用 pip
pip install package_name
```

## 相关概念

- [[Python 包管理器]]
- [[environment.yml]]
- [[conda-forge]]

#conda #包管理 #环境管理
