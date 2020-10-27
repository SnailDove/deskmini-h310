## 前言

我是**第一次**装机且**第一次**装黑果，在大佬的帮助下已经近乎完美黑果，目前已经使用6个多月，并无问题，**我只对我自己试验过的的机型，硬件，系统镜像以及使用的efi和装机工具有发言权**。对于教程和资源下文都可以获取。鼓励大家有能力要支持正版软件，一方面，任何成果都是工程师辛苦付出的结果；再者，请大家遵守相关法律法规，**本人玩这个黑果，只是出于个人娱乐目的，如有侵犯别人知识版权和商业利益，请告知本人删除相关侵权的资源**！！！

### 版本迭代

本人的 **Clover EFI** 和 **OC EFI** : 适配以下系统版本（直接从15.4升级到15.5，再升级到15.6，15.7）

1. **Catalina 15.4** : 已经测试未发现问题

2. **Catalina 15.5、15.6、15.7 和 11.0 beta** : 双屏输出时，HDMI口解决方案如下
    
    - **验证可行方案1**：[祖传土方根治10.15.5正式版UHD630黑屏问题](http://bbs.pcbeta.com/viewthread-1859830-1-1.html)，感谢 @https://github.com/twotreeszf 的验证
    - **验证可行方案2**: 更新最新的 [Lilu.kext](https://github.com/acidanthera/Lilu/releases) 和 [Whatevergreen.kext](https://github.com/acidanthera/WhateverGreen/releases/tag/1.4.3)，感谢群友 @https://github.com/xiangsanliu 验证此方案的可行性！—— 2020.10.27记录


在原来硬盘上分区出来或者在另外一个硬盘上面可以随便升级和试验操作而且不会影响你当前正在使用的稳定MacOS版本，这样稳定和可玩性都具备（有时间折腾的朋友必备）：

1. [苹果官网：在单独的 APFS 宗卷上安装 macOS](https://support.apple.com/zh-cn/HT208891) 官网第一句话：通过 APFS，您可以更轻松地在不同版本的 macOS 之间切换，包括 Beta 版（预发布版）macOS。
2. [苹果官网：在 Mac 上的“磁盘工具”中将物理磁盘分区](https://support.apple.com/zh-cn/guide/disk-utility/dskutl14027/mac) 

彩蛋：[【司波图】10代最强带核显黑苹果装机实战及性能演示，附安装所需的注意事项](https://www.bilibili.com/video/BV17t4y1y7uu)

**重要提示**：建议大家到黑果小兵公众号下载多种引导集一身的镜像，这样子可以在 Linux grub，WinPE，OC，Clover引导中随意切换，可玩性和日后升级都比较方便。

## 装机结果

### Bios版本 

目前我使用主板版本号是P4.2， 主板上有贴纸可以查看或者直接问你购买的店家的客服，也可以到官网下载新版本。我买回来以后，一直没动它。

### 完成的功能

- Ethernet/WIFI/Bluetooth/Audio/USB&EX-USB/Sensors

- DP(4K 60Hz), HDMI(4k 30Hz) dual monitor output **两口开机睡眠均能唤醒不黑屏**

- Shutdown/Sleep

- IMessage/FaceTime/AppStore/ICloud/AirDrop/Handoff/**SideCar随航** 

- HWP enable: **按照自己的意愿设置CPU的最低、日常想要的频率、最高频率**

- VideoProc(仅供参考): H264/HEVC(即H265)/Hardware Decoder (**核显硬解已经测试通过：在视频转码时，通过Intel Power Gadget查看GPU频率，也可以使用Final Cut Pro X来验证**）

    ![VideoProc，用梯子才能看到图](./VideoProc.png)

- 系统对风扇自动调速

- CPU 睿频

- HiDPI——优化各个分辨率下的显示器显示效果

### 未完成的功能

1. VGA 口（最高只支持1080p，苹果系统用1080p太为难了）。有人在7代U上成功了：[VGA+HD630在10.15.4上成功驱动显卡](https://www.bilibili.com/video/BV12k4y1R7Ko)，也可以使自己使用Hackintool定制？可是原生机型并没有VGA口。
2. SD卡待测，没有SD卡，暂不需要，需要的请注意。

![deskmini-h310_黑果群，用梯子才能看到，主要是程序员，平常忙于工作，一般是休闲时间互相帮忙](./deskmini-h310_黑果群.png)

## 硬件配置

| 项目类型  | 具体型号                       | 价钱（RMB）（2020.3月份中旬购买） | 购买渠道 |
|:-------: | ------------------------------ | :---------: |--------- |
|   固态    | 海康威视 c2000 pro 1TB （没有一赔三，有的话麻烦请告知渠道，赔偿分你一些，嘻嘻）<br/>1. 写入2.7G/s 读取3.1g/s——测速工具Mac版本的DiskSpeedTest，没有持
