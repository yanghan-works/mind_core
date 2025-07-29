---
tags:
  - Linux
aliases: 
created: 2025-07-27 14:47
---
## 1. 基本概念与核心用法

1. ***读取** : 一行文本送到工作台 (模式空间)。
	
2. **执行**: 送过来的文本，根据指令清单进行操作。
	
3. **显示**: 操作完成后，工作台的一行内容打印。
	
4. **循环**: 
	1. 清空工作台
	2. 等待下一行文本送来
	3. 重复前三步骤

### 1.1 模式空间

sed命令的临时缓冲区，处理每行文本的工作台，所有的编辑操作都发生在这个临时空间里。

## 1.2 基本命令结构

sed的基本命令格式如下：

```shell
sed [选项] '命令' 文件名
```

- **`[选项]`** 比如 `-n` (安静模式，稍后会讲)
    
- **`'命令'`** 这是你希望 `sed` 执行的具体操作，通常由 **地址** 和 **操作** 两部分组成，需要用单引号 `''` 包裹起来
    
- **`文件名`** `sed` 要处理的源文件。如果省略，`sed` 会处理从管道（`|`）传来的数据


## 2. 替换 (s)

``` shell
echo "hello world" | sed 's/world/Linux/'

## 匹配到world删除整行
$ echo "hello world" | sed '/world/d'
# (没有任何输出)

## 删除world，替换为空
echo "hello world" | sed 's/world//'

```

**命令解释**

- `echo "hello world"` 生成一行文本
    
- `|` 管道，把左边命令的输出，作为右边命令的输入
    
- `sed 's/world/Linux/'`
    
    - `s` 是 `substitute` (替换) 命令的缩写，这是 `sed` 最常用的命令
        
    - `/world/` 是我们要查找的内容
        
    - `/Linux/` 是我们要替换成的内容
        
    - `/` 是分隔符

### 2.1 替换标志 (Flags)

`s` 命令的完整形态是 `s/查找/替换/标志`。标志可以改变替换的行为。

- `g` 全局替换 `echo "hello world, beautiful world" | sed 's/world/Linux/g'`

- `i` 忽略大小写 (ignore case) `echo "Hello WORLD" | sed 's/world/Linux/i'`

- `gi` 连用 `echo "I love cat, my CAT is cute." | sed 's/cat/dog/ig'`


- 内容包含 `/` 和其他特殊字符匹配（url,|，sed 命令自身的特殊字符，正则表达式元字符）

	- 转义字符 (不推荐)`sed 's/version=1\|beta/version=2\|release/'`
		
    - 更换分隔符 (推荐) `sed 's#version=1|beta#version=2|release#'`

- 所有数字加上括号 `echo "file1 saved, file2 saved" | sed 's/[0-9]/(&)/g'`

## 地址

