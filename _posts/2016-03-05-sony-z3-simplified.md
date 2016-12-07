---
layout: post
title: Z3免root精简列表
categories: [其他]
tags: [索尼]
date: 2016-03-05 23:01:37
comments: true
---

### 步骤
1. 连接手机，开发者选项开USB调试，运行以下链接的“入口.bat”
[Z3Z3C精简adb.zip](http://pan.baidu.com/s/1jHQkc0e)
2. 输入adb shell
3. 按需要精简的程序，输入如下命令

### 精简指令
【1】移除 小窗口 （注，这个输入后需要重启手机才能消失，其余的不用）
<!--more-->
~~~css
pm block com.sony.smallapp.managerservice
pm block com.sony.smallapp.appframework
pm block com.sony.smallapp.launcher
pm block com.sony.smallapp.app.widget
~~~

【2】移除 更新中心
~~~css
pm block com.sonyericsson.updatecenter
~~~

【3】移除 备份和恢复
~~~css
pm block com.sonymobile.synchub
~~~

【4】移除 索尼精选
~~~css
pm block com.sonymobile.sonyselect
~~~

【5】移除 Xperia乐享汇
~~~css
pm block com.sonyericsson.xhs
pm block com.sonymobile.xperialounge.services
~~~

【6】移除 谷歌图书
~~~css
pm block com.google.android.apps.books
~~~

【7】移除 云端硬盘
~~~css
pm block com.google.android.apps.docs
~~~

【8】移除 谷歌新闻和天气
~~~css
pm block com.google.android.apps.genie.geniewidget
~~~

【9】移除 谷歌的Gmail
~~~css
pm block com.google.android.gm
~~~

【10】移除 Gmail读者服务
~~~css
pm block com.sonymobile.gmailreaderservice
~~~

【11】移除 环聊
~~~css
pm block com.google.android.talk
~~~

【12】移除 谷歌报亭
~~~css
pm block com.google.android.apps.magazines
~~~

【13】移除 谷歌地图
~~~css
pm block com.google.android.apps.maps
~~~

【14】移除 谷歌游戏
~~~css
pm block com.google.android.play.games
~~~

【15】移除 谷歌+
~~~css
pm block com.google.android.apps.plus
~~~

【16】移除 Lifelog
~~~css
pm block com.sonymobile.lifelog
~~~

【17】移除 影片创作工具
~~~css
pm block com.sonymobile.moviecreator.rmm
~~~

【18】移除 What’s New
~~~css
pm block com.sonymobile.advancedwidget.entrance
~~~

【19】移除 谷歌电影
~~~css
pm block com.google.android.videos
~~~

【20】移除 youtube
~~~css
pm block com.google.android.youtube
~~~

【21】移除谷歌搜索框
~~~css
pm block com.google.android.googlequicksearchbox
~~~

【22】移除 支持
~~~css
pm block com.sonymobile.helpapp7
~~~

### 恢复指令
如果需要恢复，将以上语句中的`block`改成`unblock`。

### 恢复 what’s new
~~~css
pm unblock com.sonymobile.advancedwidget.entrance
~~~

恢复 小窗口 （注，这个输入后需要重启手机才能消失，其余的不用）
~~~css
pm unblock com.sony.smallapp.launcher
pm unblock com.sony.smallapp.app.widget
~~~

![Z3免root精简]({{ site.url }}/assets/blogImg/z3_simplified_01.png)

### 参考文章
* [Z3/Z3 COMPACT 无ROOT精简，已测试，基本涵括全部该精简的程序](http://bbs.gfan.com/android-7729338-1-1.html)
* [Z3/Z3C最详细的精简列表，手写了4个小时，我自己都感动了](http://bbs.gfan.com/android-7744517-1-1.html)
