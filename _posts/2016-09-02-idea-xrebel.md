---
layout: post
title: Xrebel项目监控调优
categories: [blog ]
tags: [idea, ]
description: Xrebel项目监控调优
---

# 简介
  [XRebel](https://zeroturnaround.com/software/xrebel/) 是不间断运行在 web 应用的交互式分析器，当发现问题会在浏览器中显示警告信息。XRebel 会实时监测应用代码的性能指标和可能会发生的问题。

# Xrebel安装  

[Xrebel下载地址](https://zeroturnaround.com/software/xrebel/download/#!/have-license)  

[IDEA安装方法](http://manuals.zeroturnaround.com/xrebel/install/index.html#intellij-idea)

# 激活

  在浏览器输入：http://localhost:8080/Xrebel，在页面左下角会看到

  ![Xrebel监控画面]({{site.url}}/images/2016/09/xrebel_start.jpg)

 首次使用激活采用license server：[http://idea.lanyus.com](http://idea.lanyus.com)/your username进行激活

 激活后就能用Xrebel进行监控啦，每个sql执行时间，每次请求都有详细记录
