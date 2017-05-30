---
title: centos cmd
tags:
  - centos
  - linux
categories:
  - centos
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

# systemctl
## systemctl start docker.service
## systemctl stop docker.service
## systemctl restart docker.service
## systemctl enable docker.service

# 关闭selinux
1. setenforce 0
2. sed -i '/^SELINUX=/c\SELINUX=disabled' /etc/selinux/config
