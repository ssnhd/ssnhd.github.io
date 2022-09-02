---
layout:     post
title:      搜狗词库转换方法（支持多家输入法）
subtitle:   强大的词库转换功能
date:       2022-1-6
author:     河東
header-img: img/post-bg-rime.png
catalog: true
top: false
tags:
    - 输入法
---

如果您使用 Rime 输入法，需要添加第三方词库（如搜狗百度），但需要将词库格式转换才能使用。本文以搜狗词库为例，教您如何转换。



## 下载词库

打开 [搜狗官网](https://pinyin.sogou.com/dict/cate/index/167?rf=dictindex&pos=dict_rcmd) 下载词库，格式为 `.scel` 文件。

![](/img/sogoudict/02.png)



## 安装转换工具



下载深蓝词库转换工具 [imewlconverter_Windows.zip](https://github.com/studyzy/imewlconverter/releases) 并打开。

![](/img/sogoudict/03.png)



## 开始转换

点击 `…` 选择下载好的词库（可多选），再点击**打开**。

> 注意：如果不显示词库，将右下角改为`所有格式`。

![](/img/sogoudict/04.png)

转出项选择【Rime中州韵】。

![](/img/sogoudict/08.png)

编码类型选择 **拼音** 和 **MacOS**，点击**确定**。

![](/img/sogoudict/05.png)

点击**转换**。

![](/img/sogoudict/06.png)

点击【是】保存到本地。

![](/img/sogoudict/07.png)

保存后为 `.txt` 文件。

![](/img/sogoudict/09.png)



## 改为 yaml 文件

将下面代码粘贴在文本最上方（`...` 下面空一行），修改词库名（以 sogou 为例）并保存。

```
# 可以将包含哪些词库写在此处，方便日后查看是否有重复。

---
name: luna_pinyin.sogou    # 词库名自定义
version: "0.9"               
sort: by_weight              
use_preset_vocabulary: false
...

```

![](/img/sogoudict/10.png)

将文件重命名。

![](/img/sogoudict/11.png)

以 `.dict.yaml` 为后缀，命名为 `luna_pinyin.sogou.dict.yaml` 完成词库转换。



> 注：文件名前部分要和文件内 `name` 一致。

![](/img/sogoudict/12.png)
