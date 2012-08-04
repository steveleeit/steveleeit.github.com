---
layout: post
title: "折腾翻页和代码高亮"
description: "jekyll"
category: 
tags: [折腾]
---
{% include JB/setup %}
jekyll默认的翻页实在是惨不忍睹，遂折腾。

折腾代码参考：http://geeklu.com/

不过直接照搬的画效果不是那么理想，于是就有了后面的折腾，作为一个html菜鸟，只有靠蒙了这个。

对比 http://geeklu.com/的index.html和我博客主题自带的index.md修改。效果见首页。

刚刚测试代码高亮也行了:

在highlight后面要加上语言（C,python,php,and etc.）
{\% highlight python \%}
#!/usr/bin/python
##FILENAME = hello.py
print "hello world"
{\% endhighlight \%}

效果：
{% highlight python %}
#!/usr/bin/python
##FILENAME = hello.py
print "hello world"
{% endhighlight %}
