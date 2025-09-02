# conda channels

[[conda]] 的包源管理系统，类似于 [[PyPI 镜像源]]。

## 主要 channels

- **defaults** - Anaconda 官方仓库
- **[[conda-forge]]** - 社区维护的高质量包
- **pytorch** - PyTorch 官方 channel
- **nvidia** - NVIDIA 相关包

## 管理命令

```bash
# 查看 channels
conda config --show channels

# 添加 channel
conda config --add channels conda-forge

# 移除 channel
conda config --remove channels conda-forge

# 临时使用 channel
conda install -c conda-forge package_name
```

## 优先级设置

```bash
# 设置严格优先级
conda config --set channel_priority strict

# 设置灵活优先级
conda config --set channel_priority flexible
```

## 国内镜像

```bash
# 清华镜像
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
```

## 相关概念

- [[conda]]
- [[conda 包管理]]
- [[conda 配置]]

#conda #channels #包源
