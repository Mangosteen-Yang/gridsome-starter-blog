---
title: 为什么在SAE写公众平台时session不好使？
date: 2013-08-31T05:48:00.000Z
tags:
  - PHP
description: 今天下午写抓取学生成绩代码时候，需要把$fromUsername从主文件传到另一个文件进行处理
---
考虑到有如下几种处理方法



1.利用POST或者GET传参，但考虑到还需要表格提交按钮，略繁杂，未尝试。



2.利用公共文件，可行，但同时多个用户同时访问时会发生冲突，自动生成销毁重命名文件又很繁琐，未尝试。



3.利用SESSION，最简单易行的方法，可是尝试了一下午值就是传不过去！考虑可能是因为创建SESSION的用户是腾讯微信的服务器，传递的时候是在SAE，最后取值也是给腾讯微信服务器。但做实验用本地给SAE一个SESSION，本地取是正常的，原因尚不清楚，期待高人解答。



4.利用数据库做中间层，流程同2，未尝试。



5.直接把第二个文件包含进主文件，曾一直觉得这个方法麻烦且容易冲突以及影响效率，最后无计可施尝试了一下这个方法，3分钟改完代码，完美运行！
