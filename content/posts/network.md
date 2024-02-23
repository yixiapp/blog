+++
title = 'Network'
date = 2024-02-23T14:15:12+08:00
tags = ["网络"]
categories = ["windows"]
draft = true
+++

#### 用 PING 命令查看目标地址是否可用

`
ping cn.bing.com
`
可以用域名，也可以用ip地址
ping -t 可以一直运行，直到关闭命令窗口或者按下 ctrl+c
但是有些机器是禁止被ping的

#### 用 TELNET 查看端口是否可用
window环境需要下载这个软件使用
`
telnet 192.168.1.130 8080
`
可以用域名，也可以用ip地址
网络不通会报错，网络如果通了，窗口全黑，这时关掉这个窗口即可

#### 用 NSLOOKUP 命令查看网址的 DNS 和域名的别名
一般用于查看设置的域名解析是否生效

**非交互模式**
`
nslookup cn.bing.com
`
**交互模式**
`
nslookup
`
> 可以多次输入地址，直到按下 ctrl+c

附：资源记录的含义
![20240223144328](http://qiniu.yixiapp.com/image/sap/2024/20240223144328.png)
可以试试下面命令，依次输入
```
nslookup
set ty=A
baidu.com
```