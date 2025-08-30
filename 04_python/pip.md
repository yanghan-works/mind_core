---
tags:
  - python
  - pip
  - 工具
alias: pip,python包管理工具
date: 2025-08-30 07:53
---
# pip 核心用法

**核心结论：** `pip` 是 Python 的「应用商店」和「项目管家」，负责管理你代码世界里所有的“零件”（库）。

## 核心命令

这四个命令覆盖了 90% 的日常使用场景。

### 1. 安装 (install)

获取新的库。

```
# 示例：安装 pandas 数据分析库
pip install pandas
```

### 2. 查看 (list)

盘点当前环境中已安装的所有库。

```
pip list
```

### 3. 卸载 (uninstall)

移除不再需要的库。

```
# 示例：卸载一个没用的库
pip uninstall useless_package
```

### 4. 升级 (upgrade)

将一个已安装的库更新到最新版本。

```
# 示例：升级 pandas 库
pip install --upgrade pandas
```

## 项目依赖管理 (专业用法)

这是区分业余和专业的**唯一标准**。团队协作、项目部署和环境迁移全靠它。

- **生成依赖清单**: 将当前环境的所有库及其精确版本号，导出到一个名为 `requirements.txt` 的文件中。这个文件就是你项目的“标准配置单”。
    
    ```
    pip freeze > requirements.txt
    ```
    
- **根据清单安装**: 在新环境或与他人协作时，使用此命令可一键安装项目所需的所有依赖。
    
    ```
    pip install -r requirements.txt
    ```
    

## 更换国内镜像源 (永久加速)

**核心结论：** 默认源在国外，是龟速。换成国内镜像，体验火箭般的速度。这是**一次性**配置，一劳逸。

### 1. 选一个高速入口 (镜像地址)

- **清华大学:** `https://pypi.tuna.tsinghua.edu.cn/simple`
    
- **阿里云:** `https://mirrors.aliyun.com/pypi/simple/`
    
- **豆瓣 (http):** `http://pypi.douban.com/simple/` (注意：需要额外配置)
    

### 2. 修改配置文件（永久生效）

#### Windows 系统

1. 地址栏输入 `%APPDATA%` 回车，新建 `pip` 文件夹。
    
2. 在 `pip` 文件夹里，新建 `pip.ini` 文件并粘贴以下内容：
    
```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
```
    

#### macOS / Linux 系统

1. 在你的用户主目录 (`~`) 下，创建 `.pip` 文件夹 (`mkdir ~/.pip`)。
    
2. 在 `~/.pip/` 目录下，创建 `pip.conf` 文件并粘贴以下内容：
    
```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
```
    

### 3. 关键补充：处理HTTP源和验证配置

#### A. 信任不安全的 `http` 源

如果使用 `http` 源 (如豆瓣)，必须额外添加 `trusted-host`。

```
[global]
index-url = http://pypi.douban.com/simple/
trusted-host = pypi.douban.com
```

#### B. 验证配置是否生效

改完后，用此命令检查，确保没写错。

```
pip config list
```