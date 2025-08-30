---
tags:
  - python
  - pip
alias: pip换源
date: 2025-08-30 11:39
---
**核心结论：** 默认源在国外，是龟速。换成国内镜像，体验火箭般的速度。这是**一次性**配置，一劳永逸。

## 1. 选一个高速入口 (镜像地址)

随便挑一个，都比官方快一百倍。推荐清华或阿里。

- **清华大学:** `https://pypi.tuna.tsinghua.edu.cn/simple`
    
- **阿里云:** `https://mirrors.aliyun.com/pypi/simple/`
    
- **中国科技大学:** `https://pypi.mirrors.ustc.edu.cn/simple/`
    
- **豆瓣:** `http://pypi.douban.com/simple/`
    

## 2. 修改配置文件（永久生效）

别每次都手动加 `-i`，那是蠢办法。

### Windows 系统

1. 地址栏输入 `%APPDATA%` 回车，新建 `pip` 文件夹。
    
2. 在 `pip` 文件夹里，新建 `pip.ini` 文件。
    
3. 粘贴以下内容进去：
    
```
[global]
index-url = [https://pypi.tuna.tsinghua.edu.cn/simple](https://pypi.tuna.tsinghua.edu.cn/simple)
```
    

### macOS / Linux 系统

1. 在你的用户主目录 (`~`) 下，创建 `.pip` 文件夹 (`mkdir ~/.pip`)。
    
2. 在 `~/.pip/` 目录下，创建 `pip.conf` 文件。
    
3. 粘贴以下内容进去：
    
 ```
[global]
index-url = [https://pypi.tuna.tsinghua.edu.cn/simple](https://pypi.tuna.tsinghua.edu.cn/simple)
```

## 3. 处理HTTP源和验证配置

### A. 处理不安全的 `http` 源

如果你用了像豆瓣这样的 `http` 源，必须额外添加 `trusted-host` 来获得 `pip` 的信任。

**示例 (豆瓣源):**

```
[global]
index-url = [http://pypi.douban.com/simple/](http://pypi.douban.com/simple/)
trusted-host = pypi.douban.com
```

### B. 验证配置是否生效

改完后，用这个命令检查一下，确保没写错。它会把你当前的配置打印出来。

```
pip config list
```