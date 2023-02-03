---
layout: post
title: TVBoxRouterArmArmbianOpenwrt
description: Amlogic设备等电视盒子的研究包括Arm架构的ArmbianOpenwrt等研究
date: 2023-01-02 15:43:01
---

## 常见的Amlogic设备

<hr/>

| 芯片  | 设备 | [可选内核](https://github.com/ophub/kernel/tree/main/pub/stable) | OpenWrt 固件 |
| ---- | ---- | ---- | ---- |
| a311d | [Khadas-VIM3](https://www.gearbest.com/boards---shields/pp_3008145189226460.html) | 全部 | *_a311d_k*.img |
| s922x | [Beelink-GT-King](https://tokopedia.link/RAgZmOM41db), [Beelink-GT-King-Pro](https://www.gearbest.com/tv-box/pp_3008857542462482.html), [Ugoos-AM6-Plus](https://www.gearbest.com/tv-box/pp_3002820788090799.html), [ODROID-N2](https://www.hardkernel.com/shop/odroid-n2-with-4gbyte-ram-2/) | 全部 | *_s922x_k*.img |
| s905x3 | [X96-Max+](https://www.gearbest.com/tv-box/pp_3001768790621051.html), [HK1-Box](https://tokopedia.link/xhWeQgTuwfb), [H96-Max-X3](https://tokopedia.link/KuWvwoYuwfb), [Ugoos-X3](https://github.com/ophub/amlogic-s9xxx-armbian/issues/782), [TX3](https://www.aliexpress.com/item/1005003772717802.html), [X96-Air](https://www.gearbest.com/tv-box/pp_3002885621272175.html), [X96-Max+_A100](https://github.com/ophub/amlogic-s9xxx-armbian/issues/779), [A95XF3-Air](https://tokopedia.link/ByBL45jdGgb), [Tencent-Aurora-3Pro(s905x3-b)](https://item.jd.com/100009131339.html), [X96-Max+Q1](https://github.com/ophub/amlogic-s9xxx-armbian/issues/788) | 全部 | *_s905x3_k*.img |
| s905x2 | [X96Max-4G](https://www.ebay.com/itm/164895650425), [X96Max-2G](https://www.alibaba.com/product-detail/Amlogic-S905X2-Android-TV-Box-X96_62210191636.html), [MECOOL-KM3-4G](https://www.gearbest.com/tv-box/pp_3008133484979616.html), [Tanix-Tx5-Max](https://github.com/ophub/amlogic-s9xxx-openwrt/issues/351), [A95X-F2](https://github.com/ophub/amlogic-s9xxx-armbian/issues/851) | 全部 | *_s905x2_k*.img |
| s912 | [Tanix-TX8-Max](https://www.tanix-box.com/project-view/tanix-tx8-max-android-tv-box/), [Tanix-TX9-Pro(3G)](https://github.com/ophub/amlogic-s9xxx-armbian/issues/315), [Tanix-TX9-Pro(2G)](https://github.com/ophub/amlogic-s9xxx-armbian/issues/740), [Tanix-TX92](http://www.tanix-box.com/project-view/tanix-tx92-android-tv-box-powered-amlogic-s912/), [Nexbox-A1](https://www.gearbest.com/tv-box-mini-pc/pp_424843.html), [Nexbox-A95X-A2](https://www.cafago.com/en/p-v2979eu-2g.html),  [A95X](https://tokopedia.link/zQVlmUfgqqb), [H96-Pro-Plus](https://www.gearbest.com/tv-box-mini-pc/pp_503486.html), [VORKE-Z6-Plus](http://www.vorke.com/project/vorke-z6-2/), [Mecool-M8S-PRO-L](https://www.gearbest.com/tv-box/pp_3005746210753315.html), [Vontar-X92](https://nl.aliexpress.com/i/32734559342.html), [T95Z-Plus](https://www.ebay.com/itm/253466003975), [Octopus-Planet](https://post.smzdm.com/p/a07oer59/), [Phicomm-T1](https://github.com/ophub/amlogic-s9xxx-armbian/issues/522) | 全部 | *_s912_k*.img |
| s905d | [MECOOL-KI-Pro](https://www.gearbest.com/tv-box-mini-pc/pp_629409.html), [Phicomm-N1](https://www.cnx-software.com/2019/03/11/phicomm-n1-tv-box-linux-distributions/) | 全部 | *_s905d_k*.img |
| s905x | [HG680P](https://tokopedia.link/HbrIbqQcGgb), [B860H](https://www.zte.com.cn/global/products/cocloud/201707261551/IP-STB/ZXV10-B860H), [TBee-Box](https://www.tbee.com/product/tbee-box/), [T95](https://www.gearbest.com/tv-box-mini-pc/pp_268277.html), [TX9](https://github.com/ophub/amlogic-s9xxx-armbian/issues/645), [Q96-mini(s905l-b)](https://github.com/ophub/amlogic-s9xxx-armbian/issues/734) | 全部 | *_s905x_k*.img |
| s905w | [X96-Mini](https://www.gearbest.com/tv-box/pp_3008306149708795.html), [TX3-Mini](https://www.gearbest.com/tv-box/pp_009748238474.html), [W95](https://www.gearbest.com/tv-box/pp_736121.html) | 5.4.y/5.15.y | *_s905w_k*.img |
| s905 | [Beelink-Mini-MX-2G](https://www.gearbest.com/tv-box-mini-pc/pp_321409.html), [Sunvell-T95M](https://github.com/ophub/amlogic-s9xxx-openwrt/issues/337), [MXQ-PRO+4K](https://www.gearbest.com/tv-box-mini-pc/pp_354313.html) | 全部 | *_s905_k*.img |
| s905l3a | [E900V22C/D](https://github.com/Calmact/e900v22c), [CM311-1a-YST](https://github.com/ophub/amlogic-s9xxx-armbian/issues/517), [M401A](https://github.com/ophub/amlogic-s9xxx-armbian/issues/732), [M411A](https://blog.csdn.net/fatiaozhang9527/article/details/126388479), [UNT403A](https://blog.csdn.net/wjf149575296/article/details/123947681), [UNT413A](https://blog.csdn.net/fatiaozhang9527/article/details/122232733), [ZTE-B863AV3.2-M](https://github.com/ophub/amlogic-s9xxx-armbian/issues/741) | 全部 | *_s905l3a_k*.img |
| s905l3b | [M302A/M304A](https://blog.csdn.net/fatiaozhang9527/article/details/122006745) | 全部 | *_s905l2_k*.img |
| s905l2/3 | [MGV2000](https://github.com/ophub/amlogic-s9xxx-armbian/issues/648), [Wojia-TV-IPBS9505](https://github.com/ophub/amlogic-s9xxx-armbian/issues/648), [CM311-1(s905l3)](https://github.com/ophub/amlogic-s9xxx-armbian/issues/763) | 全部 | *_s905l2_k*.img |
| rk3588 | [Radxa-Rock5B](https://wiki.radxa.com/Rock5/install), [HinLink-H88K](http://www.hinlink.com/index.php?id=151) | [rk3588](https://github.com/ophub/kernel/tree/main/pub/rk3588) | *_box-name.img |
| rk3568 | [R66S](https://r68s.cn/), [R68S](https://r68s.cn/), [e25](https://wiki.radxa.com/Rock3/CM/CM3I/E25), [h68k](http://www.hinlink.com/index.php?id=145) | [6.0.y](https://github.com/ophub/kernel/tree/main/pub/stable) | *_box-name.img |
| rk3328 | [beikeyun](https://www.cnblogs.com/milton/p/15391525.html), [l1pro](https://post.smzdm.com/p/a4wkdo7l/) | 全部 | *_box-name.img |
| allwinner | [vplus(h6)](https://www.allwinnertech.com/index.php?c=product&a=index&id=66) | 全部 | *_vplus_*.img |
| KVM | [qemu](https://github.com/unifreq/*_packit/blob/master/files/qemu-aarch64/qemu-aarch64-readme.md) | 全部 | *_qemu_*.img |

<hr/>


## 咪咕MGV3000研究

> 暫時沒有找到開啓ADB的方法

> https://www.znds.com/tv-1222451-1-1.html

> 江苏咪咕电视盒子刷机这个教程大家都比较需要，本次楼主带来了江苏咪咕MGV3000_YST代工_S905L3_线刷固件包，文中附固件下载链接，有需要的千万不要错过了。

### 刷机教程：

> 1、准备好一根双公头USB线刷刷机线，长度30-50CM长度最佳，同时准备一台电脑，拆开盒子；

> 2、电脑上安装好刷机工具Amlogic USB Burning Tool v2.1.6软件→打开软件→文件→导入烧录包→把【擦除flash】和【擦除bootloader】两项勾选→点击【开始】；

> 3、盒子接电源线→电源关闭→把USB线一端插上盒子→保持短接→USB另一端插上电脑→通电开机。

> 就可以看到进度条在跑了（此时松开短接），耐心等待进度条跑完；等待提示成功字样后，关闭电源，拔掉刷机线，把机顶盒接上电视机，通电开机，首次开机稍微会有点慢，耐心等待初始化完成即可。

> 江苏咪咕MGV3000_YST代工_S905L3_线刷固件包

### 固件下载链接：

> 链接: https://pan.baidu.com/s/104NHWG0t_33yjy3FCSg78Q 提取码:imuq

> MGV3000_CJZM_线刷.img.zip 已经转存

> https://www.znds.com/tv-1222182-1-1.html

> 其它固件大全 https://www.znds.com/tv-1181374-1-1.html

### DiskInitial命令出错 问题解决

> 方法1(无效)： 打开烧录软件；2、导入烧录包；3、去掉“擦除”两个对号，4、点击开始。5、机顶盒连接电源；6、机顶盒连接双公头USB；7、（最关键）立即使用牙签等按住机顶盒复位按钮（不同机顶盒复位按钮位置不一样，大多在AV孔内），中途不能松手，直至刷机完

> 方法2(未试)： 7%有个办法，就是 先打开软件，短接识别盒子，然后在选择刷机包，点开始，松开短接，有一定几率过7%

> 方法3(未试)： 刷YS（M）的包，可能之前的故件是错的


> 以下方法都未试：

```
第一种方法：先短接，再连数据线，让刷机软件能识别，，松开短接，选好固件，开刷。
第二种方法：先短接，再连数据线，让刷机软件能识别，，松开短接，选好固件，开刷。出现错误，再短接，拔出电脑端，usb线口再插上。电脑会显示刷机，就松开短接。

第三种方法：先短接，再连数据线，让刷机软件能识别，，不松开短接，选好固件，开刷。
第四种方法：先短接，再连数据线，让刷机软件能识别，，不松开短接，选好固件，开刷。出现错误，拔出电脑端，usb线口再插上。电脑会显示刷机，就松开短接。
```


### hdmi短接器厂家给的意见

刷机百分几错程原因1
首先说明：连接成功后，刷机时出现的错程和短接没任何关系
1：固件不对应型号或对应代工厂版本
2：刷机软件版本不对应，28NM S905用2.2之前版本，12NM S905L3A用2.2版本，不要使用过老或过新版本
3：刷机线不是USB2.0多股铜也会不识别，刷机线不能用USB3.0。3.0都会弱化2.0，也不能使用过长的线，线过长会不稳定

刷机百分几错程原因2
4：主机使用前面的USB口因为供电不足，要使用后面USB口，有USB2.0就尽量使用2.0，没有就用原生3.0，非原生3.0也不稳定
5: 盒子一定要接电源，不接电源能识别，但刷写过程容易出错误

## 咪咕MGV3200研究 GK6323芯片

### 目前已测试 完整的破解模式 无需刷机

#### 在MGV3200上启用ADB 或者叫USB调试

> 接USB键盘鼠标，等到机顶盒启动后连续F2 F3交替按 很快就会进入安卓本上的launcher 典籍打开全部应用 可以看到一个 AdbConsole。进去后点击打开既可。

> 或者MGV3200自带的两个设置程序里边也有，可以进去找找，具体记得不清了。


#### 使用 ADB 卸载和安装程序，adb程序自己在网上下载，非常多。

##### ADB链接，MGV3200连网线的情况下，去路由器找到机顶盒的IP 比如我的是192.168.0.174

> 首先 执行 cd命令进入你的adb.exe所在的目录下。

> 那么连接就是 adb connect 192.168.0.174 正常链接后会有提示：connected to 192.168.0.174:5555，这时候就可以进行卸载了。

```
C:\ADB>adb connect 192.168.0.174
```

##### 我的卸载列表如下（可以执行 adb shell pm list packages查看当前系统中有哪些程序），照着一行一行执行既可，有些可能你的机子不一定有：

```
adb shell pm uninstall -k --user 0 com.cmcc.dlna
adb shell pm uninstall -k --user 0 package:com.cmcc.mid.softdetector
adb shell pm uninstall -k --user 0 com.yst.whitebox
adb shell pm uninstall -k --user 0 com.chinamobile.middleware.auth
adb shell pm uninstall -k --user 0 com.huawei.oot.order
adb shell pm uninstall -k --user 0 com.istv.appstore
adb shell pm uninstall -k --user 0 com.android.chinamobile.zj.ott.adpro
adb shell pm uninstall -k --user 0 com.um.tvlauncher
adb shell pm uninstall -k --user 0 com.cmcc.mid.softdetector
adb shell pm uninstall -k --user 0 com.homecdn.pservice
adb shell pm uninstall -k --user 0 com.komect.video.plive
adb shell pm uninstall -k --user 0 com.huawei.iptv.myapp
adb shell pm uninstall -k --user 0 com.um.tvlauncher
```

> 卸载成功后均有 Success 的提示消息

##### 安装程序，讲apk安装包提前下载好放到adb目录下，然后执行类似下列的命令，apk名称替换为你的：

```
C:\ADB>adb install dangbeimarket_4.4.0_288_znds.apk
C:\ADB>adb shell install dbzm_4.1.6_dangbei.apk
C:\ADB>adb sinstall dbzm_4.1.6_dangbei.apk
C:\ADB>adb install dbzm_4.1.6_dangbei.apk
```
> 安装成功后均有 Success 的提示消息

#### ADB的配置 查看IP，首先在系统中进入adb shell ping ip地址是可以的，但是ping域名不通，显然是运营商动了手脚，这时候我们就需要破解dns，也是很简单的

> 这时候需要以root执行 因此需要执行 adb root，正常情况下返回空行: 

```
C:\ADB>adb root
```

然后进入shell 模式

```
C:\ADB>adb shell
```

> 这时候如果你的机器显示 GK6323V100C:/ # 那说明你已经以root方式进入了shell。这时候我们执行getprop |grep dns 会得到以下输出：

```
GK6323V100C:/ # getprop |grep dns
[dhclient.eth0.dns1]: [fdad:ca6e:cd0b::1]
[net.dns1]: [2409:8028:2000::2222]
[net.dns2]: [2409:8028:2000::1111]
[net.dns3]: [211.140.13.188]
[net.dns4]: [211.140.188.188]
```

> 很显然net.dns3 和net.dns4 被运营商绑定成他们自己了，比如我这个是移动，我联通的宽带自然就不行了。因此我需要修改 net.dns3 net.dns4 ,命令如下：

```
GK6323V100C:/ # setprop net.dns3 192.168.0.1
GK6323V100C:/ # setprop net.dns4 8.8.8.8
```

> 正常也不会有提示 ，这时候我们Ping一个域名发现就可以ping通了。

```
GK6323V100C:/ # ping www.baidu.com
PING www.a.shifen.com (110.242.68.4) 56(84) bytes of data.
64 bytes from 110.242.68.4: icmp_seq=1 ttl=53 time=26.2 ms
64 bytes from 110.242.68.4: icmp_seq=2 ttl=53 time=26.3 ms
64 bytes from 110.242.68.4: icmp_seq=3 ttl=53 time=26.0 ms
64 bytes from 110.242.68.4: icmp_seq=4 ttl=53 time=26.0 ms
64 bytes from 110.242.68.4: icmp_seq=5 ttl=53 time=26.1 ms
64 bytes from 110.242.68.4: icmp_seq=6 ttl=53 time=25.9 ms
64 bytes from 110.242.68.4: icmp_seq=7 ttl=53 time=26.1 ms
64 bytes from 110.242.68.4: icmp_seq=8 ttl=53 time=26.1 ms
^C
--- www.a.shifen.com ping statistics ---
8 packets transmitted, 8 received, 0% packet loss, time 7008ms
rtt min/avg/max/mdev = 25.922/26.125/26.316/0.118 ms
```

> 然后执行reboot重启机顶盒：

```
127|GK6323V100C:/ # reboot
```

> 过一阵去看你的机顶盒已经可以正常上网，里边的各种app网络访问也正常了，这时候你的机顶盒已经成全网通的了。

> 当然这时候你得手动设置默认桌面，在系统 应用管理中 找到默认应用  进去设置默认启动器既可。

#### 注意，这种方式如果你还原了系统，那么就得重新再这么配置一次了，不过你要熟悉了整个过程也是很简单。

### ADB 卡刷


### 可以卡刷 403G 固件九联unt403G机顶盒6323处理器刷机教程；

九联unt403G机顶盒6323处理器刷机教程；

下载固件之前请先确认您的盒子是否能正常打开adb功能；

打开方法：点此查看；能正常打开就接着往下看，打不开的

请联系本站的在线客服求助；

优盘1个别大于8G最佳，将其格式化为fat32格式备好；

如您没合适的优盘可点此处到麒麟商城下单1个专用优盘；

点此下载专用解压工具安装至电脑；

刷机固件：请点击最上面的固件下载按钮获取固件并下载解压备好；

将机顶盒的网线插到路由器上，不要插到猫的iptv口；

将固件内update.zip、YueMe_BOX文件夹一同拷贝到U盘根目录；

然后电脑上运行固件包里的***rec.exe程序，见下图

adb.jpg

然后输入机顶盒网络里的ip地址 然后回车键

（可根据程序内的提示进行操作）；

然后将复制号文件的U盘插机顶盒，盒子会自动复制文件并刷机；
刷机完成后盒子会自动重启，优化系统程序完成启动到主界面会自动安装应用市场，
自己手上有什么好用的电视app可以放在优盘的YueMe_BOX文件夹
插入优盘开机后系统会自动帮你安装好；


### 通过ADB修改DNS

> adb connect 192.168.0.222

> adb root

>  有时候会输出restarting adbd as rooting

> adb root 有时会输出 restarting adbd as root，有的时候什么也没有提示，这个时候通过adb shell进入shell命令行，查看命令提示符是否变成#

> 有些设备root后也无法通过adb root命令让adbd以root权限执行，adb root会输出adbd cannot run as root in production builds，此时可以先安装adbd insecure，然后再尝试

添加DNS服务器地址到盒子里，杭州电信的DNS是202.101.172.35
202.101.172.46
202.101.172.47
所在地的dns服务器地址自己查询
10.0.0.139是我路由器的IP地址
查看DNS服务器的命令是 adb shell 后
输入 getprop |grep dns
修改DNS服务器的命令是
setprop
例如：setprop net.dns3 xx.xx.xx.xx
最后修改成下面的地址就行。没改动的地址可以保留我就添加了3条，2条是电信的DNS，一条是路由器IP地址

> 恢复adbd为非root权限 命令：adb unroot


>  可以参考：https://www.yisu.com/zixun/203183.html


## Root android 9

Root Android 9.0 (Pie) Device in 2021 – A Step by Step guide
Hello guys, how you all doing? Bought a new android phone and that too has the latest Pie version? I know that you can’t live without rooting your phone and gaining superuser access to it.

And since rooting Android Pie is a tough task so we have come up with some tricks to root Android 9.0 Pie. Yes in this article we will tell you 3 ways to root Android Pie 9.0 using SuperSU, Magisk, and Kingo Root easily in 2021.

Contents  hide 
1 Root Android 9.0 (Pie) Device in 2021 – A Step by Step guide
2 Root Android 9.0 via Magisk
2.1 Root Android 9.0 via Magisk Manager
3 Root Android 9.0 via SuperSU
4 Root Android 9.0 via KingoRoot
4.1 Root Android 9.0 via KingoRoot Android App
4.2 Root Android 9.0 via KingoRoot Windows Application
Must Read: How to Root any Android 10 Q Device in 2021 the Easy Way?

### Root Android 9.0 via Magisk

Magisk was introduced as an alternative to SuperSU root, which was the only rooting solution at that time. SuperSU modifies system files to provide root access to Android devices. Magisk made rooting easy with systemless root. It roots the system without modifying the core code. It is a godsend for people using Financial apps on their Android device. Magisk is the latest method to root android 9 devices. It can be done through two different ways

root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way


### Root Android 9.0 via Magisk Manager
First of all, download the Magisk Manager and place it in your phone’s storage. 
Download Magisk Manager
Now you have to boot your device into a custom recovery like the TWRP Recovery. If you haven’t installed one then search on Google or Youtube for proper instruction on how to install a custom recovery for your Android 9 Device.
Click on the Install button and then select the Magisk.zip file that you had already transferred to your device storage in Step 1.
Root Android 9
Root any Android 10 Device with Magisk
After you had selected the .zip file now Swipe to Confirm Flash on the bottom side of your mobile screen to start the flashing process.
Root any Android 10 Device with Magisk
Once Magisk is flashed, you’ll get the Reboot System option, select it.
After the device reboots, open a file manager application and then go to the folder where you transferred the Magisk Manager Apk file in Step 1. Install it.
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
Open the Magisk Manager app and check your device’s root status. That’s All.
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way


### Root Android 9.0 via SuperSU

root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
First of all download the SuperSU zip file from the link given below.
Download SuperSU
Now you have to boot your device into a custom recovery like the TWRP Recovery. If you haven’t installed one then search on Google or Youtube for proper instruction on how to install a custom recovery.
Now from the Recovery Menu click on Install and select the zip file SuperSU that you have downloaded from in Step 1.
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
After you have selected the SuperSU .zip file, Swipe to Confirm Flash on the bottom of the screen to start the flashing process.
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
After the SuperSU is flashed in your device you will get Reboot System and Wipe cache/Dalvik. Click on Wipe cache/Dalvik and then on Reboot System. On the Next Reboot, you will have full root access.
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way


### Root Android 9.0 via KingoRoot


#### Root Android 9.0 via KingoRoot Android App


Step 1. Download the KingoRoot Apk file from the button given below:

Download Kingo Root Apk
Step 2. Locate the downloaded file on your Android 10 smartphone and install the apk.

Step 3. If you get “Install Blocked” message, follow these few steps:

Open Settings.
Go to Security and then to Unknown sources and enable it.
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way


Step 4. Open the app and tap on “One Click Root”.

root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way

Step 5. The result will be displayed as “Success” or “Failure”.

Step 6. If it fails, try the process again a few number of times.

#### Root Android 9.0 via KingoRoot Windows Application

Step 1. Download the KingoRoot PC Software from the button below:

Download KingoRoot PC Software
root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
Step 2. Install the KingoRoot PC Software downloaded above. After the installation is complete, launch the app.



Step 3. Connect your Android device to your PC. Make sure to enable the USB Debugging on your Android device.

root android 9, How to Root Any Android 9.0 Device &#8211; The Right Way
Step 4. Click on “Root” to begin the rooting process.

Step 5. The result of root will be displayed when the process is complete.

Root Android 9
You can check the status of the root on your Android device. The root status should display as rooted. Check for root by downloading any root checking app from the play store.This way you can root any android 10 device


## 网心云 OneCloud 研究Openwrt研究

### 目前概述

> 目前网上的教程openwrt 18 可以顺利刷入 emmc 但是版本太老

<hr/>

###  未测试的方法

OneCloud eMMC installation script
This repository helps you with the installation of the latest Armbian image to the eMMC partition of a Xunlei OneCloud device. Tested with OneCloud hardware version v1.0.

How to use
Before you start, please make sure you have met all the following requirements:

You have installed aml_burn_tool and know how to use it.
You have flashed s805_flash_snail.img to your OneCloud device. You may download from here (PW：2091).
You have a usb2ttl converter and can get the tty output work via Putty.
Pre-steps before Image Compilation
Thanks to hzyitc, the official repository of armbian has now add support for OneCloud (see this link). You may now build the official image for OneCloud.

To make the image boot, several modifications are needed (see here):

Add boot-onecloud.cmd script at /<armbian_src>/config/bootscripts/boot-onecloud.cmd;
Modify meson_common.inc at /<armbian_src>/config/sources/families/include/meson_common.inc;
Add onecloud.txt at /<armbian_src>/config/bootenv/onecloud.txt;
Post-steps after Image Compilation
After the modification, build the image and burn the image to a USB stick with your preferred tool (e.g. rufus).

Insert the USB stick to your PC and mount the boot partition, and copy the whole folder to the boot partition. Then your file tree should look like:

|--install
|  |--mkfs
|  |  |--mkfs.fat
|  |  |--mkfs.msdoc
|  |  |--mkfs.vfat
|  |--install.sh
|  |--...
|--armbianEnv.txt
|--boot.cmd
|--boot.scr
|--...
Now your USB stick should be ready to go.

Prepare your bootloader
If you have flashed s805_flash_snail.img, then your u-boot will try to boot by locating s805_autoscript from any connected device (usb/mmc).

You may check the u-boot scripts with the following steps:

Jump into the u-boot by hitting enter after plugging the power cable.
Type print in the u-boot console.
Type the following lines one by one to make the u-boot adapt to the new boot format (lines that start with # are comments and should be ignored):

 setenv bootfromrecovery 0
 setenv bootfromnand 0

 # set a script called start_mmc_autoscript, which tries to load boot.scr from mmc 0 first, if failed, then from mmc 1
 setenv start_mmc_autoscript 'if fatload mmc 0 11000000 boot.scr; then autoscr 11000000; fi; if fatload mmc 1 11000000 boot.scr; then autoscr 11000000; fi;'

 # set a script called start_usb_autoscript, which tries to load boot.scr from usb 0 first, if failed, then from usb 1
 setenv start_usb_autoscript "if fatload usb 0 11000000 boot.scr; then autoscr 11000000; fi; if fatload usb 1 11000000 boot.scr; then autoscr 11000000; fi;"
 
 # set a script called start_autoscript, which checks if any usb device is connected. If so, call start_usb_autoscript; otherwise, call start_mmc_autoscript
 setenv start_autoscript 'if usb start; then run start_usb_autoscript; fi; if mmcinfo 1; then run start_mmc_autoscript; fi;'

 setenv bootcmd 'run start_autoscript; run storeboot'
 setenv firstboot 1

 saveenv
Now your u-boot should be ready to go. Insert your USB stick to the OneCloud and type reset to restart. Your device should be able to boot from the USB stick. After logging, navigate to /boot/install, and run

./install.sh
You will be notified to restart when finished.

Unplug your USB stick and restart the system. Now the OS has been installed to your eMMC. Enjoy!


## 魔百盒M401a玩转Coreelec

### 下载写镜像改dub.img

### U盘启动

> adb reboot update 后瞬间插入u盘

### 写入emmc

> 打开系统 ssh 功能，电脑 ssh 连接后同样使用 ceemmc -x 命令，然后按喜好设置既可 默认密码 root coreelec

### 使用docket加载天翼网盘 阿里云盘

#### 安装docker 

```
输入 docker info 确认有正常运行

输入 docker pull cloudnas/clouddrive  拉取安装文件
```

#### 设置SMB共享

```
CE设置-服务-改为SMB1

/storage/.config/samba.conf，增加以下：

[CloudDrive]

  path = /storage/Clouddrive/CloudDrive/

  available = yes

  browseable = yes

  public = yes

  writeable = yes

```

#### CoreELEC的缓存设置

> /storage/.kodi/userdata/Advancedsettings.xml 文件内容如下，2G内存的设备可以设置300M缓存

```
<advancedsettings>
  <cache>
    <buffermode>1</buffermode>
    <memorysize>314572800</memorysize>
    <readfactor>25</readfactor>
  </cache>
</advancedsettings>
```

#### 启动 clouddrive

```
docker run -d \
--name clouddrive \
--restart unless-stopped \
-v /storage/Clouddrive:/CloudNAS:shared \
-v /storage/Clouddrive/Config:/Config \
--network host \
--pid host \
--privileged \
--device /dev/fuse:/dev/fuse \
cloudnas/clouddrive

然后就可以通过 Ip 9798端口访问 例如我的就是
http://192.168.0.179:9798/

docker rm 9cd7796a669d054f3634e8ac8427508b5e48c32094923034c3d9c0c1045246f1

docker rm  "/clouddrive"

docker  rm $(docker ps -a -q)
```

### 蓝牙遥控


#### mbh文件

```
# table mbh, type: NEC
0x22dc KEY_POWER #电源
0x22ca KEY_UP #向上
0x2299 KEY_LEFT #向左
0x22c1 KEY_RIGHT #向右
0x22d2 KEY_DOWN #向下
0x2292 KEY_1
0x2293 KEY_2
0x22cc KEY_3
0x228e KEY_4
0x228f KEY_5
0x22c8 KEY_6
0x228a KEY_7
0x228d KEY_8
0x22c4 KEY_9
0x2287 KEY_0
0x22f0 KEY_DOT #M键/点号
0x22d0 KEY_BACKSPACE #删除
0x2288 KEY_HOME #主页
0x2282 KEY_CONTEXT_MENU #菜单
0x22ce KEY_ENTER #选中/确定
0x2295 KEY_ESC #返回
0x228d KEY_CONFIG #设置
0x22da KEY_STOP #按键区的电源键
0x2281 KEY_VOLUMEDOWN #音量-
0x2280 KEY_VOLUMEUP #音量+
0x229c KEY_MUTE #静音
0x2285 KEY_PLAYPAUSE #播放停止按键区的TV/AV键
```
#### rc_maps_cfg文件添加行

···
meson-ir	*		mbh
···

### 蓝牙遥控确认键问题


```
I: Bus=0005 Vendor=0416 Product=0300 Version=0505
N: Name="CMCC_Voice_Remote"
P: Phys=12:00:00:a8:e5:10
S: Sysfs=/devices/virtual/misc/uhid/0005:0416:0300.0003/input/input7
U: Uniq=0c:f3:cc:31:2d:e9
H: Handlers=sysrq kbd leds mouse1 event6
B: PROP=0
B: EV=12001f
B: KEY=3007f 0 0 0 0 483ffff 17aff32d bf544446 0 0 70001 130ff3 8b17c007 ffff7bfa d9415fff febeffdf ffefffff ffffffff fffffffe
B: REL=143
B: ABS=1 0
B: MSC=10
B: LED=1f
```

```
systemctl stop kodi
systemctl stop eventlircd
evtest /dev/input/event6(需要安装 system tools 插件)


Event: time 1673748252.082007, type 20 (EV_REP), code 0 (REP_DELAY), value 500
Event: time 1673748252.082007, type 4 (EV_MSC), code 4 (MSC_SCAN), value 70066
Event: time 1673748252.082007, type 1 (EV_KEY), code 116 (KEY_POWER), value 1
Event: time 1673748252.082007, -------------- SYN_REPORT ------------
Event: time 1673748252.281985, type 4 (EV_MSC), code 4 (MSC_SCAN), value 70066
Event: time 1673748252.281985, type 1 (EV_KEY), code 116 (KEY_POWER), value 0
Event: time 1673748252.281985, -------------- SYN_REPORT ------------
Event: time 1673748307.050762, type 4 (EV_MSC), code 4 (MSC_SCAN), value c0041
Event: time 1673748307.050762, type 1 (EV_KEY), code 353 (KEY_SELECT), value 1
Event: time 1673748307.050762, -------------- SYN_REPORT ------------
Event: time 1673748307.250770, type 4 (EV_MSC), code 4 (MSC_SCAN), value c0041
Event: time 1673748307.250770, type 1 (EV_KEY), code 353 (KEY_SELECT), value 0
Event: time 1673748307.250770, -------------- SYN_REPORT ------------



开关机 70066
确定 C0041

/etc/udev/hwdb.d/*..hwdb

evdev:input:b0005v0416p0300*
 KEYBOARD_KEY_c0041=enter
 KEYBOARD_KEY_70066=sleep
 
 
配置生效

重启服务

systemd-hwdb update

udevadm trigger

systemctl start eventlircd

systemctl start kodi

输入确定按键生效命令：

udevadm info /dev/input/event4 | grep KEYBOARD_KEY 

```

#### https://discourse.coreelec.org/t/alfawise-z1-bluetooth-remote-configuration/2955

I have an Alfawise Z1 (2/16) and there was a problem under CE, the BT remote OK button cant working only when i switch to mouse mode. With this little mod i able to use as expected.

First, create /etc/udev/hwdb.d/10-btok.hwdb file and fill with:

_evdev:input:b0005v2B54p1603e*_
_KEYBOARD_KEY_c0041=enter_
Save, reinitialize hwdb and reboot system:

_systemd-hwdb update_
_reboot_
The remote controller use the following codes:

Mute c00e2
Menu 70065
Ok c0041
Up c0042
Down c0043
Left c0044
Right c0045
Home c0223
Back c0224
Mic c0221
Vol+ c00e9
Vol- c00ea
Prev c00b4
Next c00b3

Mouse mode
Ok 90001


### 蓝牙重启后失效

> udevadm info /sys/bus/sdio/devices/sdio* | paste

#### reinstalled both TVheadend and all OK

> killall -9 hciattach

> /usr/bin/hciattach -n -s 115200 /dev/ttyS1 bcm43xx 2000000

> systemctl unmask brcmfmac_sdio-firmware-aml


> echo "ln -s /usr/lib/kernel-overlays/base/lib/firmware/brcm/BCM4335_V0343.0353.hcd /var/lib/firmware/brcm/BCM4335AO.hcd" >> /storage/.config/autostart.sh

> reboot

> There is no reason your device should not be working as the firmware is there.Revert the previous command with the following.

```
systemctl unmask brcmfmac_sdio-firmware-aml
reboot
```

> When your device comes back up paste the output of hciconfig -a.


Hi @Newoski, I had the same problem with a Harmony Hub before and used this:

#### https://discourse.coreelec.org/t/odroid-n2-bluetooth-wont-auto-reconnect-after-reboot/7702/3

> \# /storage/.config/system.d/harmony.service
[Unit]
Description=Connect to Harmony on BT on startup and resume
After=suspend.target bluetooth.service

[Service]
Type=oneshot
ExecStart=/usr/bin/sh -c "for i in 1 2 3 4 5; do if bluetoothctl connect 00:04:20:F4:F1:22; then exit; else if [ $i -eq 5 ]; then exit $?; else sleep 5; fi; fi; done"
TimeoutSec=0

[Install]
WantedBy=multi-user.target sleep.target
But it seems to do be doing fine without it for a while now (I’m at 9.2.0 on a generic S905X2 box with an external BT dongle).


Created /storage/.config/system.d/harmony.service
then
chmod a+x /storage/.config/system.d/harmony.service
then
Added contents you shared with my bluetooth address

Is that right? Which dongle are you using? Do you know a model?


Saviq
Nov '19
chmod a+x /storage/.config/system.d/harmony.service

FWIW this was wrong, the right way to enable the systemd service is using systemctl:

systemctl enable harmony.service


Hi I know it’s an old thread but I have the same issue.
I have an Odroid N2 with the generic Bluetooth dongle sold by Ameridroid and Harmony hub.
I lost connection on reboot (Mac address change ?)

I try Saviq solution with no success

All idea are welcome


#### See below

> https://discourse.coreelec.org/t/solved-bluetooth-not-working/6983/72?filter=summary


### 蓝牙遥控启动

> 暂无解决

### 直播源配置

> 安装PVR IPTV Simple Client 插件
> 网上下载m3u8配置文件并导入
> 目前直播普遍比较卡顿 待优化



## M401a刷Armbian进Emmc

### 下载Armbian S905L3a镜像

> s905L3a 处理器的机器无需做任何修改，写入U盘后就可以启动

### U盘启动

> adb reboot update 后瞬间插入u盘

### SSH连接系统并执行重启

```
login as: root
root@192.168.0.229's password:
    _              _        ___   ___  ____  _ _____
   / \   _ __ ___ | |  ___ / _ \ / _ \| ___|| |___ /  __ _
  / _ \ | '_ ` _ \| | / __| (_) | | | |___ \| | |_ \ / _` |
 / ___ \| | | | | | | \__ \\__, | |_| |___) | |___) | (_| |
/_/   \_\_| |_| |_|_| |___/  /_/ \___/|____/|_|____/ \__,_|

Welcome to Armbian 23.02.0-trunk Jammy with Linux 6.1.6-happy-new-year

System load:   172%             Up time:       11 min
Memory usage:  10% of 1.90G     IP:            192.168.0.230
192.168.0.229
CPU temp:      41°C             Usage of /:    82% of 2.4G
storage/:      57% of 252M

Last login: Mon Jan 16 13:18:04 2023 from 192.168.0.1
```

> 运行armbian-install执行写入emmc操作

```
root@armbian:~# armbian-install
[ STEPS ] Start install armbian to emmc...
[ INFO ] Custom setting parameters: [  ]
[ STEPS ] Start initializing the environment...
[ INFO ] Use mainline u-boot: [ no ]
[ INFO ] Using the Ampart tool: [ yes ]
[ INFO ] Show all lists: [ no ]
[ INFO ] The device eMMC name: [ /dev/mmcblk2 ]
[ STEPS ] Start selecting device...
--------------------------------------------------------------------------------------
ID    SOC        MODEL                          DTB                             
--------------------------------------------------------------------------------------
301   s905x2     X96-Max-4GB/Tx5-Max            meson-g12a-x96-max.dtb          
302   s905x2     X96-Max-2GB/A95X-F2            meson-g12a-x96-max-rmii.dtb     
303   s905x2     MECOOL-KM3-4G                  meson-g12a-sei510.dtb           
304   s905l3a    E900V22C-D                     meson-g12a-s905l3a-e900v22c.dtb 
305   s905l3a    CM311-1a-YST                   meson-g12a-s905l3a-cm311.dtb    
306   s905l3a    M401A/ZTE-B863AV3.2-M          meson-g12a-s905l3a-m401a.dtb    
0     Other      Customize                      Enter-custom-dtb-name           
--------------------------------------------------------------------------------------
```

> 输入306，其他设备请按实际型号来既可

```
[ OPTIONS ] Please Input ID: 306
[ INFO ] Input Box ID: [ 306 ]
[ INFO ] FDTFILE: [ meson-g12a-s905l3a-m401a.dtb ]
[ INFO ] MAINLINE_UBOOT: [  ]
[ INFO ] BOOTLOADER_IMG:  [  ]
[ INFO ] UBOOT_OVERLOAD: [ u-boot-e900v22c.bin ]
[ INFO ] K510: [ 1 ]
[ STEPS ] Start selecting file system type...
-----------------------------------------------
ID  TYPE
-----------------------------------------------
1   ext4
2   btrfs
-----------------------------------------------
```

> 输入1，分区选择 ext4 然后就是漫长的耐心等待

```
[ OPTIONS ] Please Input ID: 1
[ INFO ] Input Type ID: [ 1 ]
[ INFO ] The type of file system: [ ext4 ]
[ STEPS ] Start creating eMMC partition...
[ INFO ] Start backup default bootloader.
4+0 records in
4+0 records out
4194304 bytes (4.2 MB, 4.0 MiB) copied, 10.8834 s, 385 kB/s
1+0 records in
1+0 records out
512 bytes copied, 0.0023275 s, 220 kB/s
[ STEPS ] Use ampart partition successfully.
[ INFO ] Start create MBR and partittion.
[ INFO ] Restore the mybox bootloader: [ /usr/lib/u-boot/mybox-bootloader.img ]
444+0 records in
444+0 records out
444 bytes copied, 0.0156965 s, 28.3 kB/s
8191+0 records in
8191+0 records out
4193792 bytes (4.2 MB, 4.0 MiB) copied, 0.606319 s, 6.9 MB/s
[ STEPS ] Start processing the bootfs partition...
[ INFO ] Formatting BOOTFS partition.
mkfs.fat 4.2 (2021-01-31)
[ INFO ] Start copy BOOTFS partition data.
[ INFO ] Generate the new [ uEnv.txt ] file.
[ INFO ] Copy [ u-boot-e900v22c.bin ] to u-boot.emmc
[ STEPS ] Start processing the rootfs partition...
[ INFO ] Formatting ROOTFS partition.
[ INFO ] Start copy ROOTFS partition data.
[ INFO ] Copy the [ etc ] directory.
tar: etc: file changed as we read it
[ INFO ] Copy the [ home ] directory.
[ INFO ] Copy the [ lib64 ] directory.
[ INFO ] Copy the [ opt ] directory.
[ INFO ] Copy the [ root ] directory.
[ INFO ] Copy the [ selinux ] directory.
[ INFO ] Copy the [ srv ] directory.
[ INFO ] Copy the [ usr ] directory.
```

> 上面这个是因为使用了不合格优盘 拷贝到 usr之后就异常了，后边又换了个好u盘 执行OK 结果如下：

```
[ OPTIONS ] Please Input ID: 1
[ INFO ] Input Type ID: [ 1 ]
[ INFO ] The type of file system: [ ext4 ]
[ STEPS ] Start creating eMMC partition...
[ INFO ] Start backup default bootloader.
4+0 records in
4+0 records out
4194304 bytes (4.2 MB, 4.0 MiB) copied, 0.829114 s, 5.1 MB/s
1+0 records in
1+0 records out
512 bytes copied, 0.00125406 s, 408 kB/s
[ STEPS ] Use ampart partition successfully.
[ INFO ] Start create MBR and partittion.
[ INFO ] Restore the mybox bootloader: [ /usr/lib/u-boot/mybox-bootloader.img ]
444+0 records in
444+0 records out
444 bytes copied, 0.0160725 s, 27.6 kB/s
8191+0 records in
8191+0 records out
4193792 bytes (4.2 MB, 4.0 MiB) copied, 0.535158 s, 7.8 MB/s
[ STEPS ] Start processing the bootfs partition...
[ INFO ] Formatting BOOTFS partition.
mkfs.fat 4.2 (2021-01-31)
[ INFO ] Start copy BOOTFS partition data.
[ INFO ] Generate the new [ uEnv.txt ] file.
[ INFO ] Copy [ u-boot-e900v22c.bin ] to u-boot.emmc
[ STEPS ] Start processing the rootfs partition...
[ INFO ] Formatting ROOTFS partition.
[ INFO ] Start copy ROOTFS partition data.
[ INFO ] Copy the [ etc ] directory.
[ INFO ] Copy the [ home ] directory.
[ INFO ] Copy the [ lib64 ] directory.
[ INFO ] Copy the [ opt ] directory.
[ INFO ] Copy the [ root ] directory.
[ INFO ] Copy the [ selinux ] directory.
[ INFO ] Copy the [ srv ] directory.
[ INFO ] Copy the [ usr ] directory.
[ INFO ] Copy the [ var ] directory.
[ INFO ] Generate the new fstab file.
[ INFO ] Update the relevant parameters.
[ SUCCESS ] Successful installed, please unplug the USB, re-insert the power supply to start the armbian.
```

> 很明显后边又[ SUCCESS ] 成功的标记，这时候执行poweroff 关机后拔掉U盘，重启机顶盒，在路由器找到机顶盒ip 既可登录了。

> 经过漫长安装后系统在安装完成后会自动重启，可以关注路由器里边的设备列表，重启后IP地址会发生改变，重新登陆既可。进入后线关机，拔出U盘，重新启动既可。

### 安装Docker 

> armbian安装docker非常简单 执行 armbian-docker选择安装源既可，然后就是漫长的等待

```
root@armbian:~# armbian-docker
[ INFO ] Welcome to the docker management tool.
[ STEPS ] Initialize the docker installation environment...
[ INFO ] VERSION_CODEID: [ ubuntu ]
[ INFO ] VERSION_CODENAME: [ jammy ]
[ STEPS ] Start selecting docker source...
-----------------------------------------------
ID  SOURCE
-----------------------------------------------
1   docker.com (default)
2   aliyun.com
3   ustc.edu.cn
4   tencent.com
-----------------------------------------------
```

> 我选择用力阿里的源因此直接输入2

```
[ OPTIONS ] Please Input ID: 2
Get:1 http://ports.ubuntu.com jammy InRelease [270 kB]
Get:2 http://ports.ubuntu.com jammy-security InRelease [110 kB]
Get:3 http://ports.ubuntu.com jammy-updates InRelease [114 kB]
Get:4 http://ports.ubuntu.com jammy-backports InRelease [99.8 kB]
Get:5 http://ports.ubuntu.com jammy/restricted arm64 Packages [24.2 kB]
Get:6 http://ports.ubuntu.com jammy/universe arm64 Packages [17.2 MB]
Get:7 http://ports.ubuntu.com jammy/multiverse armhf Packages [199 kB]
Get:8 http://ports.ubuntu.com jammy/main arm64 Packages [1,758 kB]
Get:9 http://ports.ubuntu.com jammy/multiverse arm64 Packages [224 kB]
Get:10 http://ports.ubuntu.com jammy/restricted armhf Packages [13.3 kB]
Get:11 http://ports.ubuntu.com jammy/universe armhf Packages [16.8 MB]
Get:12 http://ports.ubuntu.com jammy/main armhf Packages [1,701 kB]
Get:13 http://ports.ubuntu.com jammy-security/multiverse armhf Packages [594 B]
Get:14 http://ports.ubuntu.com jammy-security/main arm64 Packages [634 kB]
Get:15 http://ports.ubuntu.com jammy-security/restricted arm64 Packages [282 kB]
Get:16 http://ports.ubuntu.com jammy-security/universe arm64 Packages [653 kB]
Get:17 http://ports.ubuntu.com jammy-security/universe armhf Packages [491 kB]
Get:18 http://ports.ubuntu.com jammy-security/restricted armhf Packages [9,804 B]
Get:19 http://ports.ubuntu.com jammy-security/main armhf Packages [414 kB]
Get:20 http://ports.ubuntu.com jammy-updates/main arm64 Packages [937 kB]
Get:21 http://ports.ubuntu.com jammy-updates/restricted arm64 Packages [295 kB]
Get:22 http://ports.ubuntu.com jammy-updates/universe arm64 Packages [852 kB]
Get:23 http://ports.ubuntu.com jammy-updates/universe armhf Packages [690 kB]
Get:24 http://ports.ubuntu.com jammy-updates/main armhf Packages [693 kB]
Get:25 http://ports.ubuntu.com jammy-updates/restricted armhf Packages [10.2 kB]
Get:26 http://ports.ubuntu.com jammy-updates/multiverse arm64 Packages [3,452 B]
Get:27 http://ports.ubuntu.com jammy-updates/multiverse armhf Packages [1,333 B]
Get:28 http://ports.ubuntu.com jammy-backports/main armhf Packages [3,503 B]
Get:29 http://ports.ubuntu.com jammy-backports/universe arm64 Packages [7,297 B]
Get:30 http://ports.ubuntu.com jammy-backports/main arm64 Packages [3,511 B]
Get:31 http://ports.ubuntu.com jammy-backports/universe armhf Packages [7,289 B]
Fetched 44.5 MB in 2min 2s (366 kB/s)
Reading package lists... Done
Reading package lists... Done
Building dependency tree... Done
E: Unable to locate package docker-engine
Reading package lists... Done
Building dependency tree... Done
lsb-release is already the newest version (11.1.0ubuntu4).
ca-certificates is already the newest version (20211016ubuntu0.22.04.1).
gnupg is already the newest version (2.2.27-3ubuntu2.1).
The following additional packages will be installed:
  libcurl4
The following NEW packages will be installed:
  apt-transport-https
The following packages will be upgraded:
  curl libcurl4
2 upgraded, 1 newly installed, 0 to remove and 15 not upgraded.
Need to get 475 kB of archives.
After this operation, 169 kB of additional disk space will be used.
Get:1 http://ports.ubuntu.com jammy-updates/universe arm64 apt-transport-https all 2.4.8 [1,506 B]
Get:2 http://ports.ubuntu.com jammy-security/main arm64 curl arm64 7.81.0-1ubuntu1.7 [190 kB]
Get:3 http://ports.ubuntu.com jammy-security/main arm64 libcurl4 arm64 7.81.0-1ubuntu1.7 [284 kB]
Fetched 475 kB in 7s (68.1 kB/s)
Selecting previously unselected package apt-transport-https.
(Reading database ... 37403 files and directories currently installed.)
Preparing to unpack .../apt-transport-https_2.4.8_all.deb ...
Unpacking apt-transport-https (2.4.8) ...
Preparing to unpack .../curl_7.81.0-1ubuntu1.7_arm64.deb ...
Unpacking curl (7.81.0-1ubuntu1.7) over (7.81.0-1ubuntu1.6) ...
Preparing to unpack .../libcurl4_7.81.0-1ubuntu1.7_arm64.deb ...
Unpacking libcurl4:arm64 (7.81.0-1ubuntu1.7) over (7.81.0-1ubuntu1.6) ...
Setting up apt-transport-https (2.4.8) ...
Setting up libcurl4:arm64 (7.81.0-1ubuntu1.7) ...
Setting up curl (7.81.0-1ubuntu1.7) ...
Processing triggers for man-db (2.10.2-1) ...
Processing triggers for libc-bin (2.35-0ubuntu3.1) ...
[ STEPS ] Install docker related packages...
Get:1 https://mirrors.aliyun.com/docker-ce/linux/ubuntu jammy InRelease [48.9 kB]
Hit:2 http://ports.ubuntu.com jammy InRelease
Get:3 https://mirrors.aliyun.com/docker-ce/linux/ubuntu jammy/stable arm64 Packages [11.4 kB]
Hit:4 http://ports.ubuntu.com jammy-security InRelease
Hit:5 http://ports.ubuntu.com jammy-updates InRelease
Hit:6 http://ports.ubuntu.com jammy-backports InRelease
Fetched 60.2 kB in 3s (18.5 kB/s)
Reading package lists... Done
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Suggested packages:
  cgroupfs-mount | cgroup-lite
Recommended packages:
  apparmor docker-ce-rootless-extras libltdl7 pigz
The following NEW packages will be installed:
  containerd.io docker-ce docker-ce-cli docker-compose-plugin
0 upgraded, 4 newly installed, 0 to remove and 15 not upgraded.
Need to get 78.1 MB of archives.
After this operation, 345 MB of additional disk space will be used.
Get:1 https://mirrors.aliyun.com/docker-ce/linux/ubuntu jammy/stable arm64 containerd.io arm64 1.6.15-1 [19.9 MB]
Get:2 https://mirrors.aliyun.com/docker-ce/linux/ubuntu jammy/stable arm64 docker-ce-cli arm64 5:20.10.22~3-0~ubuntu-jammy [37.2 MB]
35% [2 docker-ce-cli 9,702 kB/37.2 MB 26%]                    121 kB/s 6min 40s^36% [2 docker-ce-cli 9,939 kB/37.2 MB 27%]                    121 kB/s 6min 38s^Get:3 https://mirrors.aliyun.com/docker-ce/linux/ubuntu jammy/stable arm64 docker-ce arm64 5:20.10.22~3-0~ubuntu-jammy [12.7 MB]
Get:4 https://mirrors.aliyun.com/docker-ce/linux/ubuntu jammy/stable arm64 docker-compose-plugin arm64 2.14.1~ubuntu-jammy [8,182 kB]
Fetched 78.1 MB in 10min 6s (129 kB/s)
Selecting previously unselected package containerd.io.
(Reading database ... 37407 files and directories currently installed.)
Preparing to unpack .../containerd.io_1.6.15-1_arm64.deb ...
Unpacking containerd.io (1.6.15-1) ...
Selecting previously unselected package docker-ce-cli.
Preparing to unpack .../docker-ce-cli_5%3a20.10.22~3-0~ubuntu-jammy_arm64.deb ...
Unpacking docker-ce-cli (5:20.10.22~3-0~ubuntu-jammy) ...
Selecting previously unselected package docker-ce.
Preparing to unpack .../docker-ce_5%3a20.10.22~3-0~ubuntu-jammy_arm64.deb ...
Unpacking docker-ce (5:20.10.22~3-0~ubuntu-jammy) ...
Selecting previously unselected package docker-compose-plugin.
Preparing to unpack .../docker-compose-plugin_2.14.1~ubuntu-jammy_arm64.deb ...
Unpacking docker-compose-plugin (2.14.1~ubuntu-jammy) ...
Setting up containerd.io (1.6.15-1) ...
Created symlink /etc/systemd/system/multi-user.target.wants/containerd.service → /lib/systemd/system/containerd.service.
Setting up docker-compose-plugin (2.14.1~ubuntu-jammy) ...
Setting up docker-ce-cli (5:20.10.22~3-0~ubuntu-jammy) ...
Setting up docker-ce (5:20.10.22~3-0~ubuntu-jammy) ...
Created symlink /etc/systemd/system/multi-user.target.wants/docker.service → /lib/systemd/system/docker.service.
Created symlink /etc/systemd/system/sockets.target.wants/docker.socket → /lib/systemd/system/docker.socket.
Processing triggers for man-db (2.10.2-1) ...
[ STEPS ] Install docker accelerator...
[ SUCCESS ] Docker installed successfully.
```



## 魔百盒M401A刷Openwrt

### 下载rom

> 从 https://github.com/ophub/amlogic-s9xxx-openwrt 下载 openwrt_official_s905l3a_k5.15.86_2023.01.08.img.gz 这个包

> 用rar 解压出来一个Image 文件

### 使用balenaEtcher 把上面得Image 文件写入U盘

### 重新插入u盘修改

> 修改 根目录下 uEnv.txt文件中得FDT 为： FDT=/dtb/amlogic/meson-g12a-s905l3a-m401a.dtb

### 打开盒子链接到网络。开启盒子得ADB

### 从U盘启动 Openwrt

> adb connet 盒子ip 
> 链接成功后 执行adb reboot update .
> 命令执行完毕后立刻将U盘插入电视盒子usb接口。

### 连接u盘系统。

> 找根网线笔记本直连 电视盒子网口

> 这时候笔记本会自动获取到IP  直接192.168.1.1 在浏览器中打开盒子。

### 写入 emmc 

> 如果想永久体验 那么就需要写入 

> 这时候在u盘系统得后台找到 系统 -> 晶晨宝盒 ->安装Openwrt 选择设备型号 [306]M401A/ZTE-B863AV3.2-M

> 点击安装，弹出框直接确认即可，稍等几分钟，系统提示成功后，直接关机，拔出U盘，然后重启，就可以进入到路由器了。

### 然后自己随心所欲玩吧，玩法太多了



## 斐讯K2刷Breed和潘多拉固件记录


> 数年前通过0元购搞了两台斐讯K2，之后因为掉包问题一直闲置没怎么用。这几天收视垃圾，发现了这玩意，感觉做工依然很棒。所以感觉不应该白白扔掉啊，折腾折腾，上网研究研究。

> 上网搜了下可以刷机，于是本着废物利用的想法下载了刷机包。这机器居然可以通刷许多第三方固件，当然了首先得刷BREED。网上得资料和固件以及刷机工具都相当齐全。先刷Breed，只要用工具简单设置一下密码就可以了。

> 后从Breed中写ROM，一路很顺利，刚开始由于下错ROM结果刷成其他牌子的，一直没发现问题，联网中继也不成功。后来发现问题后及时刷成斐讯K2适配的潘多拉，运行，设置中继都很顺利，果然废物利用了。

> 刷完后简单评测了一下，做K2刷潘多拉中继延迟非常小，但是似乎下载速度没有我TP的AC900强，但是延迟比TP小一些。总之运行非常稳定，也似乎不掉了。看来有时候还是得动动手，第三方的东西还是有不少好动的。但是其他第三方ROM还没有体验过，以后有机会了继续折腾玩一下。
