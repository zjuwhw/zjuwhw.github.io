---
layout: post
title: 软件工程的几个“-ilities”
date: 2017-01-11
tags: ["cs"]
---

注：本文翻译自[《The 7 Software “-ilities” You Need To Know》](http://codesqueeze.com/the-7-software-ilities-you-need-to-know/)。

### 引子

> In the world of software architecture there are many “-ilities” you must take into consideration with every project. Prioritizing them is necessary because the client will optimistically ask that you do all of them. To help you out, here is a quick list outlining my top 7 default “-ilities” in the order that I prioritize them:

在软件架构的领域，每个项目你都有很多“-ilities”需要考虑。由于你的客户希望你全都做到，所以你需要排好他们的优先级（prioritizing）。这是一个快速的清单，我认为的前7个“-ilities”，帮你排优先级。

### Usability（易用性）

> Software usability can be described as how effectively end users can use, learn, or control the system. Some questions to ask yourself to determine usability might be:

> - Is there a UI metaphor that I am using to help users adapt? (for example, the ‘desktop’ is a metaphor)
- Are the most common operations streamlined to be performed quickly?
- Can new users quickly adapt to the software without help? (is it intuitive?)
- Do validation and error messages make sense?

**软件的易用性**可以被描述为“终端用户可以如何邮箱的使用、学习、控制该系统”。你需要问自己一些问题来确认可用性：

1. 是否有一个“UI隐喻”可以使用，去帮助客户适应环境？（例如，“桌面”就是一个“隐喻”）（翻译者注：我理解metaphor就是一个类比的概念吧）
2. 是否所有常用的操作都可以快速、行云流水一般的进行？
3. 是否新用户可以无需帮助快速适应软件？（满足直觉吗？）
4. 验证和报错是否合理呢？

### Maintainability (可维护性），Flexibility（灵活性），Testibility（可测试性） 

> The definition of maintainability [for me] implies how brittle the code is to change. As a result, I tie the terms flexibility and testability into the overall maintainability of a project.

> - Does the entire team understand the code base or does knowledge islands exist?
- Is the code throughly regression tested?
- Can modifications to the project be done in a timely manner?

**软件的可维护性**体现“代码是多脆弱去改变”。因此，我也加入了另外两个此会“灵活性”和“可测试性”。

1. 整个团队都理解代码基础吗？或者是否存在知识孤岛？
2. 所有代码彻底做回归测试吗？
3. 对于项目的修改可以在合理的时间内完成吗？

### Scalability 可扩展性

> Scalability is the ability for your program to gracefully meet the demand of stress caused by increased usage. In short, ensuring your program doesn’t slow or bust when pounded by more users than you originally anticipated.

> - What is your current peak load that you can handle?
- How many database records can create until critical operations slow down?
- Is the primary scaling strategy to “scale up” or to “scale out” — that is, to upgrade the nodes in a fixed topology, or to add nodes?

**软件的可扩展性**指你的程序可以很优雅地应对来自使用量增加带来的压力增加。简短说，当用户量超过你之前预期的时候，你要保证你的程序不会变慢或者崩溃。

1. 你目前可以掌控的峰值是多少？
2. 创建的数据记录达到多少会使得关键的操作变慢？
3. 主要的扩展策略是增加节点或者升级节点吗？

### Availability (or Reliability) 可用性或者可靠性

> How long the system is up and running and the Mean Time Between Failure (MTBF) is known as the availability of a program.

> - How long does the system need to run without failure?
- What is the acceptable length of time for the system to be down?
- Can down times be scheduled?

你的系统可以抑制跑多长？失败间隔时间被用来衡量一个程序的可用性。

1. 你的系统可以跑不失败的跑多长？
2. 你的系统可以接受多长时间的宕机？
3. 宕机时间是否可以预定？


### Extensibility 可升级性

> Are there points in the system where changes can be made with (or without) program changes?

> - Can the database schema flex to accommodate change?
- Does the system allow Inversion of Control (IoC)?
- Can end users extend the system (scripts, user defined fields, etc)?
- Can 3rd party developers leverage your system?

当程序改变之后，系统中哪些会改变，哪些不会改变？

1. 数据库模式是否有弹性容纳改变？
2. 系统是否允许控制反转（Inversion of Control）？
3. 终端用户可以扩展系统吗？（脚本，用户自定义领域，等）
4. 第三方开发人员可以利用你的系统吗？

### Security 安全性

> I shouldn’t need to go into this one but to be thorough I like this definition of security: the measure of system’s ability to resist unauthorized attempts at usage or behavior modification, while still providing service to legitimate users.

> - Does the system need user or role based security?
- Does code access security need to occur?
- What operations need to be secured?
- How will users be administered?

我本不必要再解释它了，但是为了全面，我还是想定义一下安全性：系统对未授权使用和修改行为的应对并同时保持对合法用户提供服务的能力。

1. 系统是否需要用户/角色安全？
2. 代码获取安全是否需要？
3. 什么操作需要被保护？
4. 用户会怎样被管理？

### Portability 轻便性

> Portability is the ability for your application to run on numerous platforms. This is can include actual application hosting, viewing, or data portability.

> - Can the data be migrated to other systems?
- For web applications, which browsers does your web app support?
- Which operating systems does your program run on?

轻便性指的是你的应用在各种平台上运行的能力。这包括应用托管、查看、数据轻便性。

1. 数据可以迁移到其他系统中吗？
2. 对于网络应用，哪些浏览器支持？
3. 你的程序可以在哪些操作系统中使用？

### 结尾

> Obviously, this is not an exhaustive list. There are many many more (Backwards compatibility, Interoperability, and Reusability to name a few).

> What is your “-ilities” list? Which do you prioritize over others?


和显然，这不是一个穷尽的清单，还有太多太多了（向后兼容性、互用性、复用性等）

你的“-ilities”清单是什么？哪一个比其他的优先级更高呢？