---
tags:
  - python
  - pip
  - 工具
alias: pip,python包管理工具
date: 2025-08-30 07:53
---
**核心结论：** `pip` 是 Python 的「应用商店」和「管家」。别想多了，就这点事。

## 四个基本动作

记住这四个，你就掌握了 `pip` 90% 的日常操作。

1. **安装 (install):** 获取新工具。
    
    ```
    # 示例：安装 pandas 库
    pip install pandas
    ```
    
2. **查看 (list):** 盘点你有什么。
    
    ```
    pip list
    ```
    
3. **卸载 (uninstall):** 扔掉垃圾。
    
    ```
    # 示例：卸载没用的库
    pip uninstall useless_package
    ```
    
4. **升级 (upgrade):** 给工具更新换代
    
    ```
    # 示例：升级指定的库
    pip install --upgrade pandas
    ```
    

## 唯一的专业用法：项目管理

这是区分菜鸟和专业人士的**唯一标准**。团队协作、项目迁移全靠它。

- **生成“装备清单”**: 把当前环境的所有库和版本号打包成一个文件。
    
    ```
    pip freeze > requirements.txt
    ```
    
- **按“装备清单”一键安装**: 拿到别人的项目后，用这个命令安装所有依赖。
    
    ```
    pip install -r requirements.txt
    ```
    

## 关联笔记

- 下载慢得像乌龟？看这个解决 -> [[pip 更换国内镜像源]]