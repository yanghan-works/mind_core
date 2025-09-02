# conda 环境管理

[[conda]] 的环境管理功能，用于创建和管理隔离的 Python 环境。

## 创建环境

```bash
# 基本创建
conda create --name myenv

# 指定 Python 版本
conda create --name myenv python=3.9

# 创建时安装包
conda create --name myenv python=3.9 numpy pandas

# 从文件创建
conda env create -f environment.yml
```

## 环境操作

```bash
# 激活环境
conda activate myenv

# 退出环境
conda deactivate

# 列出环境
conda env list

# 删除环境
conda env remove --name myenv --all

# 克隆环境
conda create --name newenv --clone myenv
```

## 环境导出导入

```bash
# 导出环境 (跨平台)
conda env export --name myenv > environment.yml

# 导出当前平台
conda list --explicit > spec-file.txt

# 导入环境
conda env create -f environment.yml
```

## 相关概念

- [[conda]]
- [[environment.yml]]
- [[虚拟环境]]
- [[项目隔离]]

#conda #环境管理 #隔离
