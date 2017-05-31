---
title: centos7 install docker
tags:
  - docker
  - centos7
  - linux
categories:
  - docker
date: 2017-05-29 22:15:59
---
摘要
<!--more-->

# 方法1 https://store.docker.com/editions/community/docker-ce-server-centos?tab=description

1. yum install -y yum-utils
2. yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
3. yum makecache fast
4. yum -y install docker-ce
5. systemctl start docker
7. 设置刀云镜像
	1. curl -sSL https://get.daocloud.io/daotools/set_mirror.sh | sh -s http://48b042ae.m.daocloud.io
	2. 生成 /etc/docker/daemon.json
5. systemctl restart docker
6. docker run hello-world
8. systemctl enable docker.service





