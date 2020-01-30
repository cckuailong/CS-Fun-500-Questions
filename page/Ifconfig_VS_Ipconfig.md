# 为什么Windows用ipconfig，Linux用ifconfig呢

## 前言

我的一位朋友习惯在Windows上编程，毕业设计时，开始使用学校的服务器进行Linux编程，
有时，习惯性使用ipconfig进行ip查询，导致报错。这个习惯一时改不过来，生气地说，
Linux里的ifconfig是不是打错了。哈哈，这个小插曲让我们发问，
为什么Windows用ipconfig，Linux用ifconfig呢？

## 解释

- ipconfig：Internet Protocol Configuring（IP地址配置）
- ifconfig：Network Interfaces Configuring（网络接口配置）

光从英文单词可以看出有点差别，但其实都是对网络的配置。
如果说为什么Linux用ifconfig而Windows用ipconfig的话，那么可以这样解释

- Linux下任何皆文件，任何皆设备，网络接口更接近设备

- Windows下用IP地址，可理解性更强

## 简单用法

### ipconfig

Windows中ipconfig实用程序可用于显示当前TCP/IP配置的设置值。这些信息一般用来检验人工配置的TCP/IP设置是否正确。

```
ipconfig            显示信息
ipconfig /all       显示详细信息
ipconfig /renew     更新所有适配器
```

### ifconfig

Linux中对应的程序是ifconfig.它用于查看、配置、启用或禁用位于内核中的网络接口，在系统引导时它被用来设置必要的网络接口参数。
可以用这个工具来临时性的配置网卡的IP地址、掩码、广播地址、网关等。

```
ifconfig            查看网络接口状态（当前激活的网络接口情况）
ifconfig -a         查看主机所有网络接口的情况
ifconfig eth0       查看某个（eth0）端口状态
```
