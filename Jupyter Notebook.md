# Jupyter Notebook

交互式计算环境，是 [[Anaconda]] 的核心组件之一。

## 基本概念

Jupyter Notebook 提供基于网页的交互式开发环境，支持代码、文档和可视化的混合编写。

## 启动方式

```bash
# 启动 Jupyter Notebook
jupyter notebook

# 启动 JupyterLab
jupyter lab

# 指定端口
jupyter notebook --port 8888

# 指定工作目录
jupyter notebook --notebook-dir=/path/to/notebooks
```

## 内核管理

```bash
# 安装 ipykernel
conda install ipykernel

# 添加环境到 Jupyter
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"

# 列出内核
jupyter kernelspec list

# 删除内核
jupyter kernelspec remove myenv
```

## 与环境集成

- 配合 [[conda 环境管理]] 使用
- 支持多个 [[虚拟环境]] 切换
- 与 [[数据科学包]] 深度集成

## 相关概念

- [[Anaconda]]
- [[conda]]
- [[数据科学工作流]]

#jupyter #notebook #交互式开发
