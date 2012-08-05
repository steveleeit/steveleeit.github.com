---
layout: post
title: "Dropbox做图床+绑定域名"
description: "Dropbox"
category: 'Dropbox' 
tags: [图床]
---
{% include JB/setup %}
Dropbox 文件外链的形式是http://dl.dropbox.com/u/xxxxxx/asd.pig 
大家都知道在国内被墙了，但是现今还是可以通过绑定域名来解决。 
在你的域名里添加一个cname记录 
dl.yourdomain.com  》 dl.dropbox.com 
坐等生效，然后把链接写成http://dl.yourdomain.com/u/xxxxxx/asd.pig就大功告成了。  
我想这应该也适用与其他文件的分享，并且在分享的同时还保存了文件，一举两得。

参考:http://chinese-alternative.blogspot.com/2012/07/dropbox-cloudflare.html
