---
layout: post
title: "Debian On T42 安装笔记"
description: ""
category: '笔记' 
tags: [debian]
---
{% include JB/setup %}
介于上次安装debian（ISO CD-1）的的悲催遭遇，作此篇整理出现的问题以及解决方法。

安装完成换源
vim /etc/apt/source.list

加入

deb http://mirrors.ustc.edu.cn/debian/ squeeze main non-free contrib
deb http://mirrors.ustc.edu.cn/debian/ squeeze-proposed-updates main non-free contrib
deb-src http://mirrors.ustc.edu.cn/debian/ squeeze main non-free contrib
deb-src http://mirrors.ustc.edu.cn/debian/ squeeze-proposed-updates main non-free contrib

1.中文乱码。

原因：缺少中文字体.

解决方法：

找一个中文字体（我找的是ubuntu下的wqy）

mv -rf  字体文件夹(例如我的是wqy) /usr/share/fonts/truetype/

OK,过一会儿中文就来了。

2.中文输入法。

切忌不可aptitude install fcitx 会导致X被删除

方法：

加源：deb http://backports.debian.org/debian-backports squeeze-backports main

apt-get install fcitx

用im-config配置环境变量

3.终端自动补全

apt-get install bash-completion （一般默认已经安装）vim /etc/bash.bashrc

找到

\#if [ -f /etc/bash_completion ]; then

\# . /etc/bash_completion

\#fi

去掉注解，然后更改用户目录的 bashrc

vim ~/.bashrc 加入一行source /etc/bash_completion

4.浏览器中文

apt-get install iceweasel-l10n-zh-cn

5.影音播放

apt-get install mplayer smplayer (前端smplayer 后端mplayer)

6.文件查看(PDF)

默认有evince 不过在程序菜单不能找到，只能终端运行evince

7.辞典（星际译王）

apt-get install stardict
然后着牛津高阶的deb安装包

8.升级lceweasel(解决部分插件不兼容)

http://mozilla.debian.net/

9.flash插件
apt-get install flashplugin-nonfree

10.安装基本编译环境

apt-get install gcc make automake

11.ftp软件

apt-get install gftp

11.安装开发环境

apt-get install vim subversion git

12.配置vim简单缩进，高亮

vim ~/.vimrc
syntax on #高亮开

set sw=4

set ts=4

filetype indent on

autocmd FileType python setlocal et sta sw=4 sts=4  ##适合python的缩进方案

set nu #显示行数

if &term=="xterm"

set t_Co=8

set t_Sb=^[[4%dm

set t_Sf=^[[3%dm
endif

解压软件

apt-get install unrar unzip p7zip-full

部分出处:
http://blog.csdn.net/laichao1112/article/details/6320067
http://mirrors.ustc.edu.cn/
http://linux-wiki.cn/wiki/zh-hans/Vim%E4%BB%A3%E7%A0%81%E7%BC%A9%E8%BF%9B%E8%AE%BE%E7%BD%AE
http://blog.csdn.net/jsufcz/article/details/387895
