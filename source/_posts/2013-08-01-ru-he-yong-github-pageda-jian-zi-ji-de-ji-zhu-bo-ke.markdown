---
layout: post
title: "如何用github page搭建自己的技术博客"
date: 2013-08-01 22:01
comments: true
categories: 
---
我参考的网站: 

* [唐巧的博客](http://blog.devtang.com/blog/2012/02/10/setup-blog-based-on-github/)<br/>
* [参考文献二](http://beiyuu.com/github-pages/)

然后这里这里还有一步: [参考官方文档](http://octopress.org/docs/deploying/github/)<br/>

	sudo rake setup_github_pages
	sudo rake generate
	sudo rake deploy
执行完rake deploy之后一般会直接帮你部署到github, 比如我的就是ben46.github.com这个仓库,<br/>
如果部署失败的话, 你就要手动部署了, 进入_deploy这个文件夹, 然后
	sudo git add remote origin ben46.github.com

最后你应该还要同步一下你的整个Octopress仓库, 目前好像只能在命令行下面管理git, 因为所有的权限都是sudo.

