---
layout:     post
title:      Mac 删除原生 ABC 英文输入法
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

禁用第三方输入法切换英文，例如搜狗输入法只输出中文（设置按键 → 状态切换 → 中英文 → 禁用快捷键），英文用系统自带 `ABC`。

## 方案二

删除系统英文 `ABC`，只保留一个输入法，这样搜狗输入法只需按 Shift 即可切换中英文。

1、打开系统偏好设置 → 键盘 → 输入法 → 添加 `US 美国`（Big Sur 及之前版本是 `🇺🇸 美国`），再删除 `ABC` 英文。

![](https://i.imgur.com/qhpNu0q.png)

2、前往 `~/Library/Preferences/` 文件夹，找到 `com.apple.HIToolbox.plist` 文件并用 [Xcode](https://apps.apple.com/cn/app/xcode/id497799835?mt=12) 软件打开。
3、删除所有 `KeyboardLayout Name String U.S.` 并保存。

![](https://i.imgur.com/q9xTLLL.png)

4、重启 Mac。

![I](https://i.imgur.com/zoyqOsr.png)
## 还原

不必担心此操作给电脑带来异常，一切正常。还原打开系统偏好设置 → 键盘 → 输入法 → 添加 `US 美国` 或 `ABC` 即可。