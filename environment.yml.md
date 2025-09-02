# environment.yml

[[conda]] 的环境配置文件，用于定义和共享 [[conda 环境管理|conda 环境]]。

## 基本格式

```yaml
name: myproject
channels:
  - conda-forge
  - defaults
dependencies:
  - python=3.9
  - numpy>=1.20
  - pandas
  - pip
  - pip:
    - some-pip-only-package
```

## 高级配置

```yaml
name: data-science-env
channels:
  - conda-forge
  - pytorch
dependencies:
  - python=3.9
  - numpy=1.21.*
  - scikit-learn
  - jupyter
  - pip:
    - streamlit
variables:
  CUDA_VISIBLE_DEVICES: "0"
```

## 使用方法

```bash
# 从文件创建环境
conda env create -f environment.yml

# 导出当前环境
conda env export > environment.yml

# 跨平台导出
conda env export --from-history > environment.yml
```

## 相关概念

- [[conda]]
- [[conda 环境管理]]
- [[conda channels]]
- [[requirements.txt]]

#conda #配置文件 #环境管理
