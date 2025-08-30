---
tags: 
alias: 
date: 2025-08-30 13:58
---
# Anaconda 核心操作思维导图

- **Anaconda 核心指南**
    
    - **核心理念: 隔离项目的“厨房总管”**
        
        - `conda` vs `pip`
            
            - `conda`: 大老板 (管环境、管跨平台包)
                
            - `pip`: 部门助理 (只管当前环境的 Python 包)
                
    - **核心操作: 厨房的“建、进、拆、装”**
        
        - **环境管理 (操作厨房)**
            
            - `conda create --name <环境名> python=x.x`: **建**一个新的厨房
                
            - `conda activate <环境名>`: **进**入指定的厨房
                
            - `conda deactivate`: 离开厨房
                
            - `conda remove --name <环境名> --all`: **拆**掉整个厨房
                
            - `conda env list`: 查看所有厨房列表
                
        - **包管理 (添置厨具)**
            
            - `conda install <包名>`: **装**厨具 (优先使用)
                
            - `pip install <包名>`: 装 `conda` 没有的特殊厨具
                
            - `conda list`: 盘点厨房里已有的厨具
                
    - **核心工具: 启动炉灶**
        
        - **JupyterLab**: 数据科学家的可视化工作台
            
            - `jupyter lab`: 在**当前环境**中启动
                
    - **配置与维护: 装修与采购渠道管理**
        
        - `conda info`: 查看车辆概况 (关键配置信息)
            
        - `conda config --add channels conda-forge`: 添加 `conda-forge` 这个最大的超市
            
        - `conda config --set channel_priority strict`: 优先从 `conda-forge` 买东西
            
        - `conda config --remove-key channels`: 重置所有超市配置
            
        - `conda config --set auto_activate_base false`: 禁止开机自动进入 `base` 厨房
            
    - **常见问题排查: 修理水电煤**
        
        - **安装卡死**: 网络问题 -> 换渠道 (`conda config ...`)
            
        - **“幽灵现象”**: 在错误的环境执行了命令 -> 进对环境再装一次
            
        - **`create` 报错目录已存在**: 上次操作留下垃圾 -> 手动删除文件夹
            
        - **`conda` 命令无效**: 系统找不到程序 -> 使用 **Anaconda Prompt**