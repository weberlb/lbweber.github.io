---
layout: blog
title: Android代码折叠问题
date: 2023-12-27 18:07:32
categories:
- 技术文章
---
当Android Studio aar或者jar包的class文件时，有时会出现 /* compiled code */
因为Android Studio在初始化的时候会默认自带反编译插件，但是在有的因为安装大意，
<!--more-->
在初始化的时候没有勾选上反编译插件，从而导致不能正常的反编译，
这时候看到的代码智能显示函数名称，函数体内部的实现显示的是/compiled code/。

这个时候可以通过终重新勾选的方式来解决
**方法**
打开Android Studio，Android Studio->Settings->Plugins，
在installed的插件中搜索Java Bytecode Decompiler，勾选上后点击右下角的apply，然后再重启IDEA即可。

小贴士:
禁用掉自己下载的编译插件
禁用掉Java Decompiler Intellij Plugin，重启Android Studio后反编译成功