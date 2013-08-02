---
layout: post
title: "安装UI7Kit"
date: 2013-08-02 19:49
comments: true
categories: 
---
今天安装UI7kit的时候遇到一个问题: 
	[!] The target `RumourGuard [Debug]` overrides the `HEADER_SEARCH_PATHS` build setting defined in `Pods/Pods.xcconfig'.

解决办法:
在 HEADER_SEARCH_PATHS里面加入{inherit}
