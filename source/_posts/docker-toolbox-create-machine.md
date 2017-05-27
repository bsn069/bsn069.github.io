---
title: docker-toolbox create machine
tags:
  - self
categories:
  - docker
date: 2017-05-27 21:29:26
---
# 安装docker-toolbox后，进入虚拟机的docker
<!--more-->
# 前期准备
1. 用户 Administrator
2. docker-toolbox安装目录 D:\Program Files\Docker Toolbox

# 步骤
1. 进入docker-toolbox安装目录 
2. 网络不好的 复制boot2docker.iso到C:\Users\Administrator\.docker\machine\cache目录下 断网
3. 打开命令行 执行以下命令
    1. cd /d "D:\Program Files\Docker Toolbox"
    2. docker-machine.exe create --driver=virtualbox default

# 命令
## docker-machine.exe ls
    D:\Program Files\Docker Toolbox>docker-machine.exe ls
    NAME      ACTIVE   DRIVER       STATE     URL                         SWARM   DOCKER    ERRORS
    default   -        virtualbox   Running   tcp://192.168.99.100:2376           v1.13.1

## docker-machine.exe env default
    SET DOCKER_TLS_VERIFY=1
    SET DOCKER_HOST=tcp://192.168.99.100:2376
    SET DOCKER_CERT_PATH=C:\Users\Administrator\.docker\machine\machines\default
    SET DOCKER_MACHINE_NAME=default
    SET COMPOSE_CONVERT_WINDOWS_PATHS=true
    REM Run this command to configure your shell:
    REM     @FOR /f "tokens=*" %i IN ('docker-machine.exe env default') DO @%i

## docker-machine.exe stop default
    D:\Program Files\Docker Toolbox>docker-machine.exe stop default
    Stopping "default"...
    Machine "default" was stopped.

## docker-machine.exe start default
    Starting "default"...
    (default) Check network to re-create if needed...
    (default) Waiting for an IP...
    Machine "default" was started.
    Waiting for SSH to be available...
    Detecting the provisioner...
    Started machines may have new IP addresses. You may need to re-run the `docker-machine env` command.

# ssh
1. 默认用户名 docker 	密码 tcuser
2. ssh进入后执行 sudo -i 即可进入root用户
3. ip 可通过docker-machine.exe ip 查看