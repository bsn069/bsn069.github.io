---
title: centos7
tags:
  - centos7
categories:
  - linux
date: 2017-05-29 22:03:35
---
摘要
<!--more-->

# 阿里镜像
http://mirrors.aliyun.com/help/centos

# ip
1. 查看ip地址 ip address
2. 启动网卡 ifup enp0s8

# yum国内
1. yum install wget
1. mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup 
2. wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo 
3. yum makecache