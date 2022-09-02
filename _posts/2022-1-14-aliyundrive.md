---
layout: post
title: 阿里云盘配合 Infuse 观影
subtitle: 
date: 2022-1-14
author: 河東
header-img: img/post-bg-film.jpg
catalog: true
top: false
tags:
  - Infuse
  - 阿里云盘
---

阿里云盘不限速且容量大，被很多人用来存储自己喜爱的影视剧，但看剧不是特别方便，今天给大家介绍阿里云盘搭配 Infuse 播放器，影视剧自动载入海报，且支持多平台。

Infuse for Mac 效果：

![](https://i.imgur.com/7P8M6CX.png)

## 准备

- Infuse 软件。
- 支持安装阿里云盘 WebDVA 插件的系统，例如 X86 OpenWrt 系统的路由器。

## 获取 token

打开阿里云盘网页端，鼠标右键选择【审查】出现代码页面，点击【Application】-【Local Storage】网址 -【token】下拉找找到 `refresh token:` 并复制后面的字符。

![](https://i.imgur.com/RMq12OF.png)

## 设置阿里云盘 WebDAV

打开路由器后台插件阿里云盘 WebDAV，将上面复制的字符粘贴到 `Refresh Token`，主机地址填写您路由器 IP，用户名、密码、端口自定义，勾选【启动】再点击【保存&应用】。

> 注：云盘根目录默认可访问所有文件，如果您只想访问某个文件夹，例如电影，可以输入`/电影`。

![](https://i.imgur.com/YX1UkuP.png)

## 设置 Infuse

打开 Infuse，点击【新增文件来源】。

![](https://i.imgur.com/fHj7O4J.png)

点击【添加 WebDAV】。

![](https://i.imgur.com/RmipUGe.png)

- 名称自定义；
- 位置输入路由器 IP 地址；
- 用户名、密码、端口填入您刚在路由器设置的内容，点击【新增】。

![](https://i.imgur.com/PoHPdCl.png)

完成后可以将影视文件夹加入收藏，然后会自动加载封面显示。

![](https://i.imgur.com/s3w5ObM.png)
