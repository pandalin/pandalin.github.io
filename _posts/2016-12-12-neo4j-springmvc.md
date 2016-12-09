---
layout: post
title: Neo4j(二)整合springmvc
categories: [blog ]
tags: [neo4j, ]
description: Neo4j 整合springmvc项目
---

##  官网配置
    
 >   鉴于官网java相关的例子都是整合springboot，本文主要讲解neo4j整合springmvc项目
   
   [官网配置地址](https://neo4j.com/developer/java/)，里面提供了各种例子使用。
   
##  整合SDN

   > SDN名词解释： spring-data-neo4j
    
   > 以maven为例,**spring版本必须选择4.2及以上，低版本会出各种问题**
   
   ![pom]({{site.url}}/images/2016/12/12/pom.jpg) 
   
   > SDN3.X版本 ，选择3.x版本时，出现
   
   [问题](http://stackoverflow.com/questions/30254176/issues-while-retrieving-existing-nodes-using-spring-data-neo4j/30633870#30633870)
   
 ##  配置
    
   ![configuration]({{site.url}}/images/2016/12/12/configuration.jpg)
   
  > 此处造成springbean 循环初始化的问题是因为整合到现有项目中，模块耦合太严重，通过如下配置即可解决
  
  ![error]({{site.url}}/images/2016/12/12/error.jpg) 
  ![error1]({{site.url}}/images/2016/12/12/error1.jpg)
  
  > 在项目classpath中加入ogm.properties配置
    DriverConfiguration
  ![ogm]({{site.url}}/images/2016/12/12/ogm.jpg)
  
  > 关于driver 可参看org.neo4j.ogm.config.DriverConfiguration类说明
   
##  建模、定义接口
> 与官网相同

## 启动

> 启动项目，当看到如下信息时，表示整合成功

 ![start]({{site.url}}/images/2016/12/12/start.jpg)
    
  
  
   
   
   
   
    
  
    