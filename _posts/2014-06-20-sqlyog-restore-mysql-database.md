---
layout: post
title: "使用SQLyog恢复数据库时出现的问题"
tagline: "SQLyog Restore Mysql Database"
description: "使用SQLyog恢复数据库时出现的问题已经解决方法"
tags: [mysql,数据库]
---
{% include JB/setup %}

数据库在使用的过程中，经常需要备份恢复，以防出现数据丢失的情况。新系统采用mysql数据库，备份还原使用的是SQLyog。一直以来都没有出现过问题。

由于系统需要搬迁机房，因此需要在新机房服务器上恢复最新的数据库，恢复的过程中出现了问题，恢复失败。原因是随着系统在线上运行，数据库越来越大，备份文件的大小超出了mysql数据库max_allowed_packet的限制。

解决方法：
	
	--执行下面的语句，将max_allowed_packet设置为(文件大小*1024*1024  如:100M)
	set global max_allowed_packet=100*1024*1024;
	
**记得恢复完数据库之后将max_allowed_packet的值改回去，以免影响性能。**