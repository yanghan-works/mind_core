# PyPI 镜像源

[[PyPI]] 的国内镜像服务器，用于加速 [[Python 包]] 下载。

## 主要镜像源

| 名称 | URL | 特点 |
|------|-----|------|
| [[清华 PyPI 镜像]] | https://pypi.tuna.tsinghua.edu.cn/simple | 速度快，稳定 |
| [[阿里 PyPI 镜像]] | https://mirrors.aliyun.com/pypi/simple | 商业支持 |
| [[中科大 PyPI 镜像]] | https://pypi.mirrors.ustc.edu.cn/simple | 教育网优化 |
| [[豆瓣 PyPI 镜像]] | https://pypi.douban.com/simple | 老牌镜像 |

## 使用方法

### 临时使用
```bash
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple package_name
```

### 永久配置
通过 [[pip 配置]] 文件设置默认镜像源。

## 相关概念

- [[pip]]
- [[pip 配置]]
- [[网络优化]]

#pip #镜像源 #网络优化
