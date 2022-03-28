---
layout: post
title: Quantumult X 分流配置设置详解
subtitle: iOS 端代理工具
date: 2022-3-28
author: 河東
header-img: img/post-bg-net.jpeg
catalog: true
top: false
tags:
  - Quantumult X
---

Quantumult X 是一款不错的 iOS 端应用，但对于初接触者而言有点难上手，今天为大家介绍如何添加配置。

# 一、订阅节点

1. 打开 Quantumult X 点击右下角**红黄蓝按钮**。
2. 节点可以通过 `添加`、`订阅`、`URL`、`扫码` 四种方式连接代理。

# 二、下载配置

1. Quantumult X 设置 - 配置文件 - 下载。
2. 输入配置链接，点击右上角保存。


参考配置：

`https://raw.githubusercontent.com/erdongchanyo/Rules/main/Quantumult%20X/LazyConf/QuantumultX_EDC-Lazy.conf`


# 三、订阅节点

重复操作步骤一

> 注：如不显示分流配置，长按右下角红黄蓝按钮，左侧出现白色刷新按钮。

# 四、开启重写

Quantumult X 设置 - 打开重写。

# 五、开启 MitM

1. Quantumult X 设置 - 开启 MitM - 生成证书 - 配置证书。
2. 跳转到浏览器下载配置证书。
3. 打开 iPhone 设置安装证书。
4. 安装好在点击通用 - VPN与设备管理打开刚刚安装的 Quantumult X 配置证书。

完成配置安装，打开 Quantumult X 愉快的享用。
