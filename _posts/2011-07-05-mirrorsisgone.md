---
layout: post
title: "源抛锚了"
description: "开源镜像"
category: 
tags: [源]
---
{% include JB/setup %}
Archlinux的中科大源抛锚了，是在同步么？

{% highlight php %}
stevelee@myhost ~]$ sudo pacman -S gimp
正在解决依赖关系...
正在查找内部冲突...

目标 (5)： libwmf-0.2.8.4-8  libmng-1.0.10-3  babl-0.1.4-1  gegl-0.1.6-1
gimp-2.6.11-5

全部下载大小:   10.26 MB
全部安装大小:  61.56 MB

进行安装吗？ [Y/n] y
:: 正在从 extra 软件库获取软件包...
^C^[[A^[[B^[[A^C^C^C^C^C^C^C^C^C^C
Interrupt signal received

[stevelee@myhost ~]$ sudo pacman -Syy gimp
:: 正在同步软件包数据库...
core                     35.9K   17.8K/s 00:00:02 [######################] 100%
错误：无法从 mirror.bjtu.edu.cn 获取文件 'extra.db'[#---------------------]   5%
错误：无法升级 extra (无法获取某些文件)
^C
Interrupt signal received

[stevelee@myhost ~]$
{% endhighlight %}
