---
layout: post
title: screen命令
date:   2016-08-08
tags: cs
---

```
screen -ls
screen -S
screen -r
screen -wipe
```

|C-a ?	|显示所有键绑定信息|
|C-a w	|显示所有窗口列表|
|C-a C-a	|切换到之前显示的窗口|
|C-a c	|创建一个新的运行shell的窗口并切换到该窗口|
|C-a n	|切换到下一个窗口|
|C-a p	|切换到前一个窗口(与C-a n相对)|
|C-a 0..9	|切换到窗口0..9|
|C-a a	|发送 C-a到当前窗口|
|C-a d	|暂时断开screen会话|
|C-a k	|杀掉当前窗口|
|C-a [	|进入拷贝/回滚模式|
