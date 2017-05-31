---
title: docker gdb
tags:
  - centos
  - docker
  - gdb
categories:
  - docker
date: 2017-05-31 17:13:39
---
docker 里使用gdb
<!--more-->

# warning:Error disabling address space randomization: Operation not permitted
1. 添加--security-opt seccomp=unconfined
	> docker run -it --security-opt seccomp=unconfined -v  /media:/media bsn/cppdev

# Missing separate debuginfos, use: debuginfo-install glibc-2.12-1.107.el6.i686
1. 需要先修改“/etc/yum.repos.d/CentOS-Debuginfo.repo”文件的enable=1；
2. 使用 sudo yum install glibc 安装；
3. 使用 debuginfo-install -y glibc-2.12-1.132.el6.i686 安装。
