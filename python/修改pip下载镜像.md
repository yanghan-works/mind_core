宝宝，修改 `pip` 镜像，这就像是给你的快递公司换个新的集散中心。

---

### 核心类比：更换快递集散中心

当你用 `pip` 安装库时，默认是去 `PyPI`（Python Package Index）这个官方“集散中心”下载包裹。这个中心在国外，有时候会因为网络问题，下载速度特别慢，甚至失败。

而国内有很多像清华、豆瓣、阿里这样的机构，都自建了 `PyPI` 的“镜像站”。这些镜像站就像是**国内的快递集散中心**，它们定期把国外的包裹同步过来，让你可以从一个更近、更快的站点取件。

修改 `pip` 镜像，就是把你的“默认快递地址”从国外的集散中心，改成离你更近的国内镜像站，从而大幅提升下载速度。

---

### 怎么修改？

修改 `pip` 镜像有两种常见方法：临时修改和永久修改。

### 1. 临时修改 (只对当前命令有效)

如果你只是偶尔需要快一点，可以在安装命令后面加上 `-i` 参数，指定一个镜像地址。

**语法：**

Bash

```python
pip install package_name -i https://pypi.tuna.tsinghua.edu.cn/simple
```

- `package_name`：你想安装的库的名字，比如 `numpy`。
    
- `-i`：`index-url` 的缩写，用来指定镜像地址。
    
- `https://pypi.tuna.tsinghua.edu.cn/simple`：这是清华大学的镜像地址。你也可以换成其他的，比如：
    
    - **阿里云**：`https://mirrors.aliyun.com/pypi/simple/`
        
    - **豆瓣**：`https://pypi.doubanio.com/simple/`
        

### 2. 永久修改 (一劳永逸)

如果你想以后每次都使用国内镜像，可以永久修改 `pip` 的配置文件。

**Windows 系统：**

1. 在你的用户目录下（比如 `C:\Users\你的用户名`）创建一个名为 **`.pip`** 的文件夹。
    
2. 进入 `.pip` 文件夹，创建一个名为 **`pip.ini`** 的文件。
    
3. 用记事本或其他文本编辑器打开 `pip.ini`，然后添加以下内容：

```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host = pypi.tuna.tsinghua.edu.cn
```

- `index-url`：指定你想要使用的镜像地址。
    
- `trusted-host`：因为镜像站不是官方的，为了防止 `pip` 报错，需要把它添加到信任列表中。
    

**macOS / Linux 系统：**

1. 在你的用户目录下（`~`）创建一个名为 **`.pip`** 的文件夹。
    
2. 进入 `.pip` 文件夹，创建一个名为 **`pip.conf`** 的文件。
    
3. 用文本编辑器打开 `pip.conf`，然后添加和 Windows 相同的配置内容。
    

Ini, TOML

```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host = pypi.tuna.tsinghua.edu.cn
```

完成这些步骤后，你以后再使用 `pip` 安装任何库，都会自动从你指定的镜像站下载，速度会快很多。

---

### 尖锐比喻

如果你不修改镜像，继续用默认的 `PyPI`，那么你的下载速度就像是**在用 56K 猫拨号上网**，别人几秒钟搞定的事，你可能要等上几分钟甚至更久，还容易下载失败。这完全是在折磨自己。

永久修改一次，一劳永逸，这是每个 Python 开发者都应该做的基础配置。