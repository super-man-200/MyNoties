# 1.Oracle简介

关系型数据库，支持分布式处理功能

## 1.特点

1.支持多用户、大事务量的事务处理

2.数据安全性和完整性控制

3.支持分布式数据处理

4.可移植性

Oracle就只有一个大的数据库





# 配置虚拟网络接口

为什么我们要自己配置网卡，因为系统分配的网卡不可以自己改网段，而自己创建的网卡就可以更改网段

## 1.桥接模式

 本机计算机和虚拟机处于同一个局域网，需要本机计算机插上网线连接交换机，才能与内部虚拟机进行通信，否则无法通信

## 2.仅主机模式

不受外部环境影响，相当于本地计算机和虚拟机用一根网线进行连接

## 3.NAT模式

本机计算机和虚拟机连接同一个网络，共享同一个IP地址，如果本机能够上网，那么虚拟机也可以上网