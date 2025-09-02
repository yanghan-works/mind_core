# conda 配置

[[conda]] 的配置文件和设置选项。

## 配置文件

主配置文件：`.condarc`

```yaml
channels:
  - conda-forge
  - defaults

channel_priority: strict

create_default_packages:
  - pip
  - ipykernel

auto_activate_base: false
show_channel_urls: true
ssl_verify: true
```

## 常用配置命令

```bash
# 查看配置
conda config --show

# 设置配置
conda config --set auto_activate_base false

# 添加 channel
conda config --add channels conda-forge

# 添加默认包
conda config --add create_default_packages pip
```

## 镜像源配置

```bash
# 清华镜像
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
```

## 相关概念

- [[conda]]
- [[conda channels]]
- [[PyPI 镜像源]]

#conda #配置 #设置
