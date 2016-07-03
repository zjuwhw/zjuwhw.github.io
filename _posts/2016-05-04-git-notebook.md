---
layout: post
title: Git学习笔记
date:   2016-05-04
tags: cs
---

注：本文为git的学习笔记，全部内容来自《[pro git](https://git-scm.com/book/en/v2)》

## Chapter 1: Getting Started

```
配置文件
/etc/gitconfig
~/.gitconfig or ~/.config/git/config
.git/config
```
	
```
#全局设置
git config --global core.editor vim
#局部设置
git config --local user.name "name"
git config --local user.email "email"
#查看设置
git config --list
```

## Chapter 2: Git Basics

```
#Add file contents to the index
git add filename
```
```
#Record changes to the repository
git commit #打开文本编辑器
git commit -m "your text"
```
```
#克隆到本地
git clone https://github.com/zjuwhw/test-repo
```
```
#查看状态
#-untracted
#-tracked: unmodified, modified, staged
git status
git status -s #简短显示
```
```
#忽略跟踪文件或文件夹".gitignore"
$cat .gitignore
*.a
*.o
*.[ao] #以上两行可以利用正则合并成这一行
build/ #忽略文件夹
doc/**/*.pdf
```
```
#查看区别
git diff
git diff --staged
git diff --cached
```
```
#不再跟踪文件
git rm filename
```
```
#重命名
git mv old_filename new_filename
#相当于
mv old_filename new_filename
git rm old_filename
git add new_filename
```
```
#查阅历史
git log
git log -p #显示不同
git log -n #显示几个
git --stat #显示统计
git log --oneline #一行显示
git log --pretty=format: "%h %an %ar %s" #按照特定格式显示
git log --graph
git log --since=2.weeks
git log --since="2008-10-01"
```
```
#git log的format参数支持的特定格式
```

|Option|Descripton of Output|Option|Descripton of Output|
|:--|:--:|:--:|--:|
|%H|commit hash|%h|abbreviated commit hash
|%T|tree hash|%t|abbreviated tree hash
|%P|parent hashes|%p|abbreviated parent hashes
|%an|author name|%ae|author email
|%ad|author date|%ar|author data, relative
|%cn|committer name|%ce|committer email
|%cd|committer date|%cr|committer data, relative
|%s|subject


```
#remote
git remote
git remote -v
git remote add origin https://github.com/name/repo.git
```
```
git fetch
git push origin master
```

## Chapter 3: Git Branching

```
#查看branch
git branch
#新建branch
git branch newbranch
#切换branch
git checkout newbranch
#新建并切换branch
git checkout -b newbranch
```
```
#log中查看branch信息
git log --decorate
```
```
#合并一个分支
git checkout master
git merge issue#2940
#删除一个分支
git branch -d issue#2940
#删除一个远端的分支
git push origin --delete issue#2940
```
```
#查看merged或没有merged的分支
git branch --merged
git branch --no-merged
```