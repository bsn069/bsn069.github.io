---
title: centos7
tags:
  - centos7
  - linux
  - centos
categories:
  - centos7
date: 2017-05-29 22:03:35
---
摘要
<!--more-->

# ip
1. 查看ip地址 ip address
2. 启动网卡 ifup enp0s8
3. 设置开机启动 /etc/sysconfig/network-scripts/ifcfg-eno16777736"里面的"ONBOOT=no"修改成"ONBOOT=yes",至此问题彻底解决！

# CentOS 6.4 国内最快的YUM源163安装
1. cd /etc/yum.repos.d
2. yum install wget
2. 
	1. wget http://mirrors.163.com/.help/CentOS6-Base-163.repo
1. mv CentOS-Base.repo CentOS-Base.repo.bak
3. mv CentOS6-Base-163.repo CentOS-Base.repo
3. yum makecache 