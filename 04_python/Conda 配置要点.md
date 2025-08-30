---
tags: 
alias: 
date: 2025-08-30 13:49
---
**核心**: 管理 `conda` 的行为和下载软件包的渠道 (Channels)。

### 查看配置

```
# 查看关键信息 (推荐)
conda info

# 查看所有配置项的来源
conda config --show-sources
```

### 修改下载渠道 (Channels)

**问题**: 默认渠道慢，或国内镜像（如清华）不稳定导致安装卡死。 **推荐配置**: 使用社区维护的 `conda-forge` 渠道，并设为高优先级。

```
# 1. 添加 conda-forge 渠道
conda config --add channels conda-forge

# 2. 设置渠道优先级为严格，优先使用 conda-forge
conda config --set channel_priority strict
```

**重置渠道**: 如果渠道配置搞乱了，用此命令恢复默认设置。

```
conda config --remove-key channels
```

### 优化体验

```
# 1. 禁止打开终端时自动激活 base 环境，避免误操作
conda config --set auto_activate_base false

# 2. 让 `conda list` 显示每个包的来源渠道，方便排查
conda config --set show_channel_urls true
```