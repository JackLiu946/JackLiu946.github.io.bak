---
layout: post
title: '新手如何一步步搭建java web开发环境'
date: '2017-4-14'
header-img: "img/post-bg-android.jpg"
tags:
     - java web
author: 'LiuGui'
---


这篇文章学习Java web时针对初期开发环境搭建的说明文档，在新手学习环境搭建时有一定的作用，避免再次踩同样的坑。同时也是对自己学习的一个总结：


  一.建立Java环境
  
  Java环境主要指的是jdk，即Java Development Kit（Java语言的环境开发包SDK），里面包含Java开发环境，Java工具以及Java的基础类库。
 下面介绍jdk下载，安装，配置和测试过程：
（1）jdk的下载和安装
jdk由sun公司开发的，为java程序的开发提供了编译和运行环境。可以去www.oracle.com下载（根据自己电脑操作系统的类型区分32位和64位），下载完成后进行安装。
（2）jdk环境配置
安装后需要进行环境变量配置，设定JAVA_HOME,CLASSPATH和PATH.以Windows操作系统为例，在桌面我的电脑图标上右键选择属性后进入系统属性高级变量，在环境变量弹框中设置系统变量（变量名JAVA_HOME,变量值C:\Program Files\Java\jdk1.8.0_101），然后继续新建系统变量 CLASSPATH,变量值“.;%JAVA_HOME%\lib\;”。（注意，前面的.表示当前路径，此处必不可少。）；，最后修改Path系统变量，新增值“%JAVA_HOME%;%JAVA_HOME%\bin;”(注意，新增值与原值之间必须要有；号分隔)。
（3）验证jdk是否安装成功
在jdk环境配置完成后，我们可以通过cmd命令行（win+R）输入java -version，回车后会显示jdk的版本等相关信息即表示jdk安装配置成功。


二.建立Tomcat环境

Tomact是Apache软件基金会的核心项目，有Apache，sun和其他一些公司和个人共同开发而成，由于sun公司的参与和支持，Tomcat支持最新的JSP和servlet规范。因为Tomcat性能稳定，技术先进，而且免费而受到广大Java开发者的热爱，获得了行业的认可，成为比较流行的web服务器。
（1）Tomcat下载和安装
Tomcat是免费且开源的，官方下载地址为www.tomcat.apache.org 同样是根据自己电脑的系统进行下载并且安装。
（2）Tomcat环境配置
和jdk环境配置相似，Tomcat的环境配置过程，可以将下载完成后的文件解压缩后移到“C:\Program Files\”目录下，也可以根据自己的情况放在任意目录下，注意目录上不要有中文。然后在系统变量中新增“TOMCAT_HOME”,值设置为“C:\Program Files\apache-tomcat-7.0.54”，最后修改系统变量CLASSPATH新增“%TOMCAT_HOME%\lib”后确认。
（3）验证Tomcat是否安装成功
在C:\Program Files\apache-tomcat-7.0.54\lib中找到startup.bat(启动Tomcat服务器)，在shutdown.bat可以关闭服务。
开启服务后可以在浏览器上输入http://localhost:8080 (8080位Tomcat默认的端口号)，进入Tomcat的web管理页面。

三.搭建Java Web环境

（1）MyEclipse的下载和安装
MyEclipse是对Eclipse IDE的扩展，作为企业级工作平台，它可以为我们在数据库，javaEE开发，发布以及服务器的整合方面极大的提高了效率。MyEclipse是Eclipse的插件，我用的是破解版的，在破解过程中遇到了一些坑，需要重新安装一下myeclipse就好了。支持去官方网站http：//www.myeclipseide.com 上下载使用，这是对开发者的尊重，谢谢！
(2)在myeclipse中配置环境
MyEclipse中配置jdk时在菜单栏的Window-->Preference(首选项)命令弹框左侧选择Java->install JREs,在单击右侧的Add按钮后add JRE 弹框中选择Standart VM，在next后选择jre安装路径。
（3）在myeclipse中配置tomcat
在菜单栏的Window-->Preference命令弹窗出左侧选择servers-->tomcat-->tomcat 7.x,将Tomcat7.x server设置为Enable.在Tomcat home directory中选择Tomcat的安装路径或解压缩的配置目录。
（4）验证是否配置成功
在主页面的server栏中开启Tomcat，启动后在浏览器输入http://localhost：8080 即可测试。（页面为空白就是成功啦~）







> 如有任何知识产权、版权问题或理论错误，还请指正。
>
> 转载请注明原作者及以上信息。
	

> 如有任何知识产权、版权问题或理论错误，还请指正。
>
> 转载请注明原作者及以上信息。
