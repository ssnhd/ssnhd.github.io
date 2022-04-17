---
layout:     post
title:      Mac 删除原生 ABC 英文输入
subtitle:   摆脱切换输入法频繁出错的困扰
date:       2022-1-1
author:     河東
header-img: img/post-bg-mac.jpeg
catalog: true
top: false
tags:
    - 输入法
    - Mac
    - macOS
---


使用第三方输入法时，常遇到想输入中文却输出英文，反之亦然，多次切换很麻烦，下面介绍两种方案来解决此问题。

## 方案一

禁用第三方输入法切换英文，例如搜狗只输出中文（设置按键 - 状态切换 - 中英文 - 禁用快捷键），英文用系统自带。

## 方案二

删除系统英文，只保留一个输入法。

1. 打开系统偏好设置 - 键盘 - 输入法 - 添加美国🇺🇸英文，再删除 ABC 英文。
2. 前往 `~/Library/Preferences/` 文件夹，找到 `com.apple.HIToolbox.plist` 文件并用 [Xcode](https://apps.apple.com/cn/app/xcode/id497799835?mt=12) 软件打开。
3. 删除所有包含 `KeyboardLayout Name String U.S.`的文件并保存。

![](https://i.imgur.com/RWMziKi.png)

重启电脑。

![I](https://i.imgur.com/JvzQHNH.png)
## 还原

打开系统偏好设置 - 键盘 - 输入法 - 添加美国🇺🇸英文或 ABC 英文即可。