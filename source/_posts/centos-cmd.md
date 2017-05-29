---
title: centos cmd
tags:
  - centos
categories:
  - linux
date: 2017-05-29 21:13:57
---
centos cmd
<!--more-->


# 版本信息
##  cat /etc/issue
	CentOS release 6.4 (Final)
	Kernel \r on an \m

## cat /etc/redhat-release
	CentOS release 6.4 (Final)

## getconf LONG_BIT
	64

##  cat /proc/version
	Linux version 2.6.32-358.el6.x86_64 (mockbuild@c6b8.bsys.dev.centos.org) (gcc version 4.4.7 20120313 (Red Hat 4.4.7-3) (GCC) ) #1 SMP Fri Feb 22 00:31:26 UTC 2013

# CentOS 6.4 国内最快的YUM源163安装
1. 进入目录/etc/yum.repos.d
2. wget http://mirrors.163.com/.help/CentOS6-Base-163.repo
1. mv CentOS-Base.repo CentOS-Base.repo.bak
3. mv CentOS6-Base-163.repo CentOS-Base.repo
3. yum makecache 
