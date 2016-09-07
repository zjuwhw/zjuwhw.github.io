
---
layout: post
title: github的issue功能
date: 2016-09-01
tags: ["cs"]
---

讨论一下issue的使用。

## [github官网关于issue功能的介绍](https://guides.github.com/features/issues/)

- 简介

> Issues are a great way to keep track of tasks, enhancements, and bugs for your projects. They’re kind of like email—except they can be shared and discussed with the rest of your team. Most software projects have a bug tracker of some kind. GitHub’s tracker is called Issues, and has its own section in every repository.

Issues是一种非常好的跟踪你项目中任务、改善和bug的方式。它们某种程度上类似于邮件，但是它们可以与团队中其他人分享和讨论。大多数的软件项目有类似的bug跟踪器。GitHub的bug跟踪器就叫做Issues，而且每个目录都有自己的一个section。

- 功能

 - title和description：标题和描述
 - labels：标签，用于分类
 - milestone：时间点
 - assignee：指定
 - Comments：评论

- Notifications, @mentions, and References

 - Notifications：消息提醒
 - @mentions： 提到他人。github建议使用`/cc`，即carbon copy，概念抄送。
 - References： 依赖的其他issue、pr等

## requesting support（需求技术支持）和reporting bug（汇报bug）的区别

参考网址：https://coenjacobs.me/2013/12/06/effective-bug-reports-on-github/

- 简介

> The purpose of resolving a support ticket is to solve a problem for one user. A bug report is to explain a bug in the software, to make the software more stable.

解决技术问题是为一个客户解决一个问题。汇报bug是解释在软件中的一个bug，来使得软件更加稳定。

- 举例

 - requesting support

```
Error when using plugin X and Y
I just activated plugin X and now plugin Y shows this error: …. How can I resolve this?

使用插件X和Y的时候报错
我刚刚激活插件X和插件Y，它显示如下错误： 。。。怎么解决它呢？
```

 - reporting bug

```
Conflicting function name in plugin X and Y
Both plugins X and Y use function name … and this results in the error: …

插件X和插件Y函数名冲突
插件X和插件Y都使用了同一函数名。。。，这样就导致了报错：。。。
```

- 好的和坏的bug reporting

尽可能多的包含能帮助研发人员解决此bug的所有信息。

 - 坏的

```
Bug
I just uploaded it and it doesn’t work. I can’t create products. Please fix.

Bug
我刚刚上传它，但是它失败了，我不能创建products了。请帮我解一下
```

 - 好的

```
Parse error when creating new products (version 2.0)
I just activated this plugin (version 2.0) on a fresh WordPress 3.7.1 install. When I now try to create a new product, the following error shows: … This didn’t happen in the previous version, which I have just confirmed using version 1.9 on the same fresh install.

创建新product时解析错误（version 2.0）
我刚刚在WordPress 3.7.1细心地激活这个插件（version 2.0）.当我现在试着创建新的product的时候，出现了以下报错：。。。我刚刚确认这个在前一个版本（version 1.9）这是不会发生的。
```

## 我们公司目前github issue功能使用现状

- 好的方面

1. 题目、labels、assign等都有要求和规范的：https://github.com/genedock/DNA/blob/master/README.md
2. 只有四个repository启动issue功能：DNA、ideabank和新加的FirstLove、Diamonds
3. 我们是使用@mention和reference的

- 有待提高的地方

1. 我们提bug时候，如何规范描述，提好的bug，有待提高
2. 不是所有工程师都会设置[notification](https://github.com/settings/notifications)
3. 很多support requesting也开在issue中了。但是总要有个地方记这些客户问题呀，可能需要有技术支持论坛给客户和技术支持人员

## 参考资料：

- [Mastering Issues](https://guides.github.com/features/issues)
- [How to effectively report bugs on GitHub (and what not to do)](https://coenjacobs.me/2013/12/06/effective-bug-reports-on-github/)