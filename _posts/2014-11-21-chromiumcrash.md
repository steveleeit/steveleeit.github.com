---
layout: post
title: "chromium崩溃"
description: ""
category: 
tags: [linux]
---
{% include JB/setup %}
上次由于debian7(gnome3)字体的原因，略带强迫症的我重装了系统，在ubuntu，linuxmint，fedora之间来回切换了几次最终还是回到了debian,不过这次转用xfce桌面。

不知如何我换到了chromium（我承认我用了chromium之后发现iceweasel太慢），但是这个chromium经常崩溃，google了很多次没有解决。于是我就去下了chrome的deb包装，装上之后确实不会出现崩溃现象，但是我的代理插件就变得不好用了（用上代理也不能登录google账户），于是我还是把它删掉继续忍受着chromium的崩溃。

今天又不知怎么的我想从终端打开chromium，崩溃之后看到这样一条崩溃信息

fish: Job 1, 'chromium' terminated by signal SIGSEGV (Address boundary error)

遂google之，发现那些东西对我的用处不大（根本没有解决我的问题or我的英文太差看不懂他们在说什么？）。然后我百度了，看到ubuntu中文论坛上的一篇类似的帖子说：重装chromium就可以解决，但是装之前要先删除.config/.chromium文件夹。于是我照做解决了问题。

我想是因为我以前在debian7(gnome)的时候装过chromium留下的配置文件夹在作怪？（我重装系统只是格式化了/目录，保留了/home）

我也不想去深究，至少现在不想，我的问题解决了。


ADD:
问题还是没有解决，于是我换到了chrome，代理不能登录google帐号的原因找到了是因为插件权限的原因。

其中我还发现一个问题，不同的shell给出的error信息不一样！！！

我也是醉了。

最终我还是免受了崩溃的烦恼 orz。。。
