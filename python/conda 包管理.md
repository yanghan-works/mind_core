# conda 包管理

[[conda]] 的包安装、更新和卸载功能。

## 安装包

```bash
# 基本安装
conda install package_name

# 指定版本
conda install package_name=1.2.3

# 多个包
conda install numpy pandas matplotlib

# 指定 channel
conda install -c conda-forge package_name

# 安装到指定环境
conda install --name myenv package_name
```

## 查询包信息

```bash
# 搜索包
conda search package_name

# 列出已安装包
conda list

# 显示包信息
conda info package_name
```

## 更新和卸载

```bash
# 更新包
conda update package_name

# 更新所有包
conda update --all

# 卸载包
conda remove package_name
```

## 相关概念

- [[conda]]
- [[conda channels]]
- [[Python 包]]
- [[包版本控制]]

#conda #包管理 #命令
