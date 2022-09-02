---
layout:     post
title:      搜狗输入法修改菜单栏图标
subtitle:   自定义 Logo
date:       2022-1-6
author:     河東
header-img: img/post-bg-huise.jpg
catalog: true
tags:
    - 输入法
--- 

⚠️ 不建议拿隐私换便捷，反之请往下看。

搜狗输入法的图标设计其实也还行，辨识度极高，但部分用户不喜欢，那么今天就教大家修改为自己喜欢的图标，例如改为 Mac 原生输入法图标。

## 准备图标

前往以下路径（自带输入法文件夹），找到 `.tiff` 格式的图标。

```
/System/Library/Input Methods/SCIM.app/Contents/PlugIns/SCIM_Extension.appex/Contents/Resources
```

![](https://i.imgur.com/yjW6EJi.png)

用预览打开（例如拼音），会出现 2 个图标，删除较模糊的。

![](https://i.imgur.com/4LRYiK8.png)

点击菜单栏导出，名称及格式为 `menubarpinyin.pdf`。

![](https://i.imgur.com/ToWbL6P.png)

## 更换图标

前往以下路径（搜狗输入法文件夹），将 `menubarpinyin.pdf` 文件放进去并替换，退出 Mac 重新进入，更换完成。

```
/Library/Input Methods/SogouInput.app/Contents/Resources
```

![](https://i.imgur.com/unIx33V.png)
