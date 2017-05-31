---
title: vbox tools
tags:
  - vboxtools
categories:
  - vbox
date: 2017-05-30 21:52:25
---
vbox 安装增强工具失败
<!--more-->


# Makefile.include.header:97: *** Error: unable to find the sources of your current Linux kernel. Specify KERN_DIR=<directory> and run Make again. 
1. 选设备 安装扩展工具(会挂在tools iso)
2. yum update
1. yum install gcc
3. yum install kernel-devel
5. yum install bzip2
4. shutdown -r now
5. 选新内核进入
5. mount /dev/cdrom /mnt
5. cd /mnt
5. ./VBoxLinuxAdditions.run 
4. shutdown -r now
5. cd /media
6. cd sf_
7. 看到共享文件夹了吧