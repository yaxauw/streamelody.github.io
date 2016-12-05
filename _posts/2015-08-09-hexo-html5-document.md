---
layout: post
title: 在Hexo博客中添加HTML5文档
categories: [博客]
tags: [hexo, html5]
date: 2015-08-09 21:50:29
comments: true
---

### 添加HTML5文档方法

1. 将需要的文档转为PDF文档。

2. 通过[idrsolutions](https://www.idrsolutions.com/online-pdf-to-html5-converter/)的`Online PDF to HTML5 Converter`在线功能转换得到HTML5文档。
<!--more-->
<img src="{{ site.url }}/assets/blogImg/idrsolutions_doc_html5.png" width="296" alt="idrsolutions在线文档转HTML5"/>

3. 将HTML5文档放到`Hexo/source/assets/html5`下。

4. 编辑hexo下的`_config.yml`，跳过渲染source文件夹下assets下html5的全部文件以及子目录。
~~~css
skip_render:
- assets/html5/*
- assets/html5/**/*
~~~

5. 添加HTML5文档，width和height可以自己调节最佳参数。
~~~css
<iframe width="86%" height="460" scrolling="auto" frameborder="0" src="HTML5网页地址"></iframe>
~~~

### 示例文档
<iframe width="86%" height="460" scrolling="auto" frameborder="0" src="{{ site.url }}/assets/html5/pic_prepare/index.html"></iframe>

### 参考文章
* [《如何不处理source目录下某个子目录的所有文件，仅仅是将其copy到public目录中对应目录？》](https://github.com/hexojs/hexo/issues/1146)
* [《在主目录下添加README.md文件或者html文件》](https://xuanwo.org/2014/08/14/hexo-usual-problem/#u5728_u4E3B_u76EE_u5F55_u4E0B_u6DFB_u52A0README-md_u6587_u4EF6_u6216_u8005html_u6587_u4EF6)
* [《Hexo 3.1.1 generate Error: expected end of comment, got end of file》](https://github.com/hexojs/hexo/issues/1604)
