# 小白黑果记录 

## 前言

我是**第一次**装机且**第一次**装黑苹果，**我只对我自己试验过的的机型，硬件，系统镜像以及使用的efi和装机工具有发言权，其他我不懂，勿扰**。对于教程和资源下文都可以获取。鼓励大家有能力要支持正版软件，一方面，任何成果都是工程师辛苦付出的结果；再者，请大家遵守相关法律法规，**本人玩这个黑果，只是个人娱乐，如有侵犯别人版权和商业利益，请告知本人，删除相关侵权的资源**！！！

## 本人需求

我作为小白用户只求装完机，安安静静地使用 MacOS 带来的便利性，装机越简单功能越完善越好，任何软件系统重要的是服务用户的使用，我也不会不断升级，系统稳定最重要。

![](https://camo.githubusercontent.com/da32bb12efddacc607d03813114a923400986a94/687474703a2f2f71396b7672616663712e626b742e636c6f7564646e2e636f6d2f736e61696c646f76652e6769746875622e696f2f6465736b6d696e693331302f6465736b6d696e693331302d6861636b6572732545372542452541342545342542412538432545372542422542342545372541302538312e706e67)![](deskmini-h310_黑果群.png)

## 硬件配置

| 项目类型  | 具体型号                       | 价钱（RMB）（3月份中旬购买） | 购买渠道 |
|:-------: | ------------------------------ | :---------: |--------- |
|   固态    | 海康威视 c2000 pro 1TB （没有一赔三，有的话麻烦请告知渠道，赔偿分你一些，嘻嘻）<br/>写入2.7G/s 读取3.1g/s——测速工具Mac版本DiskSpeedTest，没有持续压力测试（软件自带压力测试最多是5G），实测体验：3.0 U盘（读取速度100MB/s）拷贝28G多到这块盘，不到3分钟。 |     939     | 狗东 |
|   风扇    | 猫头鹰静音风扇NH-L9i（淘宝有卖家专门给风扇喷涂石墨烯，导热效果更好，本人没有试验过） |     300     | 狗东 |
| 无线网卡  | M2接口转接卡+苹果原装拆机卡BCM94360CS2 （免驱动） + 双天线 |     182     | 淘宝 |
|    CPU   | 8500 散片，拿到手开机电压 0.98v 不错 |  1356   | 熟人介绍狗东第三方卖家（略贵一点点） |
|   内存    | 威刚8g 2666Hz * 2              |     544     | 狗东（最贵的时候买入，肠子都悔青了，建议大家使用比价软件查看历史价格） |
|  显示器   | 便携 2k 显示器                 |     658     | 淘宝 |
| 机箱+主板 | deskmini 310                   |     979     | 狗东 |

自从疫情，全部涨价，我购买日期3月中旬，年前起码便宜六七百。小白第一次装机，没有旧配件和垃圾佬的水平，咸鱼也不碰，以后捡垃圾玩玩😆，不着急的小伙伴等6.18或者疫情过去又或者Intel新一代的CPU发布，到那时候价格比较香。我的黑苹果跑分如下，跟其他白苹果的对比：

![对比图，用梯子才能看到图](./Versus.jpg)

## 装机结果

### Bios版本 

目前我使用主板版本号是P4.2， 主板上有贴纸可以查看或者直接问你购买的店家的客服，也可以到官网下载更新到新版本。我买回来以后，一直没动它。

### 完成的功能

- Ethernet/WIFI/Bluetooth/Audio/USB&EX-USB/Sensors

- DP/HDMI dual monitor output

- Shutdown/Sleep

- AppStore/ICloudAirDrop/Handoff 

- VideoProc(仅供参考，Final Cut X Pro才是真正的验机工具): H264/HEVC/Hardware Decoder

    ![VideoProc，用梯子才能看到图](./VideoProc.png)

- 系统对风扇自动调速

- CPU 睿频
- HiDPI

    开启HiDPI以后，在偏好设置里面选择（我是便携超薄显示器 2k 72%NTSC约等于100%SRGB）：

    ![HiDPI-setting.jpeg，用梯子才能看到图](./HiDPI-setting.jpeg)

    下面第一张是开启HiDPI-720p，第二张1080p，第三张2k，对比一下观感:

    1. 开启HiDPI-720p

        ![开启HiDPI，用梯子才能看到图](./HiDPI.png)

    2. 1080p
    
        ![未开启HiDPI，用梯子才能看到图](./1080p-NotHiDPI.png)
    
    3. 2k
    
        ![未开启HiDPI-2K，用梯子才能看到图](./2K-NotHiDPI.jpeg)

### 未完成功能

1. VGA ：mac系统不支持vga！
2. **重点**，DP输出正常，然而HDMI视频输出的唤醒点不亮屏幕，很多15.4系统用户（尤其是用核显uhd630的用户）都反馈，只有当睡眠唤醒的时候，主机/鼠标/键盘等其他都正常，唯独HDMI视频接口输出的屏幕不亮，需要重新插拔一下HDMI输出接口的视频线或者对屏幕重新开关机，本人就不管了，但是有这个需求的用户需要注意。

## 装机过程

我这个小白根据这个 [视频教程](https://www.bilibili.com/video/BV1da4y147my) ：我按照视频教程操作到 13:11，因为我的m2型号的固态硬盘上只安装MacOS，所以我只进行到 13:11，**然后不要拔掉U盘**，将U盘里面的efi（注意不是winpe目录下的efi，而是跟winpe同一级目录的efi文件夹）替换掉装完机的MacOS系统的，这一步的目的是（通俗理解）：让新装的系统开机进入系统前引导的时候，需要这个efi文件夹下的内容去欺骗MacOS，让MacOS以为目前的的硬件就是白苹果对应的硬件，这样才能正常进入MacOS系统。下一步就是：https://blog.csdn.net/weixin_43912833/article/details/102408559 。

**注意**：装机和黑果有风险，注意重要的数据提前备份。

 ## 资源

#### 本机型相关资源

1. 目前我本人使用 **EFI** : https://github.com/cnsilvan/deskmini310_hackintosh 大佬的分享，然后进一步修改如下：

    - 电源选项
    - 开机跳过Clover选择系统界面，直接进入白苹果系统的的加载进度条，生活工作基本上不需要Windows，为了以防万一也已经装了Windows虚拟机。
    - 开启HiDPI

    我已经将我的 **EFI** 分享到本页面了。

2. 镜像使用的是：

    -  黑果小兵分享的 [10.15.4 19E287 双EFI 分区版](https://blog.daliansky.net/macOS-Catalina-10.15.4-19E266-Release-version-with-Clover-5107-original-image-Double-EFI-Version-UEFI-and-MBR.html#more) 

    - 下载镜像以后，注意校验下载的镜像有木有损坏，**必须校验**，不能跳过！

        黑果小兵的 `macOS Catalina 10.15.4(19E287) Installer for Clover 5109 and WEPE Support UEFI and MBR.dmg` 的MD5值为 `c84ebeeb84c074729c11afca91c6f952`


#### 黑苹果上手学习资源

1. [【知其然01】黑苹果CLOVER引导的目录构成及详解](https://www.bilibili.com/video/BV1BE411j7GE)
2. [【知其然02】黑苹果clover引导，如何配置属于自己的EFI？](https://www.bilibili.com/video/BV17E411p7hh/)
3. [【知其然03】那些黑苹果安装使用中常见的名词](https://www.bilibili.com/video/BV1Z7411n7fJ/?spm_id_from=333.788.videocard.1)
4. [【黑苹果】MacOS Catalina 10.15.4 详细安装过程实录(附有工具下载链接)](https://www.bilibili.com/video/BV1da4y147my)
5. [HiDPI是什么？以及黑苹果如何开启HiDPI](https://www.sqlsec.com/2018/09/hidpi.html)
6. [【AMD&intel】聪聪黑苹果安装工具3.0 零基础一键安装 全网最简单教程 兼容OpenCore及Clover EFI](https://www.bilibili.com/video/BV1iE41157Vd/?spm_id_from=333.788.videocard.5)

## 致谢

1. https://github.com/cnsilvan/deskmini310_hackintosh
2. https://github.com/zsyshuyang/Hackintosh-EFI-For-Deskmini-310-i5-9400-DW1560
3. https://github.com/liminghuang/asrock_deskmini310_hackintosh
4. https://github.com/yuqi/Deskmini-310-Hackintosh
5. https://github.com/isNextJuly/Hackintosh-EFI-for-deskmini-310-i7-8700
6. https://github.com/leogitpro/Hackintosh-DeskMini310

