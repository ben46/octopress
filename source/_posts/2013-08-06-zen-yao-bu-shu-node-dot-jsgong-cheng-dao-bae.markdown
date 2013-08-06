---
layout: post
title: "怎么部署node.js工程到bae"
date: 2013-08-06 20:26
comments: true
categories: 
---

记得如果用fs.readFile来读取文件的话, 要调用多一层文件夹
	fs.readFile('./app/json/hotel.list.json', "utf8", function (err, data) {

