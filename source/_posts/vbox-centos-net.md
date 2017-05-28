---
title: vbox centos net
tags:
  - centos
categories:
  - vbox
date: 2017-05-28 17:13:38
---
vbox 里设置 centos 的网络
<!--more-->

# NAT 可以访问外网
1. 网络网卡1 网络地址转换(NAT)
2. vi /etc/sysconfig/network-scripts/ifcfg-eth0 修改这一行 ONBOOT=yes
3. ifup eth0
4. ifconfig -a 查看ip
5. ping baidu.com 可以ping通


# Host-Only 和主机互访
1. 网络网卡2 仅主机hostonly 选个网卡 VirtualBox Host-Only Network #2 ip是 192.168.99.1
2. vi /etc/sysconfig/network-scripts/ifcfg-eth1


```	DEVICE=eth1
TYPE=Ethernet
ONBOOT=yes
BOOTPROTO=static
IPADDR=192.168.99.200
NETMASK=255.255.255.0
GATEWAY=192.168.99.1
HWADDR=08:00:27:14:08:95
```

3. ifup eth1
4. 访问主机 ping 192.168.99.1
5. 访问虚拟机 ping 192.168.99.200

# 问题
## 无法访问外部网络
  1. route add default gw 10.0.2.2
  2. ifdown eth0
  3. ifup eth0