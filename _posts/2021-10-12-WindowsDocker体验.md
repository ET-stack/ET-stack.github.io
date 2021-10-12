---
layout: post
title: "时隔几年我又拿起Windows的Docker"
category: Docker
tags: [Docker]
---
早在几年,Windows上的docker那时候bug百出，一大堆问题出现。而现在因为开发环境需要，我又拿起来了，感觉还不错安装虽然有一些小问题，但是解决很快。
## 新手入门教程
https://www.runoob.com/docker/docker-tutorial.html

## 问题

**Windows Docker Engine failed to start...**

启动失败，首先我是  Hype-V肯定是开启的。排除这个问题 怀疑是windows运行linux内核系统需要安装Linux 内核更新包

然后Windows+x+A 弹出管理powershell

`wsl --set-default-version 2`

显示需要更新

到 https://docs.microsoft.com/zh-cn/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package

下载 安装 更新 重新启动就好了
