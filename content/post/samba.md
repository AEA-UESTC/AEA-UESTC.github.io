---
title: 'AEA Samba Tutorial'
subtitle: 'AEA Samba 网络驱动器使用指南'

date: 2025-04-22T15:40:00+08:00
lastmod: 2025-04-22T15:40:00+08:00

cover: "/covers/Samba.jpg"
categories: ["服务"]
tags: ["Samba", "网络驱动器", "科协资源"]
description: '本文介绍了如何连接到科协Samba服务器，映射网络驱动器，以及使用注意事项。Samba是一个用于连接UNIX和Windows操作系统的网络协议，提供了跨平台的文件共享功能。'
---

# AEA Samba Tutorial
## AEA Samba 网络驱动器使用指南
---

## 1. 什么是Samba？
> Samba，是種用來讓UNIX系列的作業系統與微軟Windows作業系統的SMB/CIFS（Server Message Block/Common Internet File System）網路協定做連結的自由軟體。第三版不僅可存取及分享SMB的資料夾及印表機，本身還可以整合入Windows Server的網域，扮演為網域控制站（Domain Controller）以及加入Active Directory成員。簡而言之，此軟體在Windows與UNIX系列操作系统之間搭起一座橋樑，讓兩者的資源可互通有無。 ——Wikipedia
> 一句话就是映射一个网络驱动器

## 2. 连接到科协Samba服务器
- 进入Windows资源管理器，在地址栏输入`\\192.168.1.4`；
- 然后，在弹出的验证对话框内，填入用户名与密码。用户名与密码请通过另一台可访问Samba的计算机打开Samba内密码存储xls查看。**若其他非科协成员有使用Samba资源的需求，请咨询对应理事并在使用时遵守相关规定。**；
- 然后，右键选择AEA_Samba目录，点击`映射网络驱动器`，即可将网络驱动器添加至此电脑；
- 最后，您可以重命名该驱动器为您喜欢的名字。

**注意事项：**
- 1. 如果密码更改，请使用`DosDeviceInspector.exe`，按照[这个博客的教程](https://xiwaer.com/647.html)，删除旧的映射信息，重新按照上述密码登录并连接。
- 2. 该账号拥有对目录的全部权限（777），因此，各位成员若要存储个人数据，请在根目录建立名为*你的名字+file*的文件夹。并**请注意一定不要随意删除其他人的文件！否则，等着线下真人快打吧(doge)**。

*AEA Network Maintaince Group*
*2022*