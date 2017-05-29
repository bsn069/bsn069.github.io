---
title: centos7 install docker
tags:
  - docker
  - centos7
categories:
  - docker
date: 2017-05-29 22:15:59
---
摘要
<!--more-->
# 关闭selinux
1. setenforce 0
2. sed -i '/^SELINUX=/c\SELINUX=disabled' /etc/selinux/config

# 安装
1. yum install docker

# 设置为开机启动：
1. systemctl start docker.service
2. systemctl enable docker.service

# 重启
systemctl restart docker.service



# 问题
1. Job for docker.service failed because the control process exited with error code. See "systemctl status docker.service" and "journalctl -xe" for details.
	1. 设置docker 镜像源加速器 回到只启动失败
curl -sSL https://get.daocloud.io/daotools/set_mirror.sh | sh -s http://48b042ae.m.daocloud.io
生成 /etc/docker/daemon.json
移除/etc/docker/daemon.json