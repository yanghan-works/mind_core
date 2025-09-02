# conda-forge

社区维护的 [[conda channels|conda channel]]，提供高质量的开源包。

## 特点

- **社区驱动** - 由开源社区维护
- **包质量高** - 严格的构建和测试流程
- **更新及时** - 通常比官方 channel 更快
- **包数量多** - 包含大量第三方包

## 使用方法

```bash
# 添加 conda-forge
conda config --add channels conda-forge

# 临时使用
conda install -c conda-forge package_name

# 设置优先级
conda config --set channel_priority strict
```

## 与其他 channels 的关系

- 优先级高于 **defaults**
- 与 [[PyPI]] 互补
- 支持 [[conda 包管理]]

## 相关概念

- [[conda channels]]
- [[conda]]
- [[开源社区]]

#conda-forge #社区 #开源
