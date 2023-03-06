---
title: 互换 Ctrl / Caps_Lock 按键
date: 2016-05-05 20:36:40
tags:
- 系统
---

> 交换 Caps_Lock 与 Ctrl 键，与 Unix 键位统一方便快捷键使用

## Mac OS

打开系统编好设置 选择 "键盘" 菜单，在 "键盘" 选项卡右下角打开 "修饰键..." 选单

大写锁定键 -> 选择 Control
Control键 -> 选择 大写锁定键

选择 "好" 即可完成设置

> 新版系统中 轻触大写锁定键 的功能为 切换中英文输入法，若要打开大写锁定需要长按大写锁定键（即修改后的 Control 键位）

## Ubuntu / Debian

<!-- more -->
新增或修改 ~/.Xmodmap 文件

```bash
sudo vim ~/.Xmodmap
```

添加内容

```bash
remove control = Control_L
remove lock = Caps_Lock
keysym Caps_Lock = Control_L
keysym Control_L = Caps_Lock
add control = Control_L
add lock = Caps_Lock
```

添加至 .profile 开机自启动

```bash
sudo vim ~/.profile
```

添加启动项目延时启动
```bash
sleep 4 && xmodmap ~/.Xmodmap &
```

>重新启动后生效

## Windows 10 & 11

>[Windows PowerToys](https://github.com/microsoft/PowerToys/releases/)