---
layout: post
title: IDEA热部署
categories: [blog ]
tags: [idea, ]
description: IDEA热部署
---

# IDEA安装
  本文使用IDEA最新版本2016.2.3 [IDEA][d856fe09] ，直接安装就好啦，社区版是免费的，旗舰版是收费的，我们要开发web项目，当然得下载旗舰版了，不要担心收费问题。再次提供一个神奇的网址（给屌丝用，土豪请随意）：
[IDEA破解][f08ac42e]，获取注册码再IDEA安装界面输入激活码就能正常使用了。

# Jrebel安装

下面讲idea上web项目热部署神器jrebel的安装与激活

>1 打开File->Setting菜单，在plugin中搜索jrebel,在线安装好idea的jrebel插件

 ![idea jrebel]({{site.url}}/images/2016/09/_idea_jrebel_setting.png)
 安装后重启IDEA

>2 正常安装后是处于未激活状态，此时的jrebel是不能使用的

# Jrebel 激活
  土豪请随意，屌丝玩家再次给大家提供一个情趣网站,[myjrebel][c8e1be28]，用你的facebook或者tiwwter授权登录（不要告诉我不会翻墙，博主第一次听别人说翻墙的时候，博主回答到小时候就会了，被摔得很惨，然后就没有然后了....），登录进去后是这样的
![  jrebelCode]({{site.url}}/images/2016/09/_jrebel_code.png)
拿到你的jrebel激活码后，返回IDEA->Help->Jrebel->Activation,输入激活码就能成功激活了。
接下来就是见证奇迹的时刻了，如果你的项目使用MAVEN进行管理，请看这里的详细配置
[idea中jrebel详细配置][46f5be97]，虽然是全英文，但步骤很清晰。

、、、xml

<plugin>
    <groupId>org.zeroturnaround</groupId>
    <artifactId>jrebel-maven-plugin</artifactId>
    <version>1.1.5</version>
    <executions>
        <execution>
            <id>generate-rebel-xml</id>
            <phase>process-resources</phase>
            <goals>
                <goal>generate</goal>
            </goals>
        </execution>
    </executions>
    <configuration>
        <rebelXmlDirectory>${basedir}/src/main/webapp/WEB-INF/classes</rebelXmlDirectory>
    </configuration>
</plugin>

、、、

  [d856fe09]: https://www.jetbrains.com/idea/ "IDEA"
  [f08ac42e]: http://idea.qinxi1992.cn/ "IDEA破解"
  [c8e1be28]: https://my.jrebel.com "myjrebel"
  [46f5be97]: http://zeroturnaround.com/software/jrebel/quickstart/intellij/ "idea中jrebel详细配置"
