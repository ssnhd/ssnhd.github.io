---
layout: post
title: Mac 允许任何来源，关闭 SIP 等常见设置
subtitle: 修改启动台行列数、程序坞显示时间、更改密码位数
date: 2022-1-23
author: 河東
header-img: img/macos/post-bg-macos.jpeg
catalog: true
top: false
tags:
  - Mac
  - macOS
---

新买的 Mac 你可能需要对下列几项进行设置。

## 启动台行列

【终端】输入或粘贴以下命令，修改后面的数字更改行列数。

行数

```
defaults write com.apple.dock springboard-rows -int 9
```

列数

```
defaults write com.apple.dock springboard-columns -int 10
```

最后输入以下命令

```
killall Dock
```

## 程序坞显示时间

如果你习惯隐藏程序坞，鼠标放在屏幕底部，默认显示程序坞非常慢，你可以在【终端】输入或粘贴下面命令，将数值改为 `0`，这样，显示程序坞会变的很快。

```
defaults write com.apple.dock autohide-delay -int 0
```

再输入下面命令。

```
killall Dock
```

## 允许任何来源

安装非 App Store 里应用，可能会出现无法安装的情况，需要打开任何来源。【终端】输入或粘贴以下命令，按回车键。

```
sudo spctl --master-disable
```

## 密码位数

管理员默认密码至少为 `4` 位，【终端】输入或粘贴以下命令支持将密码改为 `1` 位。

```
pwpolicy -clearaccountpolicies
```

## 深色主题显示浅色窗口

程序坞和菜单栏深色，窗口是浅色。

1. 【终端】输入或粘贴以下命令，按回车键
2. 注销并重新登录 Mac
3. 系统偏好设置 - 通用 - 深色。

```
defaults write -g NSRequiresAquaSystemAppearance -bool Yes
```

恢复

```
defaults delete -g NSRequiresAquaSystemAppearance
```

## 查看 SIP 状态

【终端】输入 `csrutil status`，按回车键。

### 关闭 SIP

1. Mac 开机立即按住 `Command-R`
2. 进入实用工具窗口，点击**实用工具**里【终端】，输入下面命令按回车键，重启 Mac

```
csrutil disable
```

### 开启 SIP

同上，【终端】输入下面命令。

```
csrutil enable
```
