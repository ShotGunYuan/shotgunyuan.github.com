---
layout: post
title: "在VmWare上安装Mac OS X"
tagline: "VmWare Install Mac OS X"
description: "在Vmware虚拟机上安装Mac OS X 10.8"
tags: [VmWare,虚拟机,Mac,OS,操作系统]
---
{% include JB/setup %}

最近，有朋友在VmWare安装Mac系统的时候出了点问题。以前曾经成功安装过一次，因此就把安装过程记录下来。

###准备工作

1.	虚拟机系统：vmware workstation 10。
2.	Mac Os Mountain Lion。[Mac Os Mountain Lion 10.8.5镜像下载][1]
3.	注意还需要VmWare的Mac补丁，没有这个是无法成功安装的。[VmWare10的Mac补丁下载][2]
4.	安装中使用到的工具：好压、ultraISO。

###开始安装

在安装之前请先将下载的DMG系统镜像文件转换成ISO的格式，下面是转换的步骤：

1.	先用“好压”解压下载的DMG文件，将2.hfs解压出来。
2.	然后再用“好压”解压2.hfs，解压完之后找到4GB多的文件夹打开，打开后继续找4GB的文件夹再打开，反复多次直到找到InstallESD.dmg。
3.	使用ultraISO打开InstallESD.dmg，格式转换为ISO。

运行VmWare10的Mac补丁：把下载的补丁解压后，会有好几个文件夹，分别针对不同的操作系统。请以系统管理员身份运行windows文件夹下的install.cmd。

###创建虚拟机

打开VmWare，创建一个虚拟机，上面选择Apple Mac OS X(M)，下面选择Mac OS X 10.8。

**注意10.8.5版本的Mac OS需要分配至少2G的内存**。

其他配置则按默认选择。

###安装苹果系统

1.	载入镜像并开启虚拟机以后，选择语言(这里我选择简体中文)，点击下方的箭头。
2.	进入OS X工具界面，选择“磁盘工具”，点击继续进行磁盘分区。
3.	进入分区界面，左侧选择创建好的虚拟磁盘，右侧选择分区。
4.	分区布局下方的“+”可以增加一个分区，分区信息里可以设置分区的名称、大小、格式(我只添加了一个分区，名称自己定义，大小和格式默认)，分配好之后点击“应用”，弹出对话框选择“分区”。
5.	左上角红色“x”关闭分区工具，选择“重新安装OS X”,点击继续->继续->同意->同意。
6.	选则刚才分配好的分区，点击“安装”，等待安装完成。


[1]:http://kuai.xunlei.com/d/dBhJEAIdmABxhjZS8e7
[2]:http://pan.baidu.com/s/1A9IEB