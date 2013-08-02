---
layout: post
title: "未越狱ios设备的抓包方法"
date: 2013-08-02 19:52
comments: true
categories: 
---
##安装端口
[参考文献](http://fanliugen.com/?p=351)


打印现在所有的端口
	ifconfig -l
输出
	lo0 gif0 stf0 en0 en1 p2p0 fw0 ppp0 utun0
绑定设备的UDID, 可以从organizer中获取
	rvictl -s 74bd53c647548234ddcef0ee3abee616005051ed
输出
	Starting device 74bd53c647548234ddcef0ee3abee616005051ed [SUCCEEDED]
	network interface, rvi0, added by the previous command.
再次打印所有端口
	ifconfig -l
	lo0 gif0 stf0 en0 en1 p2p0 fw0 ppp0 utun0 rvi0
##开始抓包
到这里端口安装成功了, 接下来就要抓包了~~
	sudo tcpdump -i rvi0 -n -s 0 -w dump.pcap tcp
如果你的终端在你的根目录下面, 那在根目录下就会出现一个dump.pcap, 
这个文件可以用WireShark打开

##过滤不需要的ip
[ip过滤](http://netsecurity.51cto.com/art/201111/304449.htm)

	ip.src==192.168.0.105 or ip.dst==119.147.74.18

