---
layout: post
title:  计算机科学相关学习内容总结
description: 计算机科学相关学习内容总结,包括各种操作系统安装配置，各种编程语言学习等
date: 2022-10-01 09:01:01
---

- [计算机史话](#计算机史话)
- [Windows](#windows)
- [LinuxAndOpenSource](#linuxandopensource)
  - [Linux 命令大全](#linux-命令大全)
    - [系统信息](#系统信息)
    - [文件搜索](#文件搜索)
    - [挂载一个文件系统](#挂载一个文件系统)
    - [磁盘空间](#磁盘空间)
    - [用户和群组](#用户和群组)
    - [打包和压缩文件](#打包和压缩文件)
    - [RPM 包 - （Fedora, Redhat及类似系统）](#rpm-包---fedora-redhat及类似系统)
    - [YUM 软件包升级器 - （Fedora, RedHat及类似系统）](#yum-软件包升级器---fedora-redhat及类似系统)
    - [DEB 包 (Debian, Ubuntu 以及类似系统)](#deb-包-debian-ubuntu-以及类似系统)
    - [查看文件内容](#查看文件内容)
    - [文本处理](#文本处理)
    - [字符设置和文件格式转换](#字符设置和文件格式转换)
    - [文件系统分析](#文件系统分析)
    - [初始化一个文件系统](#初始化一个文件系统)
    - [SWAP文件系统](#swap文件系统)
    - [备份](#备份)
    - [光盘](#光盘)
    - [网络 - （以太网和WIFI无线）](#网络---以太网和wifi无线)
  - [OpenSource主流开源协议](#opensource主流开源协议)
    - [GPL](#gpl)
    - [LGPL](#lgpl)
    - [BSD](#bsd)
    - [Apache](#apache)
    - [MIT(MITL)](#mitmitl)
    - [Mozilla(MPL)](#mozillampl)
  - [Git in linux](#git-in-linux)
    - [Download and Install GithubCli](#download-and-install-githubcli)
    - [Login](#login)
    - [Git helper](#git-helper)
  - [Docker](#docker)
    - [Docker 安装 \& 配置镜像加速器](#docker-安装--配置镜像加速器)
    - [Dockerfile 详解](#dockerfile-详解)
    - [Docker 命令详解](#docker-命令详解)
  - [Kubernetes](#kubernetes)
    - [kubernetes 概述](#kubernetes-概述)
    - [核心概念](#核心概念)
    - [kubernetes 集群搭建(kubeadm 方式)](#kubernetes-集群搭建kubeadm-方式)
    - [安装方法二](#安装方法二)
    - [kubernetes 集群搭建（二进制）](#kubernetes-集群搭建二进制)
    - [kubernetes 集群 YAML 文件详解](#kubernetes-集群-yaml-文件详解)
- [结构化程序设计](#结构化程序设计)
- [面向对象程序设计](#面向对象程序设计)
- [C# .Net Base](#c-net-base)
  - [ML.NET](#mlnet)
- [WPF](#wpf)
- [HTML 5](#html-5)
- [JQuery](#jquery)
- [Angular](#angular)
- [React](#react)
- [Vue.js](#vuejs)
- [Bootstrap学习总结](#bootstrap学习总结)
  - [Bootstrap 基础](#bootstrap-基础)
    - [媒体查询（css3特性）](#媒体查询css3特性)
      - [媒体类型](#媒体类型)
      - [媒体特性](#媒体特性)
  - [Bootstrap 布局](#bootstrap-布局)
    - [包装容器](#包装容器)
    - [响应断点](#响应断点)
    - [堆叠顺序 z-index](#堆叠顺序-z-index)
    - [网格系统](#网格系统)
  - [Bootstrap 版式](#bootstrap-版式)
    - [文档案](#文档案)
    - [图片](#图片)
    - [表格](#表格)
    - [代码](#代码)
  - [Bootstrap 通用样式](#bootstrap-通用样式)
    - [文本](#文本)
    - [颜色](#颜色)
    - [边框](#边框)
    - [定位浮动](#定位浮动)
    - [代码弹性盒子](#代码弹性盒子)
    - [其它 对齐等](#其它-对齐等)
  - [Bootstrap 组件](#bootstrap-组件)
    - [按钮](#按钮)
    - [按钮组](#按钮组)
    - [下拉](#下拉)
    - [媒体对象](#媒体对象)
    - [表单](#表单)
    - [进度条](#进度条)
    - [导航栏](#导航栏)
    - [列表组](#列表组)
    - [面包屑](#面包屑)
    - [分页](#分页)
    - [加载指示器（转圈圈）](#加载指示器转圈圈)
    - [按钮卡片](#按钮卡片)
  - [Sass](#sass)
    - [变量](#变量)
    - [嵌套归斥责](#嵌套归斥责)
    - [导入](#导入)
    - [SASS 混合器 混合器继承](#sass-混合器-混合器继承)
- [Font Awesome](#font-awesome)
- [Asp.net core MVC 一些总结](#aspnet-core-mvc-一些总结)
  - [Router](#router)
    - [property router](#property-router)
    - [设置路由中间件](#设置路由中间件)
    - [多路由](#多路由)
    - [高级路由](#高级路由)
  - [Session](#session)
  - [授权认证管理](#授权认证管理)
    - [认证](#认证)
  - [DI](#di)
  - [Filters](#filters)
    - [子类Controller拦截器要先于父类Controller拦截器执行](#子类controller拦截器要先于父类controller拦截器执行)
    - [授权过滤器 AuthorizeAttribute](#授权过滤器-authorizeattribute)
    - [资源过滤器 IResourceFilter](#资源过滤器-iresourcefilter)
    - [异常过滤器 IExceptionFilter](#异常过滤器-iexceptionfilter)
    - [操作过滤器 ActionFilterAttribute](#操作过滤器-actionfilterattribute)
    - [结果过滤器 ResultFilterAttribute](#结果过滤器-resultfilterattribute)
    - [结果过滤器 IFilterDiagnostics](#结果过滤器-ifilterdiagnostics)
    - [IAsyncResultFilter](#iasyncresultfilter)
  - [Controllers](#controllers)
    - [WebAPI](#webapi)
    - [Controller](#controller)
      - [所有的动作结果都继承自ActionResult基类 ASP.NET MVC框架支持六种标准类型的动作结果：](#所有的动作结果都继承自actionresult基类-aspnet-mvc框架支持六种标准类型的动作结果)
    - [Rezor View](#rezor-view)
  - [ViewComponent](#viewcomponent)
  - [Taghelper 可以扩展一些自定义的标记 其实就是后台生成html代码的一种形式](#taghelper-可以扩展一些自定义的标记-其实就是后台生成html代码的一种形式)
  - [SignalR](#signalr)
- [Tensorflow](#tensorflow)
- [C# 调用 Tensorflow](#c-调用-tensorflow)
- [gRPC](#grpc)
  - [gRPC 概述](#grpc-概述)
  - [gRPC 服务项目模板](#grpc-服务项目模板)
  - [ASP.NET Core gRPC 服务项目模板提供了一个入门版服务：](#aspnet-core-grpc-服务项目模板提供了一个入门版服务)
  - [使用 .NET 客户端调用 gRPC 服务](#使用-net-客户端调用-grpc-服务)
- [Php](#php)
  - [Pyplot，画出各种你想要的图](#pyplot画出各种你想要的图)
- [Python](#python)
- [Java](#java)
- [低代码平台](#低代码平台)
  - [Microsoft Platform](#microsoft-platform)
- [工业自动化](#工业自动化)
  - [变频器](#变频器)
  - [伺服](#伺服)
  - [可编程逻辑控制器](#可编程逻辑控制器)
  - [人机交互 HMI](#人机交互-hmi)
  - [传感器](#传感器)
  - [电机](#电机)
  - [PAC智能控制器](#pac智能控制器)
  - [CNC控制器](#cnc控制器)
  - [仪表](#仪表)
  - [基于PC的控制器](#基于pc的控制器)
  - [识别](#识别)
  - [工业机器人机械臂系统](#工业机器人机械臂系统)
- [工业软件](#工业软件)
  - [自动化软件](#自动化软件)
    - [TIA Portal](#tia-portal)
    - [控制器软件](#控制器软件)
    - [人机界面软件](#人机界面软件)
    - [SCADA软件](#scada软件)
    - [用于能源管理的软件](#用于能源管理的软件)
- [备注](#备注)


## 计算机史话

> 阿兰图灵是通用计算机的提出者，但是在有些问题上效率十分低下。

> 图灵机，又称图灵计算机指一个抽象的机器，是，英国数学家艾伦・麦席森・图灵(1912―-1954年)于1936年提出的一种抽象的计算模型，即将人们使用纸笔进行数学运算的过程进行抽象，由一个虚拟的机器替代人类进行数学运算。它有一条无限长的纸带，纸带分成了一个一个的小方格，每个方格有不同的颜色。有一个机器头在纸带上移来移去。机器头有一组内部状态，还有一些固定的程序。在每个时刻，机器头都要从当前纸带上读入一个方格信息，然后结合自己的内部状态查找程序表，根据程序输出信息到纸带方格上，并转换自己的内部状态，然后进行移动

> 最早的存储指令结构计算机模型实际是由ENIAC创建者埃可特和莫奇利，冯诺依曼与以上二位共同商议，1944年9月起草了《EDVAC报告书一号草案》，并署名，且为埃可特和莫奇利留了署名位置，但戈德斯塔提前发表了这份报告导致埃可特和莫奇利没有书名，所以现在存储程序计算机的逻辑结构成了广为人知的“冯诺依曼体系结构”。明确提出了，存储程序，顺序执行指令，使用二进制开关电路。并且这个体系产生了两个新的工程学科，计计算机体系结构和软件工程。冯诺依曼把计算机硬件划分为：CA（中央运算单元）CC（中央控制单元）M（内存）I（输入设备）O（输出设备。）

> 第一台冯诺依曼体系计算机1948年6月研制出原型机"Baby"由英国团队研制出来。

> 二战期间英国的计算机水平非常厉害，但是英国政府隐瞒了计算机方面研究的成就，包括阿兰图林一度不为人所知，因此导致美国冯诺依曼体系结构成了以后计算机的主要设计思想。

> 香农定律是关于信道容量的计算的一个经典定律，可以说是信息论的基础。

> Bug 一次是女程序员葛蕾丝霍普引入。

## Windows

## LinuxAndOpenSource

### Linux 命令大全

#### 系统信息 

> cat /etc/redhat-release 显示安装的系统版本

> getconf LONG_BIT 显示系统是多少位的（32/64bit）

> centos7的防火墙相关：

> firewall-cmd --state （防火墙状态）

> systemctl list-unit-files|grep firewalld.service（防火墙状态）

> systemctl restart firewalld.service(重启防火墙)

> systemctl disable firewalld.service（禁止开机自动启动）

> centos7以下的防火墙相关：

> service iptables stop(关闭防火墙centos7以下)

> chkconfig iptables off（禁止开机自动启动）

> arch 显示机器的处理器架构(1) 

> uname -m 显示机器的处理器架构(2) 

> uname -r 显示正在使用的内核版本 

> dmidecode -q 显示硬件系统部件 - (SMBIOS / DMI) 

> hdparm -i /dev/hda 罗列一个磁盘的架构特性 

> hdparm -tT /dev/sda 在磁盘上执行测试性读取操作 

> cat /proc/cpuinfo 显示CPU info的信息 

> cat /proc/interrupts 显示中断 

> cat /proc/meminfo 校验内存使用 

> cat /proc/swaps 显示哪些swap被使用 

> cat /proc/version 显示内核的版本 

> cat /proc/net/dev 显示网络适配器及统计 

> cat /proc/mounts 显示已加载的文件系统 

> lspci -tv 罗列 PCI 设备 

> lsusb -tv 显示 USB 设备 

> date 显示系统日期 

> cal 2007 显示2007年的日历表 

> date 041217002007.00 设置日期和时间 - 月日时分年.秒 

> clock -w 将时间修改保存到 BIOS 

> 关机 (系统的关机、重启以及登出 ) 

> shutdown -h now 关闭系统(1) 

> init 0 关闭系统(2) 

> telinit 0 关闭系统(3) 

> shutdown -h hours:minutes & 按预定时间关闭系统 

> shutdown -c 取消按预定时间关闭系统 

> shutdown -r now 重启(1) 

> reboot 重启(2) 

> logout 注销 

> 文件和目录

> cd /home 进入 '/home' 目录' 

> cd .. 返回上一级目录 

> cd ../.. 返回上两级目录 

> cd 进入个人的主目录 

> cd ~user1 进入个人的主目录 

> cd - 返回上次所在的目录 

> pwd 显示工作路径 

> ls 查看目录中的文件 

> ls -F 查看目录中的文件 

> ls -l 显示文件和目录的详细资料 

> ls -a 显示隐藏文件 

> ls *[0-9]* 显示包含数字的文件名和目录名 

> tree 显示文件和目录由根目录开始的树形结构(1) 

> lstree 显示文件和目录由根目录开始的树形结构(2) 

> mkdir dir1 创建一个叫做 'dir1' 的目录' 

> mkdir dir1 dir2 同时创建两个目录 

> mkdir -p /tmp/dir1/dir2 创建一个目录树 

> rm -f file1 删除一个叫做 'file1' 的文件' 

> rmdir dir1 删除一个叫做 'dir1' 的目录' 

> rm -rf dir1 删除一个叫做 'dir1' 的目录并同时删除其内容 

> rm -rf dir1 dir2 同时删除两个目录及它们的内容 

> mv dir1 new_dir 重命名/移动 一个目录 

> cp file1 file2 复制一个文件 

> cp dir/* . 复制一个目录下的所有文件到当前工作目录 

> cp -a /tmp/dir1 . 复制一个目录到当前工作目录 

> cp -a dir1 dir2 复制一个目录 

> ln -s file1 lnk1 创建一个指向文件或目录的软链接 

> ln file1 lnk1 创建一个指向文件或目录的物理链接 

> touch -t 0712250000 file1 修改一个文件或目录的时间戳 - (YYMMDDhhmm) 

> file file1 outputs the mime type of the file as text 

> iconv -l 列出已知的编码 

> iconv -f fromEncoding -t toEncoding inputFile > outputFile creates a new from the given input file by assuming it is encoded in fromEncoding and converting it to toEncoding. 

> find . -maxdepth 1 -name *.jpg -print -exec convert "{}" -resize 80x60 "thumbs/{}" \; batch resize files in the current directory and send them to a thumbnails directory (requires convert from Imagemagick)

#### 文件搜索 

> find / -name file1 从 '/' 开始进入根文件系统搜索文件和目录 

> find / -user user1 搜索属于用户 'user1' 的文件和目录 

> find /home/user1 -name \*.bin 在目录 '/ home/user1' 中搜索带有'.bin' 结尾的文件 

> find /usr/bin -type f -atime +100 搜索在过去100天内未被使用过的执行文件 

> find /usr/bin -type f -mtime -10 搜索在10天内被创建或者修改过的文件 

> find / -name \*.rpm -exec chmod 755 '{}' \; 搜索以 '.rpm' 结尾的文件并定义其权限 

> find / -xdev -name \*.rpm 搜索以 '.rpm' 结尾的文件，忽略光驱、捷盘等可移动设备 

> locate \*.ps 寻找以 '.ps' 结尾的文件 - 先运行 'updatedb' 命令 

> whereis halt 显示一个二进制文件、源码或man的位置 

> which halt 显示一个二进制文件或可执行文件的完整路径

#### 挂载一个文件系统 

> mount /dev/hda2 /mnt/hda2 挂载一个叫做hda2的盘 - 确定目录 '/ mnt/hda2' 已经存在 

> umount /dev/hda2 卸载一个叫做hda2的盘 - 先从挂载点 '/ mnt/hda2' 退出 

> fuser -km /mnt/hda2 当设备繁忙时强制卸载 

> umount -n /mnt/hda2 运行卸载操作而不写入 /etc/mtab 文件- 当文件为只读或当磁盘写满时非常有用 

> mount /dev/fd0 /mnt/floppy 挂载一个软盘 

> mount /dev/cdrom /mnt/cdrom 挂载一个cdrom或dvdrom 

> mount /dev/hdc /mnt/cdrecorder 挂载一个cdrw或dvdrom 

> mount /dev/hdb /mnt/cdrecorder 挂载一个cdrw或dvdrom 

> mount -o loop file.iso /mnt/cdrom 挂载一个文件或ISO镜像文件 

> mount -t vfat /dev/hda5 /mnt/hda5 挂载一个Windows FAT32文件系统 

> mount /dev/sda1 /mnt/usbdisk 挂载一个usb 捷盘或闪存设备 

> mount -t smbfs -o username=user,password=pass //WinClient/share /mnt/share 挂载一个windows网络共享

#### 磁盘空间 

> df -h 显示已经挂载的分区列表 

> ls -lSr |more 以尺寸大小排列文件和目录 

> du -sh dir1 估算目录 'dir1' 已经使用的磁盘空间' 

> du -sk * | sort -rn 以容量大小为依据依次显示文件和目录的大小 

> rpm -q -a --qf '%10{SIZE}t%{NAME}n' | sort -k1,1n 以大小为依据依次显示已安装的rpm包所使用的空间 (fedora, redhat类系统) 

> dpkg-query -W -f='${Installed-Size;10}t${Package}n' | sort -k1,1n 以大小为依据显示已安装的deb包所使用的空间 (ubuntu, debian类系统)

#### 用户和群组 

> groupadd group_name 创建一个新用户组 

> groupdel group_name 删除一个用户组 

> groupmod -n new_group_name old_group_name 重命名一个用户组 

> useradd -c "Name Surname " -g admin -d /home/user1 -s /bin/bash user1 创建一个属于 "admin" 用户组的用户 

> useradd user1 创建一个新用户 

> userdel -r user1 删除一个用户 ( '-r' 排除主目录) 

> usermod -c "User FTP" -g system -d /ftp/user1 -s /bin/nologin user1 修改用户属性 

> passwd 修改口令 

> passwd user1 修改一个用户的口令 (只允许root执行) 

> chage -E 2005-12-31 user1 设置用户口令的失效期限 

> pwck 检查 '/etc/passwd' 的文件格式和语法修正以及存在的用户 

> grpck 检查 '/etc/passwd' 的文件格式和语法修正以及存在的群组 

> newgrp group_name 登陆进一个新的群组以改变新创建文件的预设群组

>  文件的权限 - 使用 "+" 设置权限，使用 "-" 用于取消 

> ls -lh 显示权限 

> ls /tmp | pr -T5 -W$COLUMNS 将终端划分成5栏显示 

> chmod ugo+rwx directory1 设置目录的所有人(u)、群组(g)以及其他人(o)以读（r ）、写(w)和执行(x)的权限 

> chmod go-rwx directory1 删除群组(g)与其他人(o)对目录的读写执行权限 

> chown user1 file1 改变一个文件的所有人属性 

> chown -R user1 directory1 改变一个目录的所有人属性并同时改变改目录下所有文件的属性 

> chgrp group1 file1 改变文件的群组 

> chown user1:group1 file1 改变一个文件的所有人和群组属性 

> find / -perm -u+s 罗列一个系统中所有使用了SUID控制的文件 

> chmod u+s /bin/file1 设置一个二进制文件的 SUID 位 - 运行该文件的用户也被赋予和所有者同样的权限 

> chmod u-s /bin/file1 禁用一个二进制文件的 SUID位 

> chmod g+s /home/public 设置一个目录的SGID 位 - 类似SUID ，不过这是针对目录的 

> chmod g-s /home/public 禁用一个目录的 SGID 位 

> chmod o+t /home/public 设置一个文件的 STIKY 位 - 只允许合法所有人删除文件 

> chmod o-t /home/public 禁用一个目录的 STIKY 位

>  文件的特殊属性 - 使用 "+" 设置权限，使用 "-" 用于取消 

> chattr +a file1 只允许以追加方式读写文件 

> chattr +c file1 允许这个文件能被内核自动压缩/解压 

> chattr +d file1 在进行文件系统备份时，dump程序将忽略这个文件 

> chattr +i file1 设置成不可变的文件，不能被删除、修改、重命名或者链接 

> chattr +s file1 允许一个文件被安全地删除 

> chattr +S file1 一旦应用程序对这个文件执行了写操作，使系统立刻把修改的结果写到磁盘 

> chattr +u file1 若文件被删除，系统会允许你在以后恢复这个被删除的文件 

> lsattr 显示特殊的属性

#### 打包和压缩文件 

> bunzip2 file1.bz2 解压一个叫做 'file1.bz2'的文件 

> bzip2 file1 压缩一个叫做 'file1' 的文件 

> gunzip file1.gz 解压一个叫做 'file1.gz'的文件 

> gzip file1 压缩一个叫做 'file1'的文件 

> gzip -9 file1 最大程度压缩 

> rar a file1.rar test_file 创建一个叫做 'file1.rar' 的包 

> rar a file1.rar file1 file2 dir1 同时压缩 'file1', 'file2' 以及目录 'dir1' 

> rar x file1.rar 解压rar包 

> unrar x file1.rar 解压rar包 

> tar -cvf archive.tar file1 创建一个非压缩的 tarball 

> tar -cvf archive.tar file1 file2 dir1 创建一个包含了 'file1', 'file2' 以及 'dir1'的档案文件 

> tar -tf archive.tar 显示一个包中的内容 

> tar -xvf archive.tar 释放一个包 

> tar -xvf archive.tar -C /tmp 将压缩包释放到 /tmp目录下 

> tar -cvfj archive.tar.bz2 dir1 创建一个bzip2格式的压缩包 

> tar -xvfj archive.tar.bz2 解压一个bzip2格式的压缩包 

> tar -cvfz archive.tar.gz dir1 创建一个gzip格式的压缩包 

> tar -xvfz archive.tar.gz 解压一个gzip格式的压缩包 

> zip file1.zip file1 创建一个zip格式的压缩包 

> zip -r file1.zip file1 file2 dir1 将几个文件和目录同时压缩成一个zip格式的压缩包 

> unzip file1.zip 解压一个zip格式压缩包

#### RPM 包 - （Fedora, Redhat及类似系统） 

> rpm -ivh package.rpm 安装一个rpm包 

> rpm -ivh --nodeeps package.rpm 安装一个rpm包而忽略依赖关系警告 

> rpm -U package.rpm 更新一个rpm包但不改变其配置文件 

> rpm -F package.rpm 更新一个确定已经安装的rpm包 

> rpm -e package_name.rpm 删除一个rpm包 

> rpm -qa 显示系统中所有已经安装的rpm包 

> rpm -qa | grep httpd 显示所有名称中包含 "httpd" 字样的rpm包 

> rpm -qi package_name 获取一个已安装包的特殊信息 

> rpm -qg "System Environment/Daemons" 显示一个组件的rpm包 

> rpm -ql package_name 显示一个已经安装的rpm包提供的文件列表 

> rpm -qc package_name 显示一个已经安装的rpm包提供的配置文件列表 

> rpm -q package_name --whatrequires 显示与一个rpm包存在依赖关系的列表 

> rpm -q package_name --whatprovides 显示一个rpm包所占的体积 

> rpm -q package_name --scripts 显示在安装/删除期间所执行的脚本l 

> rpm -q package_name --changelog 显示一个rpm包的修改历史 

> rpm -qf /etc/httpd/conf/httpd.conf 确认所给的文件由哪个rpm包所提供 

> rpm -qp package.rpm -l 显示由一个尚未安装的rpm包提供的文件列表 

> rpm --import /media/cdrom/RPM-GPG-KEY 导入公钥数字证书 

> rpm --checksig package.rpm 确认一个rpm包的完整性 

> rpm -qa gpg-pubkey 确认已安装的所有rpm包的完整性 

> rpm -V package_name 检查文件尺寸、 许可、类型、所有者、群组、MD5检查以及最后修改时间 

> rpm -Va 检查系统中所有已安装的rpm包- 小心使用 

> rpm -Vp package.rpm 确认一个rpm包还未安装 

> rpm2cpio package.rpm | cpio --extract --make-directories *bin* 从一个rpm包运行可执行文件 

> rpm -ivh /usr/src/redhat/RPMS/`arch`/package.rpm 从一个rpm源码安装一个构建好的包 

> rpmbuild --rebuild package_name.src.rpm 从一个rpm源码构建一个 rpm 包

#### YUM 软件包升级器 - （Fedora, RedHat及类似系统） 

> yum install package_name 下载并安装一个rpm包 

> yum localinstall package_name.rpm 将安装一个rpm包，使用你自己的软件仓库为你解决所有依赖关系 

> yum update package_name.rpm 更新当前系统中所有安装的rpm包 

> yum update package_name 更新一个rpm包 

> yum remove package_name 删除一个rpm包 

> yum list 列出当前系统中安装的所有包 

> yum search package_name 在rpm仓库中搜寻软件包 

> yum clean packages 清理rpm缓存删除下载的包 

> yum clean headers 删除所有头文件 

> yum clean all 删除所有缓存的包和头文件

#### DEB 包 (Debian, Ubuntu 以及类似系统) 

> dpkg -i package.deb 安装/更新一个 deb 包 

> dpkg -r package_name 从系统删除一个 deb 包 

> dpkg -l 显示系统中所有已经安装的 deb 包 

> dpkg -l | grep httpd 显示所有名称中包含 "httpd" 字样的deb包 

> dpkg -s package_name 获得已经安装在系统中一个特殊包的信息 

> dpkg -L package_name 显示系统中已经安装的一个deb包所提供的文件列表 

> dpkg --contents package.deb 显示尚未安装的一个包所提供的文件列表 

> dpkg -S /bin/ping 确认所给的文件由哪个deb包提供 

> APT 软件工具 (Debian, Ubuntu 以及类似系统) 

> apt-get install package_name 安装/更新一个 deb 包 

> apt-cdrom install package_name 从光盘安装/更新一个 deb 包 

> apt-get update 升级列表中的软件包 

> apt-get upgrade 升级所有已安装的软件 

> apt-get remove package_name 从系统删除一个deb包 

> apt-get check 确认依赖的软件仓库正确 

> apt-get clean 从下载的软件包中清理缓存 

> apt-cache search searched-package 返回包含所要搜索字符串的软件包名称

#### 查看文件内容 

> cat file1 从第一个字节开始正向查看文件的内容 

> tac file1 从最后一行开始反向查看一个文件的内容 

> more file1 查看一个长文件的内容 

> less file1 类似于 'more' 命令，但是它允许在文件中和正向操作一样的反向操作 

> head -2 file1 查看一个文件的前两行 

> tail -2 file1 查看一个文件的最后两行 

> tail -f /var/log/messages 实时查看被添加到一个文件中的内容 

#### 文本处理 

> cat file1 file2 ... | command <> file1_in.txt_or_file1_out.txt general syntax for text manipulation using PIPE, STDIN and STDOUT 

> cat file1 | command( sed, grep, awk, grep, etc...) > result.txt 合并一个文件的详细说明文本，并将简介写入一个新文件中 

> cat file1 | command( sed, grep, awk, grep, etc...) >> result.txt 合并一个文件的详细说明文本，并将简介写入一个已有的文件中 

> grep Aug /var/log/messages 在文件 '/var/log/messages'中查找关键词"Aug" 

> grep ^Aug /var/log/messages 在文件 '/var/log/messages'中查找以"Aug"开始的词汇 

> grep [0-9] /var/log/messages 选择 '/var/log/messages' 文件中所有包含数字的行 

> grep Aug -R /var/log/* 在目录 '/var/log' 及随后的目录中搜索字符串"Aug" 

> sed 's/stringa1/stringa2/g' example.txt 将example.txt文件中的 "string1" 替换成 "string2" 

> sed '/^$/d' example.txt 从example.txt文件中删除所有空白行 

> sed '/ *#/d; /^$/d' example.txt 从example.txt文件中删除所有注释和空白行 

> echo 'esempio' | tr '[:lower:]' '[:upper:]' 合并上下单元格内容 

> sed -e '1d' result.txt 从文件example.txt 中排除第一行 

> sed -n '/stringa1/p' 查看只包含词汇 "string1"的行 

> sed -e 's/ *$//' example.txt 删除每一行最后的空白字符 

> sed -e 's/stringa1//g' example.txt 从文档中只删除词汇 "string1" 并保留剩余全部 

> sed -n '1,5p;5q' example.txt 查看从第一行到第5行内容 

> sed -n '5p;5q' example.txt 查看第5行 

> sed -e 's/00*/0/g' example.txt 用单个零替换多个零 

> cat -n file1 标示文件的行数 

> cat example.txt | awk 'NR%2==1' 删除example.txt文件中的所有偶数行 

> echo a b c | awk '{print $1}' 查看一行第一栏 

> echo a b c | awk '{print $1,$3}' 查看一行的第一和第三栏 

> paste file1 file2 合并两个文件或两栏的内容 

> paste -d '+' file1 file2 合并两个文件或两栏的内容，中间用"+"区分 

> sort file1 file2 排序两个文件的内容 

> sort file1 file2 | uniq 取出两个文件的并集(重复的行只保留一份) 

> sort file1 file2 | uniq -u 删除交集，留下其他的行 

> sort file1 file2 | uniq -d 取出两个文件的交集(只留下同时存在于两个文件中的文件) 

> comm -1 file1 file2 比较两个文件的内容只删除 'file1' 所包含的内容 

> comm -2 file1 file2 比较两个文件的内容只删除 'file2' 所包含的内容 

> comm -3 file1 file2 比较两个文件的内容只删除两个文件共有的部分 

#### 字符设置和文件格式转换 

> dos2unix filedos.txt fileunix.txt 将一个文本文件的格式从MSDOS转换成UNIX 

> unix2dos fileunix.txt filedos.txt 将一个文本文件的格式从UNIX转换成MSDOS 

> recode ..HTML < page.txt > page.html 将一个文本文件转换成html 

> recode -l | more 显示所有允许的转换格式 

#### 文件系统分析 

> badblocks -v /dev/hda1 检查磁盘hda1上的坏磁块 

> fsck /dev/hda1 修复/检查hda1磁盘上linux文件系统的完整性 

> fsck.ext2 /dev/hda1 修复/检查hda1磁盘上ext2文件系统的完整性 

> e2fsck /dev/hda1 修复/检查hda1磁盘上ext2文件系统的完整性 

> e2fsck -j /dev/hda1 修复/检查hda1磁盘上ext3文件系统的完整性 

> fsck.ext3 /dev/hda1 修复/检查hda1磁盘上ext3文件系统的完整性 

> fsck.vfat /dev/hda1 修复/检查hda1磁盘上fat文件系统的完整性 

> fsck.msdos /dev/hda1 修复/检查hda1磁盘上dos文件系统的完整性 

> dosfsck /dev/hda1 修复/检查hda1磁盘上dos文件系统的完整性 

#### 初始化一个文件系统 

> mkfs /dev/hda1 在hda1分区创建一个文件系统 

> mke2fs /dev/hda1 在hda1分区创建一个linux ext2的文件系统 

> mke2fs -j /dev/hda1 在hda1分区创建一个linux ext3(日志型)的文件系统 

> mkfs -t vfat 32 -F /dev/hda1 创建一个 FAT32 文件系统 

> fdformat -n /dev/fd0 格式化一个软盘 

> mkswap /dev/hda3 创建一个swap文件系统 

#### SWAP文件系统 

> mkswap /dev/hda3 创建一个swap文件系统 

> swapon /dev/hda3 启用一个新的swap文件系统 

> swapon /dev/hda2 /dev/hdb3 启用两个swap分区 

#### 备份 

> dump -0aj -f /tmp/home0.bak /home 制作一个 '/home' 目录的完整备份 

> dump -1aj -f /tmp/home0.bak /home 制作一个 '/home' 目录的交互式备份 

> restore -if /tmp/home0.bak 还原一个交互式备份 

> rsync -rogpav --delete /home /tmp 同步两边的目录 

> rsync -rogpav -e ssh --delete /home ip_address:/tmp 通过SSH通道rsync 

> rsync -az -e ssh --delete ip_addr:/home/public /home/local 通过ssh和压缩将一个远程目录同步到本地目录 

> rsync -az -e ssh --delete /home/local ip_addr:/home/public 通过ssh和压缩将本地目录同步到远程目录 

> dd bs=1M if=/dev/hda | gzip | ssh user@ip_addr 'dd of=hda.gz' 通过ssh在远程主机上执行一次备份本地磁盘的操作 

> dd if=/dev/sda of=/tmp/file1 备份磁盘内容到一个文件 

> tar -Puf backup.tar /home/user 执行一次对 '/home/user' 目录的交互式备份操作 

> ( cd /tmp/local/ && tar c . ) | ssh -C user@ip_addr 'cd /home/share/ && tar x -p' 通过ssh在远程目录中复制一个目录内容 

> ( tar c /home ) | ssh -C user@ip_addr 'cd /home/backup-home && tar x -p' 通过ssh在远程目录中复制一个本地目录 

> tar cf - . | (cd /tmp/backup ; tar xf - ) 本地将一个目录复制到另一个地方，保留原有权限及链接 

> find /home/user1 -name '*.txt' | xargs cp -av --target-directory=/home/backup/ --parents 从一个目录查找并复制所有以 '.txt' 结尾的文件到另一个目录 

> find /var/log -name '*.log' | tar cv --files-from=- | bzip2 > log.tar.bz2 查找所有以 '.log' 结尾的文件并做成一个bzip包 

> dd if=/dev/hda of=/dev/fd0 bs=512 count=1 做一个将 MBR (Master Boot Record)内容复制到软盘的动作 

> dd if=/dev/fd0 of=/dev/hda bs=512 count=1 从已经保存到软盘的备份中恢复MBR内容 

#### 光盘 

> cdrecord -v gracetime=2 dev=/dev/cdrom -eject blank=fast -force 清空一个可复写的光盘内容 

> mkisofs /dev/cdrom > cd.iso 在磁盘上创建一个光盘的iso镜像文件 

> mkisofs /dev/cdrom | gzip > cd_iso.gz 在磁盘上创建一个压缩了的光盘iso镜像文件 

> mkisofs -J -allow-leading-dots -R -V "Label CD" -iso-level 4 -o ./cd.iso data_cd 创建一个目录的iso镜像文件 

> cdrecord -v dev=/dev/cdrom cd.iso 刻录一个ISO镜像文件 

> gzip -dc cd_iso.gz | cdrecord dev=/dev/cdrom - 刻录一个压缩了的ISO镜像文件 

> mount -o loop cd.iso /mnt/iso 挂载一个ISO镜像文件 

> cd-paranoia -B 从一个CD光盘转录音轨到 wav 文件中 

> cd-paranoia -- "-3" 从一个CD光盘转录音轨到 wav 文件中（参数-3） 

> cdrecord --scanbus 扫描总线以识别scsi通道 

> dd if=/dev/hdc | md5sum 校验一个设备的md5sum编码，例如一张 CD 

#### 网络 - （以太网和WIFI无线）

> ifconfig eth0 显示一个以太网卡的配置 

> ifup eth0 启用一个 'eth0' 网络设备 

> ifdown eth0 禁用一个 'eth0' 网络设备 

> ifconfig eth0 192.168.1.1 netmask 255.255.255.0 控制IP地址 

> ifconfig eth0 promisc 设置 'eth0' 成混杂模式以嗅探数据包 (sniffing) 

> dhclient eth0 以dhcp模式启用 'eth0' 

> route -n show routing table 

> route add -net 0/0 gw IP_Gateway configura default gateway 

> route add -net 192.168.0.0 netmask 255.255.0.0 gw 192.168.1.1 configure static route to reach network '192.168.0.0/16' 

> route del 0/0 gw IP_gateway remove static route 

> echo "1" > /proc/sys/net/ipv4/ip_forward activate ip routing 

> hostname show hostname of system 

> host www.example.com lookup hostname to resolve name to ip address and viceversa(1) 

> nslookup www.example.com lookup hostname to resolve name to ip address and viceversa(2) 

> ip link show show link status of all interfaces 

> mii-tool eth0 show link status of 'eth0' 

> ethtool eth0 show statistics of network card 'eth0' 

> netstat -tup show all active network connections and their PID 

> netstat -tupl show all network services listening on the system and their PID 

> tcpdump tcp port 80 show all HTTP traffic 

> iwlist scan show wireless networks 

> iwconfig eth1 show configuration of a wireless network card 

> hostname show hostname 

> host www.example.com lookup hostname to resolve name to ip address and viceversa 

> nslookup www.example.com lookup hostname to resolve name to ip address and viceversa 

> whois www.example.com lookup on Whois database 

### OpenSource主流开源协议

#### GPL

> 最开放，只要引用GPL协议的软件必须开源免费，不适合商业软件 有5大自由 使用，复制，修改，衍生，收费。

#### LGPL

> 较GPL 宽松

#### BSD  

> 发布带源代码 则源代码必须遵循BSD

> 发布只有二进制则必须声明遵循了BSD协议

#### Apache 

> 软件以及衍生品必须继续使用Apache许可。

> 修改了源代码则必须声明

> 基于他人源代码则必须保留原始代码的许可商标声明等。

> 类库保护，只正对引用的类库，而无须适用整个软件系统。

> 发布软件中有声明软件则需在此文件中注明基于Apache 和其他协议。

#### MIT(MITL)

> 修改后的源代码需要保留作者的许可信息即可。

#### Mozilla(MPL)

> 后续只开源使用的特定代码

> 多种协议可以混合使用

> 发布软件附带专门说明文件有原始的代码的修改时间和方式。

### Git in linux 

#### Download and Install GithubCli

> https://github.com/cli/cli/releases

#### Login 

> $ gh auth login (config use ssh,need your token from github config)

#### Git helper 

> $ git clone git@github.com:devgis/MyWriting.git  //need your private key
> 提交修改 上传修改的代码后执行增加修改： 
> $ git add . 
> 增加修改信息： 
> $ git commit -m ‘修改lol清晰增加口径’ 
> 推送分支： 
> $ git push origin main

### Docker 

#### Docker 安装 & 配置镜像加速器

> step 1：安装必要的一些系统工具

> > apt update

> > apt -y install apt-transport-https ca-certificates curl software-properties-common

> step 2：安装 GPG 证书

> > curl -fsSL http://mirrors.aliyun.com/docker-ce/linux/ubuntu/gpg | apt-key add -

> Step 3：写入软件源信息

> > add-apt-repository "deb [arch=amd64] http://mirrors.aliyun.com/docker-ce/linux/ubuntu $(lsb_release -cs) stable"

> Step 4：更新并安装 Docker-CE

> > apt -y update

> > apt -y install docker-ce

> > mkdir -p /etc/docker

> > tee /etc/docker/daemon.json <<-'EOF'

> > {

> >   "registry-mirrors": ["https://jrzzvzok.mirror.aliyuncs.com"]

> > }

> > EOF

> > systemctl daemon-reload

> > systemctl restart docker


#### Dockerfile 详解

> Docker 的架构很有魅力，他拥有类似于虚拟机性质的隔离机制，但并不是严格意义上的虚拟机。我还是喜欢拿货轮举例，以前我们是一条小船运一个集装箱的货物，现在可以把 N 个集装箱扔到一条大货轮上。每个容器（集装箱）共用宿主机（货轮）的内核（运载力），Dockerfile 就像是每个集装箱中的货物清单和说明书，一般由以下五部分构成：

> 2.1 基础指令

> > FROM： 指定基础镜像，且必须位于第一行，使用格式如下：

> > FROM <image>

> > FROM <image>:<tag>

> > FROM <image>@<digest>

> > Docker 的原理基于 Linux 内核的隔离技术，且 Linux From Scratch，因此 FROM scratch 是 docker 中最基础的镜像，debian、ubuntu 和 centos 等都基于 scratch 之上。在实际的运用中，如果必须从零开始搭建镜像的一般都选择 FROM debian 作为基础镜像，不过大多数情况下一般都会以如下：FROM python、FROM nginx、FROM java 等为基础镜像。

> > MAINTAINER：指定维护者信息，例：MAINTAINER user user@mail.com。

> 2.2 控制指令

> > RUN： 在构建的过程中指定需要被执行的命令，使用格式如下：

> > RUN command param1 param2 # 更推荐

> > RUN ["executable","param1","param2"]

> > WORKDIR： 用于切换构建过程中的工作目录，例：WORKDIR project。可配合环境变量使用，例：

> > ENV BASEDIR /project

> > WORKDIR $BASEDIR/test

> > ONBUILD: 在当前镜像被当做基础镜像时，执行其携带指令，例：ONBUILD RUN echo "hello world" “hello world”会在子镜像被构建的过程中输出。

> 2.3 引入指令

> > COPY： 拷贝文件或目录，格式：

> > COPY <src> <dest>

> > COPY ["<src>","<dest>"]

> > ADD： 在COPY的基础之上，ADD可识别压缩文件，例：ADD rootfs.tar.xz /。理论上也可添加网络地址，但还是建议在 RUN 指令中执行 wget 或 curl 命令，感觉这样更加可控。实际应用中我喜欢将 COPY 用于文件，ADD 用于目录（仅我个人的使用习惯）。

> 2.4 执行指令

> > CMD： 容器启动时需要执行的命令，格式：

> > CMD ["executable","param1","param2"] # 更推荐

> > CMD ["param1","param2"]

> > CMD command param1 param2 

> > 若在 docker run 中指定启动命令，则 CMD 将被覆盖。

> > ENTRYPOINT：主程序启动前的准备指令，用于启动主程序所依赖的服务，格式同CMD（基本上没用过就不介绍了，而且容易出错，不推荐使用）。

> 2.5 配置指令

> > EXPOSE： 暴露容器端口，格式：EXPOSE <port> [<port>...]，注意此处的暴露端口和docker run 中-p指定的映射端口是两个概念。

> > ENV： 声明环境变量，格式：ENV <key>=<value> ...。

> > LABEL： 标记，格式：LABEL <key>=<value>...。

> > USER： 设置启动容器的用户，格式：USER daemo。

> > ARG： 设置变量，格式同ENV。

> > STOPSIGNAL： 容器停止时给应用程序发出的信号，例：STOPSIGNAL SIGKELL。

> > SHELL： 指定shell，例：SHELL ["bash","-c"]。

#### Docker 命令详解

> 为了避免喧宾夺主，此处仅摘录我个人操作中较为常用的命令。

> 3.1 生命周期管理

> > run： 创建并运行容器，格式：docker run [OPTIONS] IMAGE [COMMAND] [ARG...]，参数说明：

> > -d , --detach            # 后台运行

> > -it, --interactive tty   # 交互终端形式运行

> > -p , --publish list      # 指定端口

> > -v , --volume list       # 挂载存储卷

> > 		 --name string       # 定义名字

> > 		 --rm                # 容器终止后自动删除（不支持在后台运行的容器）

> > 		 --restart string    # no、on-failure（非正常退出时重启，on-failure:3 最多重启三次）、always、unless-stopped

> > docker run 的参数甚多，可通过 --help 查询，后续这些复杂的配置都会移交给 Docker Compose，以上几个足以应用70%~80%的场景，例：

> 类似 ubuntu 这类容器必须以 -it 交互终端形式运行，否则无法在后台保留

> > docker run -it -d --name my-ubuntu ubuntu

> 端口映射和挂载数据卷

> > docker run -d \

> > -p 8080:80 \

> > -v /data/www:/usr/share/nginx/html\

> > --name my-nginx nginx

> > start/stop/restart：docker start/stop/restart my-container。

> > rm：移除容器，格式：docker rm [OPTIONS] CONTAINER [CONTAINER...]，参数说明：

> > -f, --force     Force the removal of a running container

> > -l, --link      Remove the specified link

> > -v, --volumes   Remove the volumes associated with the container

> > exec：在运行的容器中执行命令，不过更常用的还是先进入容器再执行命令，例子:docker exec -it my-nginx bash。

> 3.2 容器操作

> > ps： 列出容器，常用：docker ps -anq，参数说明：all、n last（最新 n 个容器）、quiet（只显示容器编号）。

> > top： 查看容器中的进程信息，例：docker top my-container。

> > logs： 查看容器日志，常用：docker logs -f --tail，参数说明：follow、--tail n（最新条日志）。

> > port：查看端口映射情况，例：docker port my-container。

> 3.3 镜像仓库

> > login/logout： 镜像仓库的登录和退出，格式：

> > docker login [OPTIONS] [SERVER]

> > docker logout  [SERVER]

> > 如果是Docker Hub，则示例如下：

> > docker login -u username -p passward

> > docker logout

> > 在生产环境中，我们一般会选择使用云厂商的镜像仓库，例：

> > docker login -u yo****@qq.com -p ****** registry-vpc.cn-hangzhou.aliyuncs.com

> > docker logout registry-vpc.cn-hangzhou.aliyuncs.com 

> > pull： 拉取镜像，最常用的命令之一，格式：docker pull [OPTIONS] NAME[:TAG|@DIGEST]。

> > push： 上传镜像，格式：docker push [OPTIONS] NAME[:TAG]。

> 3.4 本地镜像管理

> > images： 列出本地镜像，常用 docker images -q，参数说明：quiet（只显示image Id）。

> > rmi： 删除本地镜像，常用 docker rmi -f，参数说明：force。

> > tag： 标记镜像，归入仓库，格式：docker tag [OPTIONS] IMAGE[:TAG] [REGISTRYHOST/][USERNAME/]NAME[:TAG]，例：docker tag ubuntu youclk/my-ubuntu:v1。

> > build： 使用Dockerfile创建镜像，格式：docker build [OPTIONS] PATH | URL | -，参数说明：-t tag 例：docker build -t youclk/my-ubuntu:v1 .。

> > Install :sudo apt-get -y install docker.io

> Other

> > docker image ls # 列出当前环境下的镜像

> > docker images   # 列出当前环境下的镜像

> > docker image rm ididididid      # 安装id删除镜像

> > 操作容器

> > docker run -i -t --rm centos /bin/bash   # 启动一个centos容器并进入，此时容器是干干净净，没有一点东西的，do everything

> > docker container kill container_id    # 杀掉这个容器，强行终止

> > docker container rm container_id      # 删除这个容器

> > docker container ls            # 查找当前容器

> > docker ps // 查看所有正在运行容器

> > docker stop containerId // containerId 是容器的ID

> > docker ps -a // 查看所有容器

> > docker ps -a -q // 查看所有容器ID

> > docker stop $(docker ps -a -q) //  stop停止所有容器

> > docker  rm $(docker ps -a -q) //   remove删除所有容器

### Kubernetes

> Kubernetes 也称为 K8s，是用于自动部署、扩缩和管理容器化应用程序的开源系统。

#### kubernetes 概述

> kubernetes 基本介绍

> > kubernetes，简称 K8s，是用 8 代替 8 个字符“ubernete”而成的缩写。是一个开源的，用于管理云平台中多个主机上的容器化的应用，Kubernetes 的目标是让部署容器化的应用简单并且高效（powerful）,Kubernetes 提供了应用部署，规划，更新，维护的一种机制。说白了，K8S，就是基于容器(Docker单机版)的集群管理平台,用于管理多个Docker的。Docker 非常适合在一台主机上运行容器，并为此提供所有必需的功能。但在当今的分布式服务环境中，真正的挑战是管理跨服务器和复杂基础架构的资源和工作负载。

> > Kubernetes 是 Google 开源的一个容器编排引擎，它支持自动化部署、大规模可伸缩、应用容器化管理。在生产环境中部署一个应用程序时，通常要部署该应用的多个实例以便对应用请求进行负载均衡。在 Kubernetes 中，我们可以创建多个容器，每个容器里面运行一个应用实例，然后通过内置的负载均衡策略，实现对这一组应用实例的管理、发现、访问，而这些细节都不需要运维人员去进行复杂的手工配置和处理。

> kubernetes 功能和架构

> > Kubernetes 是一个轻便的和可扩展的开源平台，用于管理容器化应用和服务。通过Kubernetes 能够进行应用的自动化部署和扩缩容。在 Kubernetes 中，会将组成应用的容器组合成一个逻辑单元以更易管理和发现。Kubernetes 积累了作为 Google 生产环境运行工作负载 15 年的经验，并吸收了来自于社区的最佳想法和实践。

> > K8s 功能(Kubernetes 适用场景):

> > > （1）自动装箱:基于容器对应用运行环境的资源配置要求自动部署应用容器

> > > （2）自我修复(自愈能力):当容器失败时，会对容器进行重启,当所部署的 Node 节点有问题时，会对容器进行重新部署和重新调度,当容器未通过监控检查时，会关闭此容器直到容器正常运行时，才会对外提供服务

> > > （3）水平扩展:通过简单的命令、用户 UI 界面或基于 CPU 等资源使用情况，对应用容器进行规模扩大或规模剪裁

> > > （3）服务发现:用户不需使用额外的服务发现机制，就能够基于 Kubernetes 自身能力实现服务发现和负载均衡

> > > （4）滚动更新:可以根据应用的变化，对应用容器运行的应用，进行一次性或批量式更新

> > > （5）版本回退:可以根据应用部署情况，对应用容器运行的应用，进行历史版本即时回退

> > > （6）密钥和配置管理:在不需要重新构建镜像的情况下，可以部署和更新密钥和应用配置，类似热部署。

> > > （7）存储编排:自动实现存储系统挂载及应用，特别对有状态应用实现数据持久化非常重要存储系统可以来自于本地目录、网络存储(NFS、Gluster、Ceph 等)、公共云存储服务

> > > （8）批处理:提供一次性任务，定时任务；满足批量数据处理和分析的场景

> > 应用部署架构分类

> > > (1) 无中心节点架构： GlusterFS

> > > (2) 有中心节点架构： HDFS、K8S

> > k8s 集群架构


> > > Pod

> > > > 一个服务，是k8s管理的`最小单元`，k8s从 Pod中启动和管理容器；

> > > > 由Pod来管理一组相同功能的容器；

> > > > 一个Pod可以管理一个容器,也可以管理多个容器；

> > k8s 集群架构节点角色功能



Master Node:集群主控制节点，对集群进行调度管理，接受集群外用户去集群操作请求；Master Node 由

API server (管理接口):是整个系统的对外接口，供客户端和其他组件调用，相当于“营业厅”
scheduler（调度器）:负责对集群内部的资源进行调度，相当于“调度室”
controller (控制器):负责管理控制器，相当于“大总管”。
etcd (键值对数据库):是一个键值存储仓库，存储集群的状态
Worker Node:集群工作节点，运行用户业务应用容器；Worker Node 包含 `
docker：容器管理
kubelet：主要负责监视指派到它所在的 Pod，包括创建、修改、监控、删除等。
kube-proxy：主要负责为Pod对象提供代理
其他附加服务

分布式键值存储服务
Etcd 服务
etcd是什么：

etcd 是 CoreOS 团队于 2013 年 6 月发起的开源项目，它的目标是构建一个高可用的分布式键值（key-value）数据库，基于 Go 语言实现。在分布式系统中，各种服务的配置信息的管理分享，服务的发现是一个很基本同时也是很重要的问题。CoreOS 项目就希望基于 etcd 来解决这一问题。
我们使用 etcd 来存储网络配置，解决容器互联互通的问题。


> > K8S核心概念：
通过Service统一入口进行访问，Controller用于创建Pot，Pot是一组容器的集合。

Pod:最小部署单元,一组容器的集合,共享网络,生命周期是短暂的
controller：确保预期的pod副本数量、无状态应用部署（无约定）、有状态应用部署(有特定条件)、确保所有的node运行同一个pod、一次性任务和定时任务
Service：定义一组pod的访问规则
搭建k8环境平台规划



服务器硬件配置要求搭建
测试环境：

master：2核+4G+20G
node：4核+8G+40G
生产环境：
Kubernetes 架构


核心角色
master (管理节点)
node（计算节点）
image (镜像仓库)
master 节点


master 节点服务
API server (管理接口)
scheduler（调度器）
controller (控制器)
etcd (键值对数据库)
Node 节点
node节点服务
docer
kubelet
kube-proxy

#### 核心概念

> 基础架构

> > Master

> > > Master节点上面主要由四个模块组成：APIServer、scheduler、controller manager、etcd。

> > > APIServer。APIServer负责对外提供RESTful的Kubernetes API服务，它是系统管理指令的统一入口，任何对资源进行增删改查的操作都要交给APIServer处理后再提交给etcd。如架构图中所示，kubectl（Kubernetes提供的客户端工具，该工具内部就是对Kubernetes API的调用）是直接和APIServer交互的。

> > > schedule。scheduler的职责很明确，就是负责调度pod到合适的Node上。如果把scheduler看成一个黑匣子，那么它的输入是pod和由多个Node组成的列表，输出是Pod和一个Node的绑定，即将这个pod部署到这个Node上。Kubernetes目前提供了调度算法，但是同样也保留了接口，用户可以根据自己的需求定义自己的调度算法。

> > > controller manager。如果说APIServer做的是“前台”的工作的话，那controller manager就是负责“后台”的。每个资源一般都对应有一个控制器，而controller manager就是负责管理这些控制器的。比如我们通过APIServer创建一个pod，当这个pod创建成功后，APIServer的任务就算完成了。而后面保证Pod的状态始终和我们预期的一样的重任就由controller manager去保证了。

> > > etcd。etcd是一个高可用的键值存储系统，Kubernetes使用它来存储各个资源的状态，从而实现了Restful的API。

> > Node

> > > 每个Node节点主要由三个模块组成：kubelet、kube-proxy、runtime。

> > > runtime。runtime指的是容器运行环境，目前Kubernetes支持docker和rkt两种容器。

> > > kube-proxy。该模块实现了Kubernetes中的服务发现和反向代理功能。反向代理方面：kube-proxy支持TCP和UDP连接转发，默认基于Round Robin算法将客户端流量转发到与service对应的一组后端pod。服务发现方面，kube-proxy使用etcd的watch机制，监控集群中service和endpoint对象数据的动态变化，并且维护一个service到endpoint的映射关系，从而保证了后端pod的IP变化不会对访问者造成影响。另外kube-proxy还支持session affinity。

> > > kubelet。Kubelet是Master在每个Node节点上面的agent，是Node节点上面最重要的模块，它负责维护和管理该Node上面的所有容器，但是如果容器不是通过Kubernetes创建的，它并不会管理。本质上，它负责使Pod得运行状态与期望的状态一致。

> > > 至此，Kubernetes的Master和Node就简单介绍完了。下面我们来看Kubernetes中的各种资源/对象。

> Pod

> > > Pod 是Kubernetes的基本操作单元，也是应用运行的载体。整个Kubernetes系统都是围绕着Pod展开的，比如如何部署运行Pod、如何保证Pod的数量、如何访问Pod等。另外，Pod是一个或多个机关容器的集合，这可以说是一大创新点，提供了一种容器的组合的模型。

> > 基本操作
 
> > > 创建

> > > > kubectl create -f xxx.yaml

> > > 查询

> > > > kubectl get pod yourPodName

> > > > kubectl describe pod yourPodName

> > > 删除

> > > > kubectl delete pod yourPodName

> > > 更新

> > > > kubectl replace /path/to/yourNewYaml.yaml

> > Pod与容器

> > > 在Docker中，容器是最小的处理单元，增删改查的对象是容器，容器是一种虚拟化技术，容器之间是隔离的，隔离是基于Linux Namespace实现的。而在Kubernetes中，Pod包含一个或者多个相关的容器，Pod可以认为是容器的一种延伸扩展，一个Pod也是一个隔离体，而Pod内部包含的一组容器又是共享的（包括PID、Network、IPC、UTS）。除此之外，Pod中的容器可以访问共同的数据卷来实现文件系统的共享。

> > 镜像

> > > 在kubernetes中，镜像的下载策略为：

> > > Always：每次都下载最新的镜像

> > > Never：只使用本地镜像，从不下载

> > > IfNotPresent：只有当本地没有的时候才下载镜像


> > > Pod被分配到Node之后会根据镜像下载策略进行镜像下载，可以根据自身集群的特点来决定采用何种下载策略。无论何种策略，都要确保Node上有正确的镜像可用。

> > 其他设置

> > > 通过yaml文件，可以在Pod中设置：

> > > 启动命令，如：spec-->containers-->command；

> > > 环境变量，如：spec-->containers-->env-->name/value；

> > > 端口桥接，如：spec-->containers-->ports-->containerPort/protocol/hostIP/hostPort（使用hostPort时需要注意端口冲突的问题，不过Kubernetes在调度Pod的时候会检查宿主机端口是否冲突，比如当两个Pod均要求绑定宿主机的80端口，Kubernetes将会将这两个Pod分别调度到不同的机器上）;

> > > Host网络，一些特殊场景下，容器必须要以host方式进行网络设置（如接收物理机网络才能够接收到的组播流），在Pod中也支持host网络的设置，如：spec-->hostNetwork=true；

> > > 数据持久化，如：spec-->containers-->volumeMounts-->mountPath;

> > > 重启策略，当Pod中的容器终止退出后，重启容器的策略。这里的所谓Pod的重启，实际上的做法是容器的重建，之前容器中的数据将会丢失，如果需要持久化数据，那么需要使用数据卷进行持久化设置。Pod支持三种重启策略：Always（默认策略，当容器终止退出后，总是重启容器）、OnFailure（当容器终止且异常退出时，重启）、Never（从不重启）；

> > Pod生命周期

> > > Pod被分配到一个Node上之后，就不会离开这个Node，直到被删除。当某个Pod失败，首先会被Kubernetes清理掉，之后ReplicationController将会在其它机器上（或本机）重建Pod，重建之后Pod的ID发生了变化，那将会是一个新的Pod。所以，Kubernetes中Pod的迁移，实际指的是在新Node上重建Pod。以下给出Pod的生命周期图。

> > > 生命周期回调函数：PostStart（容器创建成功后调研该回调函数）、PreStop（在容器被终止前调用该回调函数）。以下示例中，定义了一个Pod，包含一个JAVA的web应用容器，其中设置了PostStart和PreStop回调函数。即在容器创建成功后，复制/sample.war到/app文件夹中。而在容器终止之前，发送HTTP请求到http://monitor.com:8080/waring，即向监控系统发送警告。具体示例如下：

```
………..
containers:
- image: sample:v2  
     name: war
     lifecycle：
      posrStart:
       exec:
         command:
          - “cp”
          - “/sample.war”
          - “/app”
      prestop:
       httpGet:
        host: monitor.com
        psth: /waring
        port: 8080
        scheme: HTTP
```
 
> Replication Controller

> > > Replication Controller（RC）是Kubernetes中的另一个核心概念，应用托管在Kubernetes之后，Kubernetes需要保证应用能够持续运行，这是RC的工作内容，它会确保任何时间Kubernetes中都有指定数量的Pod在运行。在此基础上，RC还提供了一些更高级的特性，比如滚动升级、升级回滚等。

> > RC与Pod的关联——Label

> > > RC与Pod的关联是通过Label来实现的。Label机制是Kubernetes中的一个重要设计，通过Label进行对象的弱关联，可以灵活地进行分类和选择。对于Pod，需要设置其自身的Label来进行标识，Label是一系列的Key/value对，在Pod-->metadata-->labeks中进行设置。


> > > Label的定义是任一的，但是Label必须具有可标识性，比如设置Pod的应用名称和版本号等。另外Lable是不具有唯一性的，为了更准确的标识一个Pod，应该为Pod设置多个维度的label。如下：

> > > "release" : "stable", "release" : "canary"

> > > "environment" : "dev", "environment" : "qa", "environment" : "production"

> > > "tier" : "frontend", "tier" : "backend", "tier" : "cache"

> > > "partition" : "customerA", "partition" : "customerB"

> > > "track" : "daily", "track" : "weekly"


> > > 举例，当你在RC的yaml文件中定义了该RC的selector中的label为app:my-web，那么这个RC就会去关注Pod-->metadata-->labeks中label为app:my-web的Pod。修改了对应Pod的Label，就会使Pod脱离RC的控制。同样，在RC运行正常的时候，若试图继续创建同样Label的Pod，是创建不出来的。因为RC认为副本数已经正常了，再多起的话会被RC删掉的。

> > 弹性伸缩

> > > 弹性伸缩是指适应负载变化，以弹性可伸缩的方式提供资源。反映到Kubernetes中，指的是可根据负载的高低动态调整Pod的副本数量。调整Pod的副本数是通过修改RC中Pod的副本是来实现的，示例命令如下：


> > > 扩容Pod的副本数目到10

> > > > $ kubectl scale relicationcontroller yourRcName --replicas=10

> > > 缩容Pod的副本数目到1

> > > > $ kubectl scale relicationcontroller yourRcName --replicas=1
 
> > 滚动升级

> > > 滚动升级是一种平滑过渡的升级方式，通过逐步替换的策略，保证整体系统的稳定，在初始升级的时候就可以及时发现、调整问题，以保证问题影响度不会扩大。Kubernetes中滚动升级的命令如下：

$ kubectl rolling-update my-rcName-v1 -f my-rcName-v2-rc.yaml --update-period=10s

> > > 升级开始后，首先依据提供的定义文件创建V2版本的RC，然后每隔10s（--update-period=10s）逐步的增加V2版本的Pod副本数，逐步减少V1版本Pod的副本数。升级完成之后，删除V1版本的RC，保留V2版本的RC，及实现滚动升级。


> > > 升级过程中，发生了错误中途退出时，可以选择继续升级。Kubernetes能够智能的判断升级中断之前的状态，然后紧接着继续执行升级。当然，也可以进行回退，命令如下：

$ kubectl rolling-update my-rcName-v1 -f my-rcName-v2-rc.yaml --update-period=10s --rollback
回退的方式实际就是升级的逆操作，逐步增加V1.0版本Pod的副本数，逐步减少V2版本Pod的副本数。

> > 新一代副本控制器replica set

> > > 这里所说的replica set，可以被认为 是“升级版”的Replication Controller。也就是说。replica set也是用于保证与label selector匹配的pod数量维持在期望状态。区别在于，replica set引入了对基于子集的selector查询条件，而Replication Controller仅支持基于值相等的selecto条件查询。这是目前从用户角度肴，两者唯一的显著差异。 社区引入这一API的初衷是用于取代vl中的Replication Controller，也就是说．当v1版本被废弃时，Replication Controller就完成了它的历史使命，而由replica set来接管其工作。虽然replica set可以被单独使用，但是目前它多被Deployment用于进行pod的创建、更新与删除。Deployment在滚动更新等方面提供了很多非常有用的功能，关于DeplOymCn的更多信息，读者们可以在后续小节中获得。

 
> Job

> > > 从程序的运行形态上来区分，我们可以将Pod分为两类：长时运行服务（jboss、mysql等）和一次性任务（数据计算、测试）。RC创建的Pod都是长时运行的服务，而Job创建的Pod都是一次性任务。


> > > 在Job的定义中，restartPolicy（重启策略）只能是Never和OnFailure。Job可以控制一次性任务的Pod的完成次数（Job-->spec-->completions）和并发执行数（Job-->spec-->parallelism），当Pod成功执行指定次数后，即认为Job执行完毕。

 
> Service

> > > 为了适应快速的业务需求，微服务架构已经逐渐成为主流，微服务架构的应用需要有非常好的服务编排支持。Kubernetes中的核心要素Service便提供了一套简化的服务代理和发现机制，天然适应微服务架构。

> > 原理

> > > 在Kubernetes中，在受到RC调控的时候，Pod副本是变化的，对于的虚拟IP也是变化的，比如发生迁移或者伸缩的时候。这对于Pod的访问者来说是不可接受的。Kubernetes中的Service是一种抽象概念，它定义了一个Pod逻辑集合以及访问它们的策略，Service同Pod的关联同样是居于Label来完成的。Service的目标是提供一种桥梁， 它会为访问者提供一个固定访问地址，用于在访问时重定向到相应的后端，这使得非 Kubernetes原生应用程序，在无须为Kubemces编写特定代码的前提下，轻松访问后端。


> > > Service同RC一样，都是通过Label来关联Pod的。当你在Service的yaml文件中定义了该Service的selector中的label为app:my-web，那么这个Service会将Pod-->metadata-->labeks中label为app:my-web的Pod作为分发请求的后端。当Pod发生变化时（增加、减少、重建等），Service会及时更新。这样一来，Service就可以作为Pod的访问入口，起到代理服务器的作用，而对于访问者来说，通过Service进行访问，无需直接感知Pod。


> > > 需要注意的是，Kubernetes分配给Service的固定IP是一个虚拟IP，并不是一个真实的IP，在外部是无法寻址的。真实的系统实现上，Kubernetes是通过Kube-proxy组件来实现的虚拟IP路由及转发。所以在之前集群部署的环节上，我们在每个Node上均部署了Proxy这个组件，从而实现了Kubernetes层级的虚拟转发网络。

> > Service代理外部服务

> > > Service不仅可以代理Pod，还可以代理任意其他后端，比如运行在Kubernetes外部Mysql、Oracle等。这是通过定义两个同名的service和endPoints来实现的。示例如下：

> > > redis-service.yaml

```
apiVersion: v1
kind: Service
metadata:
  name: redis-service
spec:
  ports:
  - port: 6379
    targetPort: 6379
    protocol: TCP
```
> > > redis-endpoints.yaml

```
apiVersion: v1
kind: Endpoints
metadata:
  name: redis-service
subsets:
  - addresses:
    - ip: 10.0.251.145
    ports:
    - port: 6379
      protocol: TCP
```

> > > 基于文件创建完Service和Endpoints之后，在Kubernetes的Service中即可查询到自定义的Endpoints。

```
[root@k8s-master demon]# kubectl describe service redis-service
Name:            redis-service
Namespace:        default
Labels:            <none>
Selector:        <none>
Type:            ClusterIP
IP:            10.254.52.88
Port:            <unset>    6379/TCP
Endpoints:        10.0.251.145:6379
Session Affinity:    None
No events.
[root@k8s-master demon]# etcdctl get /skydns/sky/default/redis-service
{"host":"10.254.52.88","priority":10,"weight":10,"ttl":30,"targetstrip":0}
```

> > Service内部负载均衡

> > > 当Service的Endpoints包含多个IP的时候，及服务代理存在多个后端，将进行请求的负载均衡。默认的负载均衡策略是轮训或者随机（有kube-proxy的模式决定）。同时，Service上通过设置Service-->spec-->sessionAffinity=ClientIP，来实现基于源IP地址的会话保持。

> > 发布Service

> > > Service的虚拟IP是由Kubernetes虚拟出来的内部网络，外部是无法寻址到的。但是有些服务又需要被外部访问到，例如web前段。这时候就需要加一层网络转发，即外网到内网的转发。Kubernetes提供了NodePort、LoadBalancer、Ingress三种方式。

> > > NodePort，在之前的Guestbook示例中，已经延时了NodePort的用法。NodePort的原理是，Kubernetes会在每一个Node上暴露出一个端口：nodePort，外部网络可以通过（任一Node）[NodeIP]:[NodePort]访问到后端的Service。

> > > LoadBalancer，在NodePort基础上，Kubernetes可以请求底层云平台创建一个负载均衡器，将每个Node作为后端，进行服务分发。该模式需要底层云平台（例如GCE）支持。

> > > Ingress，是一种HTTP方式的路由转发机制，由Ingress Controller和HTTP代理服务器组合而成。Ingress Controller实时监控Kubernetes API，实时更新HTTP代理服务器的转发规则。HTTP代理服务器有GCE Load-Balancer、HaProxy、Nginx等开源方案。

> > servicede 自发性机制

> > > Kubernetes中有一个很重要的服务自发现特性。一旦一个service被创建，该service的service IP和service port等信息都可以被注入到pod中供它们使用。Kubernetes主要支持两种service发现 机制：环境变量和DNS。

> > 环境变量方式

> > > Kubernetes创建Pod时会自动添加所有可用的service环境变量到该Pod中，如有需要．这些环境变量就被注入Pod内的容器里。需要注意的是，环境变量的注入只发送在Pod创建时，且不会被自动更新。这个特点暗含了service和访问该service的Pod的创建时间的先后顺序，即任何想要访问service的pod都需要在service已经存在后创建，否则与service相关的环境变量就无法注入该Pod的容器中，这样先创建的容器就无法发现后创建的service。

> > DNS方式

> > > Kubernetes集群现在支持增加一个可选的组件——DNS服务器。这个DNS服务器使用Kubernetes的watchAPI，不间断的监测新的service的创建并为每个service新建一个DNS记录。如果DNS在整个集群范围内都可用，那么所有的Pod都能够自动解析service的域名。Kube-DNS搭建及更详细的介绍请见：基于Kubernetes集群部署skyDNS服务

> > 多个service如何避免地址和端口冲突

> > > 此处设计思想是，Kubernetes通过为每个service分配一个唯一的ClusterIP，所以当使用ClusterIP：port的组合访问一个service的时候，不管port是什么，这个组合是一定不会发生重复的。另一方面，kube-proxy为每个service真正打开的是一个绝对不会重复的随机端口，用户在service描述文件中指定的访问端口会被映射到这个随机端口上。这就是为什么用户可以在创建service时随意指定访问端口。

> > service目前存在的不足

> > > Kubernetes使用iptables和kube-proxy解析service的人口地址，在中小规模的集群中运行良好，但是当service的数量超过一定规模时，仍然有一些小问题。首当其冲的便是service环境变量泛滥，以及service与使用service的pod两者创建时间先后的制约关系。目前来看，很多使用者在使用Kubernetes时往往会开发一套自己的Router组件来替代service，以便更好地掌控和定制这部分功能。

 
> Deployment

> > > Kubernetes提供了一种更加简单的更新RC和Pod的机制，叫做Deployment。通过在Deployment中描述你所期望的集群状态，Deployment Controller会将现在的集群状态在一个可控的速度下逐步更新成你所期望的集群状态。Deployment主要职责同样是为了保证pod的数量和健康，90%的功能与Replication Controller完全一样，可以看做新一代的Replication Controller。但是，它又具备了Replication Controller之外的新特性：

> > > Replication Controller全部功能：Deployment继承了上面描述的Replication Controller全部功能。

> > > 事件和状态查看：可以查看Deployment的升级详细进度和状态。

> > > 回滚：当升级pod镜像或者相关参数的时候发现问题，可以使用回滚操作回滚到上一个稳定的版本或者指定的版本。

> > > 版本记录: 每一次对Deployment的操作，都能保存下来，给予后续可能的回滚使用。

> > > 暂停和启动：对于每一次升级，都能够随时暂停和启动。

> > > 多种升级方案：Recreate----删除所有已存在的pod,重新创建新的; RollingUpdate----滚动升级，逐步替换的策略，同时滚动升级时，支持更多的附加参数，例如设置最大不可用pod数量，最小升级间隔时间等等。

> > 滚动升级

> > > 相比于RC，Deployment直接使用kubectl edit deployment/deploymentName 或者kubectl set方法就可以直接升级（原理是Pod的template发生变化，例如更新label、更新镜像版本等操作会触发Deployment的滚动升级）。操作示例——首先 我们同样定义一个nginx-deploy-v1.yaml的文件，副本数量为2：

```
apiVersion: extensions/v1beta1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.7.9
        ports:
        - containerPort: 80
```

> > > 创建deployment：

```
$ kubectl create -f nginx-deploy-v1.yaml --record
deployment "nginx-deployment" created
$ kubectl get deployments
NAME       DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
nginx-deployment   3         0         0            0           1s
$ kubectl get deployments
NAME       DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
nginx-deployment   3         3         3            3           18s
```

> > > 正常之后，将nginx的版本进行升级，从1.7升级到1.9。第一种方法，直接set镜像：

$ kubectl set image deployment/nginx-deployment2 nginx=nginx:1.9
deployment "nginx-deployment2" image updated

> > > 第二种方法，直接edit：

> > > > $ kubectl edit deployment/nginx-deployment

> > > > deployment "nginx-deployment2" edited

> > > 查看Deployment的变更信息（以下信息得以保存，是创建时候加的“--record”这个选项起的作用）：

```
$ kubectl rollout history deployment/nginx-deployment
deployments "nginx-deployment":
REVISION    CHANGE-CAUSE
1           kubectl create -f docs/user-guide/nginx-deployment.yaml --record
2           kubectl set image deployment/nginx-deployment nginx=nginx:1.9.1
3           kubectl set image deployment/nginx-deployment nginx=nginx:1.91

$ kubectl rollout history deployment/nginx-deployment --revision=2
deployments "nginx-deployment" revision 2
  Labels:       app=nginx
          pod-template-hash=1159050644
  Annotations:  kubernetes.io/change-cause=kubectl set image deployment/nginx-deployment nginx=nginx:1.9.1
  Containers:
   nginx:
    Image:      nginx:1.9.1
    Port:       80/TCP
     QoS Tier:
        cpu:      BestEffort
        memory:   BestEffort
    Environment Variables:      <none>
  No volumes.
```

> > > 最后介绍下Deployment的一些基础命令。

> > > > $ kubectl describe deployments  #查询详细信息，获取升级进度

> > > > $ kubectl rollout pause deployment/nginx-deployment2  #暂停升级

> > > > $ kubectl rollout resume deployment/nginx-deployment2  #继续升级

> > > > $ kubectl rollout undo deployment/nginx-deployment2  #升级回滚

> > > > $ kubectl scale deployment nginx-deployment --replicas 10  #弹性伸缩Pod数量

> > > 关于多重升级，举例，当你创建了一个nginx1.7的Deployment，要求副本数量为5之后，Deployment Controller会逐步的将5个1.7的Pod启动起来；当启动到3个的时候，你又发出更新Deployment中Nginx到1.9的命令；这时Deployment Controller会立即将已启动的3个1.7Pod杀掉，然后逐步启动1.9的Pod。Deployment Controller不会等到1.7的Pod都启动完成之后，再依次杀掉1.7，启动1.9。

 

> Volume

> > 在Docker的设计实现中，容器中的数据是临时的，即当容器被销毁时，其中的数据将会丢失。如果需要持久化数据，需要使用Docker数据卷挂载宿主机上的文件或者目录到容器中。在Kubernetes中，当Pod重建的时候，数据是会丢失的，Kubernetes也是通过数据卷挂载来提供Pod数据的持久化的。Kubernetes数据卷是对Docker数据卷的扩展，Kubernetes数据卷是Pod级别的，可以用来实现Pod中容器的文件共享。目前，Kubernetes支持的数据卷类型如下：

> > > 1)        EmptyDir

> > > 2)        HostPath

> > > 3)        GCE Persistent Disk

> > > 4)        AWS Elastic Block Store

> > > 5)        NFS

> > > 6)        iSCSI

> > > 7)        Flocker

> > > 8)        GlusterFS

> > > 9)        RBD

> > > 10)    Git Repo

> > > 11)    Secret

> > > 12)    Persistent Volume Claim

> > > 13)    Downward API

> > 本地数据卷

> > > EmptyDir、HostPath这两种类型的数据卷，只能最用于本地文件系统。本地数据卷中的数据只会存在于一台机器上，所以当Pod发生迁移的时候，数据便会丢失。该类型Volume的用途是：Pod中容器间的文件共享、共享宿主机的文件系统。

> > > EmptyDir

> > > 如果Pod配置了EmpyDir数据卷，在Pod的生命周期内都会存在，当Pod被分配到 Node上的时候，会在Node上创建EmptyDir数据卷，并挂载到Pod的容器中。只要Pod 存在，EmpyDir数据卷都会存在（容器删除不会导致EmpyDir数据卷丟失数据），但是如果Pod的生命周期终结（Pod被删除），EmpyDir数据卷也会被删除，并且永久丢失。


> > > EmpyDir数据卷非常适合实现Pod中容器的文件共享。Pod的设计提供了一个很好的容器组合的模型，容器之间各司其职，通过共享文件目录来完成交互，比如可以通过一个专职日志收集容器，在每个Pod中和业务容器中进行组合，来完成日志的收集和汇总。

> > > HostPath

> > > HostPath数据卷允许将容器宿主机上的文件系统挂载到Pod中。如果Pod需要使用宿主机上的某些文件，可以使用HostPath。

> > 网络数据卷

> > > Kubernetes提供了很多类型的数据卷以集成第三方的存储系统，包括一些非常流行的分布式文件系统，也有在IaaS平台上提供的存储支持，这些存储系统都是分布式的，通过网络共享文件系统，因此我们称这一类数据卷为网络数据卷。


> > > 网络数据卷能够满足数据的持久化需求，Pod通过配置使用网络数据卷，每次Pod创建的时候都会将存储系统的远端文件目录挂载到容器中，数据卷中的数据将被水久保存，即使Pod被删除，只是除去挂载数据卷，数据卷中的数据仍然保存在存储系统中，且当新的Pod被创建的时候，仍是挂载同样的数据卷。网络数据卷包含以下几种：NFS、iSCISI、GlusterFS、RBD（Ceph Block Device）、Flocker、AWS Elastic Block Store、GCE Persistent Disk

> > Persistent Volume和Persistent Volume Claim

> > > 理解每个存储系统是一件复杂的事情，特别是对于普通用户来说，有时候并不需要关心各种存储实现，只希望能够安全可靠地存储数据。Kubernetes中提供了Persistent Volume和Persistent Volume Claim机制，这是存储消费模式。Persistent Volume是由系统管理员配置创建的一个数据卷（目前支持HostPath、GCE Persistent Disk、AWS Elastic Block Store、NFS、iSCSI、GlusterFS、RBD），它代表了某一类存储插件实现；而对于普通用户来说，通过Persistent Volume Claim可请求并获得合适的Persistent Volume，而无须感知后端的存储实现。Persistent Volume和Persistent Volume Claim的关系其实类似于Pod和Node，Pod消费Node资源，Persistent Volume Claim则消费Persistent Volume资源。Persistent Volume和Persistent Volume Claim相互关联，有着完整的生命周期管理：

> > > 1)        准备：系统管理员规划或创建一批Persistent Volume；

> > > 2)        绑定：用户通过创建Persistent Volume Claim来声明存储请求，Kubernetes发现有存储请求的时候，就去查找符合条件的Persistent Volume（最小满足策略）。找到合适的就绑定上，找不到就一直处于等待状态；

> > > 3)        使用：创建Pod的时候使用Persistent Volume Claim；

> > > 4)        释放：当用户删除绑定在Persistent Volume上的Persistent Volume Claim时，Persistent Volume进入释放状态，此时Persistent Volume中还残留着上一个Persistent Volume Claim的数据，状态还不可用；

> > > 5)        回收：是否的Persistent Volume需要回收才能再次使用。回收策略可以是人工的也可以是Kubernetes自动进行清理（仅支持NFS和HostPath）

> > 信息数据卷
　　
> > >Kubernetes中有一些数据卷，主要用来给容器传递配置信息，我们称之为信息数据卷，比如Secret（处理敏感配置信息，密码、Token等）、Downward API（通过环境变量的方式告诉容器Pod的信息）、Git Repo（将Git仓库下载到Pod中），都是将Pod的信息以文件形式保存，然后以数据卷方式挂载到容器中，容器通过读取文件获取相应的信息。

> Pet Sets/StatefulSet

> > K8s在1.3版本里发布了Alpha版的PetSet功能。在云原生应用的体系里，有下面两组近义词；第一组是无状态（stateless）、牲畜（cattle）、无名（nameless）、可丢弃（disposable）；第二组是有状态（stateful）、宠物（pet）、有名（having name）、不可丢弃（non-disposable）。RC和RS主要是控制提供无状态服务的，其所控制的Pod的名字是随机设置的，一个Pod出故障了就被丢弃掉，在另一个地方重启一个新的Pod，名字变了、名字和启动在哪儿都不重要，重要的只是Pod总数；而PetSet是用来控制有状态服务，PetSet中的每个Pod的名字都是事先确定的，不能更改。PetSet中Pod的名字的作用，是用来关联与该Pod对应的状态。

> > 对于RC和RS中的Pod，一般不挂载存储或者挂载共享存储，保存的是所有Pod共享的状态，Pod像牲畜一样没有分别；对于PetSet中的Pod，每个Pod挂载自己独立的存储，如果一个Pod出现故障，从其他节点启动一个同样名字的Pod，要挂在上原来Pod的存储继续以它的状态提供服务。

> > 适合于PetSet的业务包括数据库服务MySQL和PostgreSQL，集群化管理服务Zookeeper、etcd等有状态服务。PetSet的另一种典型应用场景是作为一种比普通容器更稳定可靠的模拟虚拟机的机制。传统的虚拟机正是一种有状态的宠物，运维人员需要不断地维护它，容器刚开始流行时，我们用容器来模拟虚拟机使用，所有状态都保存在容器里，而这已被证明是非常不安全、不可靠的。使用PetSet，Pod仍然可以通过漂移到不同节点提供高可用，而存储也可以通过外挂的存储来提供高可靠性，PetSet做的只是将确定的Pod与确定的存储关联起来保证状态的连续性。

> ConfigMap

> > 很多生产环境中的应用程序配置较为复杂，可能需要多个config文件、命令行参数和环境变量的组合。并且，这些配置信息应该从应用程序镜像中解耦出来，以保证镜像的可移植性以及配置信息不被泄露。社区引入ConfigMap这个API资源来满足这一需求。

> > ConfigMap包含了一系列的键值对，用于存储被Pod或者系统组件（如controller）访问的信息。这与secret的设计理念有异曲同工之妙，它们的主要区别在于ConfigMap通常不用于存储敏感信息，而只存储简单的文本信息。

> Horizontal Pod Autoscaler

> > 自动扩展作为一个长久的议题，一直为人们津津乐道。系统能够根据负载的变化对计算资源的分配进行自动的扩增或者收缩，无疑是一个非常吸引人的特征，它能够最大可能地减少费用或者其他代价（如电力损耗）。自动扩展主要分为两种，其一为水平扩展，针对于实例数目的增减；其二为垂直扩展，即单个实例可以使用的资源的增减。Horizontal Pod Autoscaler（HPA）属于前者。

> > Horizontal Pod Autoscaler如何工作

> > > Horizontal Pod Autoscaler的操作对象是Replication Controller、ReplicaSet或Deployment对应的Pod，根据观察到的CPU实际使用量与用户的期望值进行比对，做出是否需要增减实例数量的决策。controller目前使用heapSter来检测CPU使用量，检测周期默认是30秒。

> > Horizontal Pod Autoscaler的决策策略

> > > 在HPA Controller检测到CPU的实际使用量之后，会求出当前的CPU使用率（实际使用量与pod 请求量的比率)。然后，HPA Controller会通过调整副本数量使得CPU使用率尽量向期望值靠近．另外，考虑到自动扩展的决策可能需要一段时间才会生效，甚至在短时间内会引入一些噪声． 例如当pod所需要的CPU负荷过大，从而运行一个新的pod进行分流，在创建的过程中，系统的CPU使用量可能会有一个攀升的过程。所以，在每一次作出决策后的一段时间内，将不再进行扩展决策。对于ScaleUp而言，这个时间段为3分钟，Scaledown为5分钟。再者HPA Controller允许一定范围内的CPU使用量的不稳定，也就是说，只有当aVg（CurrentPodConsumption／Target低于0.9或者高于1.1时才进行实例调整，这也是出于维护系统稳定性的考虑。

#### kubernetes 集群搭建(kubeadm 方式)

2.搭建K8s集群--->kubeadm
2.1环境准备
2.1.1关闭防火墙
2.1.2关闭seliux
2.1.3关闭swap分区
2.1.4设置主机名称
2.1.5将桥接的IPv4流量传递到iptables的链
2.1.6时间同步
2.2三台虚拟机都安装Docker
2.3添加阿里云YUM软件源
2.4安装/kubeadm/kubelet
2.5部署Kubernetes Master
2.6加入Kubernetes Node
2.7 部署CNI网络插件
2.8 测试kubernetes集群


> 目前生产部署 Kubernetes 集群主要有两种方式：

（1）kubeadm
Kubeadm 是一个K8s 部署工具，提供kubeadm init和 kubeadm join，用于快速部署 Kubernetes 集群。官方地址
（2）二进制包
从 github 下载发行版的二进制包，手动部署每个组件，组成 Kubernetes 集群。
Kubeadm 降低部署门槛，但屏蔽了很多细节，遇到问题很难排查。如果想更容易可
控，推荐使用二进制包部署 Kubernetes 集群，虽然手动部署麻烦点，期间可以学习很
多工作原理，也利于后期维护。
kubeadm 部署方式介绍
kubeadm 是官方社区推出的一个用于快速部署 kubernetes 集群的工具，这个工具能通过两条指令完成一个 kubernetes 集群的部署：

第一、创建一个 Master 节点 kubeadm init
第二， 将 Node节点加入到当前集群中 $ kubeadm join <Master 节点的 IP 和端口 >
安装要求
在开始之前，部署 Kubernetes 集群机器需要满足以下几个条件：

一台或多台机器，操作系统 CentOS7.x-86_x64
硬件配置：2GB 或更多 RAM，2 个 CPU 或更多 CPU，硬盘 30GB 或更多
集群中所有机器之间网络互通
可以访问外网，需要拉取镜像
禁止 swap 分区
最终目标
角色	IP
k8s-master	192.168.31.61
k8s-node1	192.168.31.62
k8s-node2	192.168.31.63


> 系统初始化

> > 关闭防火墙：

```
$ systemctl stop firewalld
$ systemctl disable firewalld
```

> > 关闭 selinux：

```
$ sed -i 's/enforcing/disabled/' /etc/selinux/config # 永久
$ setenforce 0 # 临时
```

> > swap：

```
$ swapoff -a # 临时
$ vim /etc/fstab # 永久
```

> > 主机名：

```
$ hostnamectl set-hostname <hostname>
```

> > 在 master 添加 hosts：

```
$ cat >> /etc/hosts << EOF
192.168.31.61 k8s-master
192.168.31.62 k8s-node1
192.168.31.63 k8s-node2
EOF
```

> > 将桥接的 IPv4 流量传递到 iptables 的链：

```
$ cat > /etc/sysctl.d/k8s.conf << EOF
net.bridge.bridge-nf-call-ip6tables = 1
net.bridge.bridge-nf-call-iptables = 1
EOF
$ sysctl --system # 生效
```

> > 时间同步：

```
$ yum install ntpdate -y
$ ntpdate time.windows.com
```

> 所有节点安装 Docker/kubeadm/kubelet

> > Kubernetes 默认 CRI（容器运行时）为 Docker，因此先安装 Docker。

> > （1）安装 Docker

```
$ wget https://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo -O /etc/yum.repos.d/docker-ce.repo
$ yum -y install docker-ce-18.06.1.ce-3.el7
$ systemctl enable docker && systemctl start docker
$ docker --version
```

> > 添加阿里云 YUM 软件源
> > 设置仓库地址

```
$ cat > /etc/docker/daemon.json << EOF
{
"registry-mirrors": ["https://b9pmyelo.mirror.aliyuncs.com"]
}
EOF
```

> > 添加 yum 源

```
$ cat > /etc/yum.repos.d/kubernetes.repo << EOF
[kubernetes]
name=Kubernetes
baseurl=https://mirrors.aliyun.com/kubernetes/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=0
repo_gpgcheck=0
gpgkey=https://mirrors.aliyun.com/kubernetes/yum/doc/yum-key.gpg
https://mirrors.aliyun.com/kubernetes/yum/doc/rpm-package-key.gpg
EOF
```

> > 安装 kubeadm，kubelet 和 kubectl

```
$ yum install -y kubelet kubeadm kubectl
$ systemctl enable kubelet
```

> 部署 Kubernetes Master

> > 在 192.168.31.61（Master）执行

```
$ kubeadm init \
--apiserver-advertise-address=192.168.31.61 \
--image-repository registry.aliyuncs.com/google_containers \
--kubernetes-version v1.17.0 \
--service-cidr=10.96.0.0/12 \
--pod-network-cidr=10.244.0.0/16
```
> > 由于默认拉取镜像地址 k8s.gcr.io 国内无法访问，这里指定阿里云镜像仓库地址。

> > 使用 kubectl 工具：

```
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
$ kubectl get nodes
```

> 安装 Pod 网络插件（CNI）

```
$ kubectl apply –f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kubeflannel.yml
```

> > 检查一下

```
kubect1 get pods -n kube-system
```

> > 确保能够访问到 quay.io 这个 registery。如果 Pod 镜像下载失败，可以改这个镜像地址

> 加入 Kubernetes Node

> > 在 192.168.31.62/63（Node）执行

> > 向集群添加新节点，执行在 kubeadm init 输出的 kubeadm join 命令：

```
$ kubeadm join 192.168.31.61:6443 --token esce21.q6hetwm8si29qxwn \
--discovery-token-ca-cert-hash
sha256:00603a05805807501d7181c3d60b478788408cfe6cedefedb1f97569708be9c5
```

> 测试 kubernetes 集群

> > 在 Kubernetes 集群中创建一个 pod，验证是否正常运行：

```
$ kubectl create deployment nginx --image=nginx
$ kubectl expose deployment nginx --port=80 --type=NodePort
$ kubectl get pod,svc
```

> > 访问地址：http://NodeIP:Port

#### 安装方法二

> 安装三台虚拟机，centos7

> 对三台操作系统进行初始化

> > 关闭防火墙

```
systemctl status firewalld //查看防火墙状态
systemctl stop firewalld //关闭防火墙
systemctl disable firewalld //开机不启动防火墙
```

> > 关闭seliux

```
 getenforce
 sed -ri 's/SELINUX=enforcing/SELINUX=disabled/' /etc/selinux/config
```

> > 关闭swap分区

```
swapoff -a # 临时关闭
sed -ri 's/.*swap.*/#&/' /etc/fstab    # 永久
```

> > 设置主机名称

> > > 根据规划设置主机名

```
hostnamectl set-hostname <hostname>
```

> > > 在master添加hosts

```
cat >> /etc/hosts << EOF
192.168.26.128 k8smaster
192.168.26.129 k8snode1
192.168.26.130 k8snode2
EOF
```

> > 将桥接的IPv4流量传递到iptables的链

```
cat > /etc/sysctl.d/k8s.conf << EOF
net.bridge.bridge-nf-call-ip6tables = 1
net.bridge.bridge-nf-call-iptables = 1
EOF
sysctl --system  # 生效
```

> > 时间同步

```
yum install ntpdate -y
ntpdate time.windows.com
```

> 三台虚拟机都安装Docker

```
yum -y install wget


$ wget https://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo -O /etc/yum.repos.d/docker-ce.repo
$ yum -y install docker-ce-18.06.1.ce-3.el7
$ systemctl enable docker && systemctl start docker
$ docker --version
Docker version 18.06.1-ce, build e68fc7a


$ cat > /etc/docker/daemon.json << EOF
{
  "registry-mirrors": ["https://b9pmyelo.mirror.aliyuncs.com"]
}
EOF

systemctl restart docker
```

> 添加阿里云YUM软件源

```
$ cat > /etc/yum.repos.d/kubernetes.repo << EOF
[kubernetes]
name=Kubernetes
baseurl=https://mirrors.aliyun.com/kubernetes/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=0
repo_gpgcheck=0
gpgkey=https://mirrors.aliyun.com/kubernetes/yum/doc/yum-key.gpg https://mirrors.aliyun.com/kubernetes/yum/doc/rpm-package-key.gpg
EOF
```

> 安装/kubeadm/kubelet

> > 由于版本更新频繁，这里指定版本号部署：

```
$ yum install -y kubelet-1.18.0 kubeadm-1.18.0 kubectl-1.18.0
$ systemctl enable kubelet
```

> 部署Kubernetes Master

> > 在192.168.26.128（Master）执行。

```
$ kubeadm init \
  --apiserver-advertise-address=192.168.26.128 \
  --image-repository registry.aliyuncs.com/google_containers \
  --kubernetes-version v1.18.0 \
  --service-cidr=10.96.0.0/12 \
  --pod-network-cidr=10.244.0.0/16
```

> > 执行慢，稍作等待


> > 由于默认拉取镜像地址k8s.gcr.io国内无法访问，这里指定阿里云镜像仓库地址。

> > 使用kubectl工具：

```
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
$ kubectl get nodes
```

> 加入Kubernetes Node

> > 在（Node）服务器执行。

> > 向集群添加新节点，执行在kubeadm init输出的kubeadm join命令：

```
$ kubeadm join 192.168.1.11:6443 --token esce21.q6hetwm8si29qxwn \
    --discovery-token-ca-cert-hash sha256:00603a05805807501d7181c3d60b478788408cfe6cedefedb1f97569708be9c5
```

> > 默认token有效期为24小时，当过期之后，该token就不可用了。这时就需要重新创建token，操作如下：

> > kubeadm token create --print-join-command


> 部署CNI网络插件

> > wget https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml

> > 默认镜像地址无法访问，sed命令修改为docker hub镜像仓库。可以换源下载

```
kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml

kubectl get pods -n kube-system

NAME                          READY   STATUS    RESTARTS   AGE
kube-flannel-ds-amd64-2pc95   1/1     Running   0          72s
```

> 测试kubernetes集群

> > 在Kubernetes集群中创建一个pod，验证是否正常运行：

```
$ kubectl create deployment nginx --image=nginx
$ kubectl expose deployment nginx --port=80 --type=NodePort
$ kubectl get pod,svc
```

> > 访问地址：http://NodeIP:Port

```
http://192.168.26.128:30340/
```

#### kubernetes 集群搭建（二进制）

> 安装要求

> 准备环境、操作系统初始化

> 为etcd和apiserver准备自签证书（△）

> > 准备 cfssl 证书生成工具

> > > cfssl 是一个开源的证书管理工具， 使用 json 文件生成证书， 相比 openssl 更方便使用。找任意一台服务器操作， 这里用 Master 节点。

```
wget https://pkg.cfssl.org/R1.2/cfssl_linux-amd64
wget https://pkg.cfssl.org/R1.2/cfssljson_linux-amd64
wget https://pkg.cfssl.org/R1.2/cfssl-certinfo_linux-amd64
chmod +x cfssl_linux-amd64 cfssljson_linux-amd64 cfssl-certinfo_linux-amd64
mv cfssl_linux-amd64 /usr/local/bin/cfssl
mv cfssljson_linux-amd64 /usr/local/bin/cfssljson
mv cfssl-certinfo_linux-amd64 /usr/bin/cfssl-certinfo
```

> > 生成 Etcd 证书

> > > 自签证书颁发机构（ CA）

> > > 创建工作目录：

```
mkdir -p ~/TLS/{etcd,k8s}
cd TLS/etcd
```

> > > 自签 CA：

```
cat > ca-config.json<< EOF
	{
	"signing": {
	"default": {
		"expiry": "87600h"
	},
	"profiles": {
	"www": {
		"expiry": "87600h",
		"usages": [
			"signing",
			"key encipherment",
			"server auth",
			"client auth"
		]
	}
	}
}
} EOF

cat > ca-csr.json<< EOF
{
	"CN": "etcd CA",
	"key": {
	"algo": "rsa",
	"size": 2048
	},
	"names": [
		{
		"C": "CN",
		"L": "Beijing",
		"ST": "Beijing"
		}
	]
} EOF
```

> > > 生成证书：

```
cfssl gencert -initca ca-csr.json | cfssljson -bare ca -
ls *pem
ca-key.pem ca.pem
```

> > > 使用自签 CA 签发 Etcd HTTPS 证书

> > > 创建证书申请文件：

```
cat > server-csr.json<< EOF
{
	"CN": "etcd",
	"hosts": [
		"192.168.31.71",
		"192.168.31.72",
		"192.168.31.73"
	],
	"key": {
		"algo": "rsa",
		"size": 2048
	},
	"names": [
		{
			"C": "CN",
			"L": "BeiJing",
			"ST": "BeiJing"
		}
	]
} EOF
```

> > > 注： 上述文件 hosts 字段中 IP 为所有 etcd 节点的集群内部通信 IP， 一个都不能少！ 为了方便后期扩容可以多写几个预留的 IP。

> > > 生成证书：

```
cfssl gencert -ca=ca.pem -ca-key=ca-key.pem -config=ca-config.json -
profile=www server-csr.json | cfssljson -bare server
ls server*pem
server-key.pem server.pem
```

> > 从 Github 下载二进制文件

> > > 下载地址： https://github.com/etcd-io/etcd/releases/download/v3.4.9/etcd-v3.4.9-linux-amd64.tar.gz


> 部署Etcd集群（△）

> > Etcd 是一个分布式键值存储系统， Kubernetes 使用 Etcd 进行数据存储， 所以先准备一个 Etcd 数据库， 为解决 Etcd 单点故障， 应采用集群方式部署， 这里使用 3 台组建集群， 可容忍 1 台机器故障， 当然， 你也可以使用 5 台组建集群， 可容忍 2 台机器故障。


> > > 创建工作目录并解压二进制包

```
mkdir /opt/etcd/{bin,cfg,ssl} – p
tar zxvf etcd-v3.4.9-linux-amd64.tar.gz
mv etcd-v3.4.9-linux-amd64/{etcd,etcdctl} /opt/etcd/bin/
```

> > > 创建 etcd 配置文件

```
cat > /opt/etcd/cfg/etcd.conf << EOF
#[Member]
	ETCD_NAME="etcd-1"
	ETCD_DATA_DIR="/var/lib/etcd/default.etcd"
	ETCD_LISTEN_PEER_URLS="https://192.168.31.71:2380"
	ETCD_LISTEN_CLIENT_URLS="https://192.168.31.71:2379"
	#[Clustering]
	ETCD_INITIAL_ADVERTISE_PEER_URLS="https://192.168.31.71:2380"
	ETCD_ADVERTISE_CLIENT_URLS="https://192.168.31.71:2379"
	ETCD_INITIAL_CLUSTER="etcd-1=https://192.168.31.71:2380,etcd-
	2=https://192.168.31.72:2380,etcd-3=https://192.168.31.73:2380"
	ETCD_INITIAL_CLUSTER_TOKEN="etcd-cluster"
	ETCD_INITIAL_CLUSTER_STATE="new"
EOF

ETCD_NAME： 节点名称， 集群中唯一
ETCD_DATA_DIR： 数据目录
ETCD_LISTEN_PEER_URLS： 集群通信监听地址
ETCD_LISTEN_CLIENT_URLS： 客户端访问监听地址
ETCD_INITIAL_ADVERTISE_PEER_URLS： 集群通告地址
ETCD_ADVERTISE_CLIENT_URLS： 客户端通告地址
ETCD_INITIAL_CLUSTER： 集群节点地址
ETCD_INITIAL_CLUSTER_TOKEN： 集群 Token
ETCD_INITIAL_CLUSTER_STATE： 加入集群的当前状态， new 是新集群， existing 表示加入已有集群
```

> > > systemd 管理 etcd

```
cat > /usr/lib/systemd/system/etcd.service << EOF
[Unit]
	Description=Etcd Server
	After=network.target
	After=network-online.target
	Wants=network-online.target
	[Service]
	Type=notify
	EnvironmentFile=/opt/etcd/cfg/etcd.conf
	ExecStart=/opt/etcd/bin/etcd \
	--cert-file=/opt/etcd/ssl/server.pem \
	--key-file=/opt/etcd/ssl/server-key.pem \
	--peer-cert-file=/opt/etcd/ssl/server.pem \
	--peer-key-file=/opt/etcd/ssl/server-key.pem \
	--trusted-ca-file=/opt/etcd/ssl/ca.pem \
	--peer-trusted-ca-file=/opt/etcd/ssl/ca.pem \
	--logger=zap
	Restart=on-failure
	LimitNOFILE=65536
	[Install]
	WantedBy=multi-user.target
EOF
```

> > > 拷贝刚才生成的证书把刚才生成的证书拷贝到配置文件中的路径：

```
cp ~/TLS/etcd/ca*pem ~/TLS/etcd/server*pem /opt/etcd/ssl/
```

> > > 启动并设置开机启动

```
systemctl daemon-reload
systemctl start etcd
systemctl enable etcd
```

> > > 将上面节点 1 所有生成的文件拷贝到节点 2 和节点 3

```
scp -r /opt/etcd/ root@192.168.31.72:/opt/
scp /usr/lib/systemd/system/etcd.service
root@192.168.31.72:/usr/lib/systemd/system/
scp -r /opt/etcd/ root@192.168.31.73:/opt/
scp /usr/lib/systemd/system/etcd.service
root@192.168.31.73:/usr/lib/systemd/system/
```

> > > 然后在节点 2 和节点 3 分别修改 etcd.conf 配置文件中的节点名称和当前服务器 IP：

```
vi /opt/etcd/cfg/etcd.conf
#[Member]
ETCD_NAME="etcd-1" # 修改此处， 节点 2 改为 etcd-2， 节点 3 改为 etcd-3
ETCD_DATA_DIR="/var/lib/etcd/default.etcd"
ETCD_LISTEN_PEER_URLS="https://192.168.31.71:2380" # 修改此处为当前服务器 IP
ETCD_LISTEN_CLIENT_URLS="https://192.168.31.71:2379" # 修改此处为当前服务器 IP
#[Clustering]
ETCD_INITIAL_ADVERTISE_PEER_URLS="https://192.168.31.71:2380" # 修改此处为当前
服务器 IP
ETCD_ADVERTISE_CLIENT_URLS="https://192.168.31.71:2379" # 修改此处为当前服务器
IP
ETCD_INITIAL_CLUSTER="etcd-1=https://192.168.31.71:2380,etcd-
2=https://192.168.31.72:2380,etcd-3=https://192.168.31.73:2380"
ETCD_INITIAL_CLUSTER_TOKEN="etcd-cluster"
ETCD_INITIAL_CLUSTER_STATE="new"
```

> > > 最后启动 etcd 并设置开机启动， 同上。

> > > 查看集群状态

```
ETCDCTL_API=3 /opt/etcd/bin/etcdctl --cacert=/opt/etcd/ssl/ca.pem --
cert=/opt/etcd/ssl/server.pem --key=/opt/etcd/ssl/server-key.pem --
endpoints="https://192.168.31.71:2379,https://192.168.31.72:2379,https://192.16
8.31.73:2379" endpoint health
https://192.168.31.71:2379 is healthy: successfully committed proposal: took =
8.154404ms
https://192.168.31.73:2379 is healthy: successfully committed proposal: took =
9.044117ms
https://192.168.31.72:2379 is healthy: successfully committed proposal: took =
10.000825ms
```

> > > 如果输出上面信息， 就说明集群部署成功。 如果有问题第一步先看日志：

```
/var/log/message 或 journalctl -u etcd
```

> 安装Docker

> > systemd 管理 docker

```
cat > /usr/lib/systemd/system/docker.service << EOF
[Unit]
Description=Docker Application Container Engine
Documentation=https://docs.docker.com
After=network-online.target firewalld.service
Wants=network-online.target
[Service]
Type=notify
ExecStart=/usr/bin/dockerd
ExecReload=/bin/kill -s HUP $MAINPID
LimitNOFILE=infinity
LimitNPROC=infinity
LimitCORE=infinity
TimeoutStartSec=0
Delegate=yes
KillMode=process
Restart=on-failure
StartLimitBurst=3
StartLimitInterval=60s
[Install]
WantedBy=multi-user.target
EOF
```

> > 创建配置文件

```
mkdir /etc/docker
cat > /etc/docker/daemon.json << EOF
{"registry-mirrors": ["https://b9pmyelo.mirror.aliyuncs.com"]
} EOF
```

> > > registry-mirrors 阿里云镜像加速器

> 部署Master Node

> 部署Worker Node

> 部署集群网络

#### kubernetes 集群 YAML 文件详解

1、YAML 文件概述
k8s 集群中对资源管理和资源对象编排部署都可以通过声明样式（YAML）文件来解决，也就是可以把需要对资源对象操作编辑到 YAML 格式文件中，我们把这种文件叫做资源清单文件，通过 kubectl 命令直接使用资源清单文件就可以实现对大量的资源对象进行编排部署了。

3、资源清单描述方法
（1）在 k8s 中，一般使用 YAML 格式的文件来创建符合我们预期期望的 pod,这样的 YAML文件称为资源清单。

必须存在的属性（必须写）
参数名	字段类型	说明	默认值
apiVersion	String	这里是指的是K8S API的版本，目前基本上是v1，可以用 kubectl api-versions 或者 kubectl explain pod 命令查询	
kind	String	这里指的是yaml文件定义的资源类型和角色，比如: Pod	
metadata	Object	元数据对象，固定值就写metadata	
metadata.name	String	元数据对象的名字，这里由我们编写，比如命名Pod的名字	
metadata.namespace	String	元数据对象的命名空间，由我们自身定义	default
metadata.labels	map[string]string	键值数据，常被用作挑选条件	
spec	Object 详细定义对象，固定值就写Spec		
spec.containers[]		List	这里是Spec对象的容器列表定义，是个列表
spec.containers[].name	String	这里定义容器的名字	
spec.containers[].image	String	这里定义要用到的镜像名称，如果镜像的标签是 latest，每次使用该镜像都会从远程下载	

## 结构化程序设计

## 面向对象程序设计

## C# .Net Base 

第1部分CLR基础
第1章CLR的执行模型
第2章生成、打包、部署和管理应用程序及类型
第3章共享程序集和强命名程序集
第2部分设计类型
第4章类型基础
第5章基元类型、引用类型和值类型
第6章类型和成员基础
第7章常量和字段
第8章方法
第9章参数
第10章属性
第11章事件
第12章泛型
第13章接口
第3部分基本类型
第14章字符、字符串和文本处理
第15章枚举类型和位标志
第16章数组
第17章委托
第18章定制特性
第19章可空值类型
第4部分核心机制
第20章异常和状态管理
第21章托管堆和垃圾回收
第22章CLR寄宿和AppDomain
第23章程序集加载和反射
第24章运行时序列化
第25章与WinRT组件互操作
第5部分线程处理
第26章线程基础
第27章计算的异步操作
第28章I/O的异步操作
第29章基元线程同步构造
第30章混合线程同步构造

### ML.NET

> 微软人工智能学习

## WPF

第Ⅰ部分 基础知识
第1章 WPF概述 3
1.1 Windows图形演化 3
1.1.1 DirectX：新的图形引擎 4
1.1.2 硬件加速与WPF 4
1.2 WPF：高级API 4
1.3 分辨率无关性 5
1.3.1 WPF单位 6
1.3.2 系统DPI 7
1.3.3 位图和矢量图形 9
1.4 WPF体系结构 10
1.5 WPF 4.5 13
1.5.1 WPF工具包 14
1.5.2 Visual Studio 2012 14
1.6 小结 16
第2章 XAML 17
2.1 理解XAML 17
2.1.1 WPF之前的图形用户界面 17
2.1.2 XAML变体 19
2.1.3 XAML编译 19
2.2 XAML基础 20
2.2.1 XAML名称空间 21
2.2.2 代码隐藏类 22
2.3 XAML中的属性和事件 24
2.3.1 简单属性与类型转换器 25
2.3.2 复杂属性 26
2.3.3 标记扩展 28
2.3.4 附加属性 29
2.3.5 嵌套元素 30
2.3.6 特殊字符与空白 32
2.3.7 事件 34
2.3.8 完整的Eight Ball Answer示例 35
2.4 使用其他名称空间中的类型 36
2.5 加载和编译XAML 38
2.5.1 只使用代码 38
2.5.2 使用代码和未经编译的XAML 40
2.5.3 使用代码和编译过的XAML 42
2.5.4 只使用XAML 44
2.6 小结 45
第3章 布局 47
3.1 理解WPF中的布局 47
3.1.1 WPF布局原则 47
3.1.2 布局过程 48
3.1.3 布局容器 48
3.2 使用StackPanel面板进行简单
布局 50
3.2.1 布局属性 52
3.2.2 对齐方式 52
3.2.3 边距 53
3.2.4 小尺寸、尺寸以及显式地
设置尺寸 54
3.2.5 Border控件 56
3.3 WrapPanel和DockPanel面板 57
3.3.1 WrapPanel面板 57
3.3.2 DockPanel面板 58
3.3.3 嵌套布局容器 59
3.4 Grid面板 60
3.4.1 调整行和列 63
3.4.2 布局舍入 64
3.4.3 跨越行和列 65
3.4.4 分割窗口 66
3.4.5 共享尺寸组 69
3.4.6 UniformGrid面板 72
3.5 使用Canvas面板进行基于
坐标的布局 72
3.5.1 Z顺序 73
3.5.2 lnkCanvas元素 74
3.6 布局示例 76
3.6.1 列设置 76
3.6.2 动态内容 77
3.6.3 组合式用户界面 79
3.7 小结 80
第4章 依赖项属性 83
4.1 理解依赖项属性 83
4.1.1 定义依赖项属性 84
4.1.2 注册依赖项属性 84
4.1.3 添加属性包装器 86
4.1.4 WPF使用依赖项属性的方式 87
4.1.5 共享的依赖项属性 88
4.1.6 附加的依赖项属性 88
4.2 属性验证 90
4.2.1 验证回调 90
4.2.2 强制回调 91
4.3 小结 93
第5章 路由事件 95
5.1 理解路由事件 95
5.1.1 定义、注册和封装路由事件 95
5.1.2 共享路由事件 96
5.1.3 引发路由事件 96
5.1.4 处理路由事件 97
5.2 事件路由 99
5.2.1 RoutedEventArgs类 100
5.2.2 冒泡路由事件 100
5.2.3 处理挂起的事件 103
5.2.4 附加事件 103
5.2.5 隧道路由事件 105
5.3 WPF事件 106
5.3.1 生命周期事件 106
5.3.2 输入事件 108
5.4 键盘输入 108
5.4.1 处理按键事件 109
5.4.2 焦点 111
5.4.3 获取键盘状态 112
5.5 鼠标输入 113
5.5.1 鼠标单击 115
5.5.2 捕获鼠标 115
5.5.3 鼠标拖放 116
5.6 多点触控输入 118
5.6.1 多点触控的输入层次 119
5.6.2 原始触控 119
5.6.3 操作 122
5.6.4 惯性 124
5.7 小结 125
第Ⅱ部分 进一步研究WPF
第6章 控件 129
6.1 控件类 129
6.1.1 背景画刷和前景画刷 130
6.1.2 字体 132
6.1.3 鼠标光标 136
6.2 内容控件 137
6.2.1 Content属性 138
6.2.2 对齐内容 140
6.2.3 WPF内容原则 141
6.2.4 标签 142
6.2.5 按钮 142
6.2.6 工具提示 145
6.3 特殊容器 151
6.3.1 ScrollViewer 152
6.3.2 GroupBox 154
6.3.3 TabItem 154
6.3.4 Expander 155
6.4 文本控件 158
6.4.1 多行文本 158
6.4.2 选择文本 159
6.4.3 拼写检查 160
6.4.4 PasswordBox 162
6.5 列表控件 162
6.5.1 ListBox 163
6.5.2 ComboBox 166
6.6 基于范围的控件 166
6.6.1 Slider 167
6.6.2 ProgressBar 168
6.7 日期控件 169
6.8 小结 171
第7章 Application类 173
7.1 应用程序的生命周期 173
7.1.1 创建Application对象 173
7.1.2 派生自定义的Application类 174
7.1.3 应用程序的关闭方式 176
7.1.4 应用程序事件 177
7.2 Application类的任务 179
7.2.1 显示初始界面 179
7.2.2 处理命令行参数 180
7.2.3 访问当前Application对象 181
7.2.4 在窗口之间进行交互 182
7.2.5 单实例应用程序 184
7.3 程序集资源 189
7.3.1 添加资源 189
7.3.2 检索资源 190
7.3.3 pack URI 192
7.3.4 内容文件 193
7.4 本地化 193
7.4.1 构建能够本地化的用户界面 194
7.4.2 使应用程序为本地化做好准备 194
7.4.3 管理翻译过程 195
7.5 小结 200
第8章 元素绑定 201
8.1 将元素绑定到一起 201
8.1.1 绑定表达式 202
8.1.2 绑定错误 203
8.1.3 绑定模式 203
8.1.4 使用代码创建绑定 205
8.1.5 使用代码检索绑定 206
8.1.6 多绑定 207
8.1.7 绑定更新 210
8.1.8 绑定延迟 211
8.2 绑定到非元素对象 211
8.2.1 Source属性 212
8.2.2 RelativeSource属性 212
8.2.3 DataContext属性 213
8.3 小结 214
第9章 命令 215
9.1 理解命令 215
9.2 WPF命令模型 216
9.2.1 ICommand接口 217
9.2.2 RoutedCommand类 217
9.2.3 RoutedUICommand类 218
9.2.4 命令库 219
9.3 执行命令 220
9.3.1 命令源 220
9.3.2 命令绑定 221
9.3.3 使用多命令源 223
9.3.4 微调命令文本 224
9.3.5 直接调用命令 224
9.3.6 禁用命令 225
9.3.7 具有内置命令的控件 227
9.4 高级命令 229
9.4.1 自定义命令 229
9.4.2 在不同位置使用相同的命令 230
9.4.3 使用命令参数 232
9.4.4 跟踪和翻转命令 233
9.5 小结 237
第10章 资源 239
10.1 资源基础 239
10.1.1 资源集合 239
10.1.2 资源的层次 241
10.1.3 静态资源和动态资源 242
10.1.4 非共享资源 243
10.1.5 通过代码访问资源 244
10.1.6 应用程序资源 244
10.1.7 系统资源 245
10.2 资源字典 246
10.2.1 创建资源字典 246
10.2.2 使用资源字典 247
10.2.3 在程序集之间共享资源 248
10.3 小结 251
第11章 样式和行为 253
11.1 样式基础 253
11.1.1 创建样式对象 256
11.1.2 设置属性 257
11.1.3 关联事件处理程序 258
11.1.4 多层样式 259
11.1.5 通过类型自动应用样式 261
11.2 触发器 262
11.2.1 简单触发器 262
11.2.2 事件触发器 264
11.3 行为 266
11.3.1 获取行为支持 266
11.3.2 理解行为模型 267
11.3.3 创建行为 268
11.3.4 使用行为 270
11.3.5 Blend中的设计时行为支持 271
11.4 小结 271
第Ⅲ部分 图画和动画
第12章 形状、画刷和变换 275
12.1 理解形状 275
12.1.1 Shape类 276
12.1.2 矩形和椭圆 277
12.1.3 改变形状的尺寸和放置形状 278
12.1.4 使用Viewbox控件缩放形状 280
12.1.5 直线 282
12.1.6 折线 283
12.1.7 多边形 284
12.1.8 直线线帽和直线交点 286
12.1.9 点划线 287
12.1.10 像素对齐 288
12.2 画刷 289
12.2.1 SolidColorBrush画刷 290
12.2.2 LinearGradientBrush画刷 290
12.2.3 RadialGradientBrush画刷 292
12.2.4 ImageBrush画刷 294
12.2.5 平铺的ImageBrush画刷 295
12.2.6 VisualBrush画刷 297
12.2.7 BitmapCacheBrush画刷 298
12.3 变换 299
12.3.1 变换形状 300
12.3.2 变换元素 302
12.4 透明 303
12.4.1 使元素半透明 303
12.4.2 透明掩码 304
12.5 小结 306
第13章 几何图形和图画 307
13.1 路径和几何图形 307
13.1.1 直线、矩形和椭圆图形 308
13.1.2 使用GeometryGroup
组合形状 309
13.1.3 使用CombinedGeometry融合
几何图形 311
13.1.4 使用PathGeometry绘制曲线和
直线 313
13.1.5 微语言几何图形 318
13.1.6 使用几何图形进行剪裁 319
13.2 图画 320
13.2.1 显示图画 322
13.2.2 导出插图 324
13.3 小结 326
第14章 效果和可视化对象 327
14.1 可视化对象 327
14.1.1 绘制可视化对象 328
14.1.2 在元素中封装可视化对象 329
14.1.3 命中测试 332
14.1.4 复杂的命中测试 334
14.2 效果 338
14.2.1 BlurEffect类 338
14.2.2 DropShadowEffect类 339
14.2.3 ShaderEffect类 340
14.3 WriteableBitmap类 342
14.3.1 生成位图 342
14.3.2 写入WriteableBitmap对象 343
14.3.3 更高效的像素写入 345
14.4 小结 347
第15章 动画基础 349
15.1 理解WPF动画 349
15.1.1 基于时间的动画 349
15.1.2 基于属性的动画 350
15.2 基本动画 351
15.2.1 Animation类 351
15.2.2 使用代码创建动画 353
15.2.3 同时发生的动画 358
15.2.4 动画的生命周期 358
15.2.5 Timeline类 359
15.3 故事板 362
15.3.1 故事板 363
15.3.2 事件触发器 363
15.3.3 重叠动画 366
15.3.4 同步的动画 367
15.3.5 控制播放 367
15.3.6 监视动画进度 371
15.4 动画缓动 373
15.4.1 使用缓动函数 373
15.4.2 在动画开始时应用缓动与在动画
结束时应用缓动 374
15.4.3 缓动函数类 375
15.4.4 创建自定义缓动函数 377
15.5 动画性能 379
15.5.1 期望的帧率 380
15.5.2 位图缓存 382
15.6 小结 384
第16章 高级动画 385
16.1 动画类型回顾 385
16.1.1 动态变换 386
16.1.2 动态改变画刷 390
16.1.3 动态改变像素着色器 392
16.2 关键帧动画 393
16.2.1 离散的关键帧动画 395
16.2.2 缓动关键帧 395
16.2.3 样条关键帧动画 396
16.3 基于路径的动画 397
16.4 基于帧的动画 399
16.5 使用代码创建故事板 402
16.5.1 创建主窗口 403
16.5.2 创建Bomb用户控件 405
16.5.3 投弹 406
16.5.4 拦截炸弹 409
16.5.5 统计炸弹和清理工作 410
16.6 小结 412
第Ⅳ部分 模板和自定义元素
第17章 控件模板 417
17.1 理解逻辑树和可视化树 417
17.2 理解模板 422
17.2.1 修饰类 424
17.2.2 剖析控件 426
17.3 创建控件模板 428
17.3.1 简单按钮 429
17.3.2 模板绑定 430
17.3.3 改变属性的触发器 431
17.3.4 使用动画的触发器 434
17.4 组织模板资源 435
17.4.1 分解按钮控件模板 436
17.4.2 通过样式应用模板 438
17.4.3 自动应用模板 439
17.4.4 由用户选择的皮肤 440
17.5 构建更复杂的模板 442
17.5.1 嵌套的模板 443
17.5.2 修改滚动条 445
17.5.3 控件模板示例 450
17.6 可视化状态 451
17.7 小结 452
第18章 自定义元素 453
18.1 理解WPF中的自定义元素 454
18.2 构建基本的用户控件 456
18.2.1 定义依赖项属性 456
18.2.2 定义路由事件 459
18.2.3 添加标记 460
18.2.4 使用控件 462
18.2.5 命令支持 462
18.2.6 深入分析用户控件 465
18.3 创建无外观控件 466
18.3.1 修改颜色拾取器的代码 466
18.3.2 修改颜色拾取器的标记 467
18.3.3 精简控件模板 469
18.4 支持可视化状态 472
18.4.1 开始编写FlipPanel类 473
18.4.2 选择部件和状态 475
18.4.3 默认控件模板 476
18.4.4 使用FlipPanel控件 482
18.4.5 使用不同的控件模板 483
18.5 创建自定义面板 485
18.5.1 两步布局过程 485
18.5.2 Canvas面板的副本 488
18.5.3 更好的WrapPanel面板 489
18.6 自定义绘图元素 492
18.6.1 OnRender( )方法 493
18.6.2 评估自定义绘图 494
18.6.3 自定义绘图元素 495
18.6.4 创建自定义装饰元素 497
18.7 小结 498
第Ⅴ部分 数据
第19章 数据绑定 501
19.1 使用自定义对象绑定到
数据库 501
19.1.1 构建数据访问组件 502
19.1.2 构建数据对象 504
19.1.3 显示绑定对象 505
19.1.4 更新数据库 508
19.1.5 更改通知 508
19.2 绑定到对象集合 510
19.2.1 显示和编辑集合项 510
19.2.2 插入和移除集合项 513
19.2.3 绑定到ADO.NET对象 514
19.2.4 绑定到LINQ表达式 515
19.3 提高大列表的性能 518
19.3.1 虚拟化 518
19.3.2 项容器再循环 519
19.3.3 缓存长度 519
19.3.4 延迟滚动 520
19.4 验证 521
19.4.1 在数据对象中进行验证 521
19.4.2 自定义验证规则 526
19.4.3 响应验证错误 528
19.4.4 获取错误列表 529
19.4.5 显示不同的错误指示符号 530
19.4.6 验证多个值 533
19.5 数据提供者 535
19.5.1 ObjectDataProvider 536
19.5.2 XmlDataProvider 539
19.6 小结 541
第20章 格式化绑定的数据 543
20.1 数据绑定回顾 543
20.2 数据转换 544
20.2.1 使用StringFormat属性 545
20.2.2 值转换器简介 546
20.2.3 使用值转换器设置字符串
的格式 547
20.2.4 使用值转换器创建对象 549
20.2.5 应用条件格式化 551
20.2.6 评估多个属性 552
20.3 列表控件 554
20.4 列表样式 555
20.4.1 ItemContainerStyle 556
20.4.2 包含复选框或单选按钮的ListBox
控件 557
20.4.3 交替条目样式 559
20.4.4 样式选择器 561
20.5 数据模板 564
20.5.1 分离和重用模板 566
20.5.2 使用更高级的模板 567
20.5.3 改变模板 569
20.5.4 模板选择器 570
20.5.5 模板与选择 573
20.5.6 改变项的布局 577
20.6 ComboBox控件 578
20.7 小结 581
第21章 数据视图 583
21.1 View对象 583
21.1.1 检索视图对象 584
21.1.2 视图导航 584
21.1.3 以声明方式创建视图 587
21.2 过滤、排序与分组 588
21.2.1 过滤集合 588
21.2.2 过滤DataTable对象 591
21.2.3 排序 592
21.2.4 分组 593
21.2.5 实时成型 598
21.3 小结 599
第22章 列表、树和网格 601
22.1 ListView控件 601
22.1.1 使用GirdView创建列 602
22.1.2 创建自定义视图 606
22.2 TreeView控件 613
22.2.1 创建数据绑定的TreeView
控件 614
22.2.2 将DataSet对象绑定到TreeView
控件 617
22.2.3 即时创建节点 618
22.3 DataGrid控件 621
22.3.1 改变列的尺寸与重新安排列 622
22.3.2 定义列 623
22.3.3 设置列的格式和样式 628
22.3.4 设置行的格式 629
22.3.5 显示行细节 630
22.3.6 冻结列 631
22.3.7 选择 632
22.3.8 排序 632
22.3.9 编辑 633
22.4 小结 635


第Ⅵ 窗口、页面和富控件
第23章 窗口 639
23.1 Window类 639
23.1.1 显示窗口 641
23.1.2 定位窗口 642
23.1.3 保存和还原窗口位置 642
23.2 窗口交互 644
23.2.1 窗口所有权 646
23.2.2 对话框模型 647
23.2.3 通用对话框 648
23.3 非矩形窗口 649
23.3.1 简单形状窗口 649
23.3.2 具有形状内容的透明窗口 651
23.3.3 移动形状窗口 653
23.3.4 改变形状窗口的尺寸 653
23.3.5 组合到一起：窗口的自定义控件
模板 655
23.4 Windows 7任务栏编程 658
23.4.1 使用跳转列表 659
23.4.2 改变任务栏图标和预览 663
23.5 小结 667
第24章 页面和导航 669
24.1 基于页面的导航 669
24.2 基于页面的界面 670
24.2.1 创建一个具有导航窗口的基于
页面的简单应用程序 670
24.2.2 Page类 672
24.2.3 超链接 673
24.2.4 在框架中驻留页面 675
24.2.5 在另一个页面中驻留页面 677
24.2.6 在Web浏览器中驻留页面 678
24.3 页面历史 678
24.3.1 深入分析WPF中的URI 678
24.3.2 导航历史 679
24.3.3 维护自定义的属性 681
24.4 导航服务 682
24.4.1 通过编程进行导航 682
24.4.2 导航事件 683
24.4.3 管理日志 684
24.4.4 向日志添加自定义项 685
24.4.5 使用页函数 689
24.5 XAML浏览器应用程序 692
24.5.1 创建XBAP应用程序 692
24.5.2 部署XBAP应用程序 693
24.5.3 更新XBAP应用程序 695
24.5.4 XBAP应用程序的安全性 695
24.5.5 完全信任的XBAP应用程序 696
24.5.6 组合XBAP/独立应用程序 697
24.5.7 为不同的安全级别编写代码 697
24.5.8 在网页中嵌入XBAP
应用程序 702
24.6 WebBrowser控件 702
24.6.1 导航到页面 703
24.6.2 构建DOM树 704
24.6.3 使用.NET代码为网页添加
脚本 706
24.7 小结 708
第25章 菜单、工具栏和功能区 709
25.1 菜单 709
25.1.1 Menu类 710
25.1.2 菜单项 710
25.1.3 ContextMenu类 712
25.1.4 菜单分隔条 713
25.2 工具栏和状态栏 714
25.2.1 ToolBar控件 714
25.2.2 StatusBar控件 717
25.3 功能区 718
25.3.1 添加功能区 719
25.3.2 应用程序菜单 720
25.3.3 选项卡、组与按钮 722
25.3.4 富工具提示 724
25.3.5 带有快捷键提示的键盘访问 725
25.3.6 改变功能区的大小 726
25.3.7 快速访问工具栏 729
25.4 小结 730
第26章 声音和视频 731
26.1 播放WAV音频 731
26.1.1 SoundPlayer类 731
26.1.2 SoundPlayerAction类 733
26.1.3 系统声音 733
26.2 MediaPlayer类 734
26.3 MediaElement类 735
26.3.1 使用代码播放音频 736
26.3.2 处理错误 737
26.3.3 使用触发器播放音频 737
26.3.4 播放多个声音 739
26.3.5 改变音量、平衡、速度以及
位置 740
26.3.6 将动画同步到音频 742
26.3.7 播放视频 744
26.3.8 视频效果 744
26.4 语音 747
26.4.1 语音合成 747
26.4.2 语音识别 749
26.5 小结 751
第27章 3D绘图 753
27.1 3D绘图基础 753
27.1.1 视口 754
27.1.2 3D对象 754
27.1.3 摄像机 761
27.2 深入研究3D绘图 765
27.2.1 着色和法线 766
27.2.2 更复杂的形状 769
27.2.3 Model3DGroup集合 769
27.2.4 使用材质 771
27.2.5 纹理映射 773
27.3 交互和动画 777
27.3.1 变换 777
27.3.2 旋转 778
27.3.3 飞过 779
27.3.4 跟踪球 781
27.3.5 命中测试 782
27.3.6 3D表面上的2D元素 786
27.4 小结 789
第Ⅶ部分 文档和打印
第28章 文档 793
28.1 理解文档 793
28.2 流文档 794
28.2.1 流内容元素 795
28.2.2 设置内容元素的格式 796
28.2.3 创建简单的流文档 797
28.2.4 块元素 799
28.2.5 内联元素 804
28.2.6 通过代码与元素进行交互 809
28.2.7 文本对齐 812
28.3 只读流文档容器 813
28.3.1 缩放 814
28.3.2 创建页面和列 815
28.3.3 从文件加载文档 817
28.3.4 打印 818
28.4 编辑流文档 818
28.4.1 加载文件 819
28.4.2 保存文件 821
28.4.3 设置所选文本的格式 822
28.4.4 获取单个单词 824
28.5 固定文档 825
28.6 批注 826
28.6.1 批注类 827
28.6.2 启用批注服务 828
28.6.3 创建批注 829
28.6.4 检查批注 832
28.6.5 响应批注更改 835
28.6.6 在固定文档中保存批注 835
28.6.7 自定义便签的外观 836
28.7 小结 837
第29章 打印 839
29.1 基本打印 839
29.1.1 打印元素 840
29.1.2 变换打印输出 842
29.1.3 打印不显示的元素 844
29.1.4 打印文档 845
29.1.5 在文档打印输出中控制页面 848
29.2 自定义打印 851
29.2.1 使用可视化层中的类
进行打印 851
29.2.2 自定义多页打印 854
29.3 打印设置和管理 859
29.3.1 保存打印设置 859
29.3.2 打印页面范围 859
29.3.3 管理打印队列 860
29.4 通过XPS进行打印 863
29.4.1 为打印预览创建XPS文档 863
29.4.2 写入内存的XPS文档 864
29.4.3 通过XPS直接打印到
打印机 865
29.4.4 异步打印 866
29.5 小结 866
第Ⅷ部分 其他主题
第30章 与Windows窗体进行交互 869
30.1 访问互操作性 869
30.2 混合窗口和窗体 870
30.2.1 为WPF应用程序添加窗体 870
30.2.2 为Windows窗体应用程序
添加WPF窗口 870
30.2.3 显示模态窗口和窗体 871
30.2.4 显示非模态窗口和窗体 871
30.2.5 启用Windows窗体控件的
可视化风格 872
30.3 创建具有混合内容的窗口 872
30.3.1 WPF和Windows窗体
“空域” 873
30.3.2 在WPF中驻留Windows
窗体控件 874
30.3.3 使用WPF和Windows窗体
用户控件 876
30.3.4 在Windows窗体中驻留WPF
控件 877
30.3.5 访问键、助记码和焦点 879
30.3.6 属性映射 880
30.4 小结 882
第31章 多线程 883
31.1 了解多线程模型 883
31.1.1 Dispatcher类 884
31.1.2 DispatcherObject类 884
31.2 BackgroundWorker类 887
31.2.1 简单的异步操作 887
31.2.2 创建BackgroundWorker
对象 888
31.2.3 运行BackgroundWorker
对象 889
31.2.4 跟踪进度 891
31.2.5 支持取消 893
31.3 小结 894
第32章 插件模型 895
32.1 在MAF和MEF两者间
进行选择 895
32.2 了解插件管道 896
32.2.1 管道的工作原理 897
32.2.2 插件文件夹结构 898
32.2.3 为使用插件模型准备
解决方案 899
32.3 创建使用插件模型的
应用程序 900
32.3.1 协定 901
32.3.2 插件视图 901
32.3.3 插件 902
32.3.4 插件适配器 902
32.3.5 宿主视图 903
32.3.6 宿主适配器 904
32.3.7 宿主 904
32.3.8 更多插件 907
32.4 与宿主进行交互 908
32.5 可视化插件 912
32.6 小结 915
第33章 ClickOnce部署 917
33.1 理解应用程序部署 917
33.1.1 ClickOnce安装模型 918
33.1.2 ClickOnce部署的局限性 919
33.2 简单的ClickOnce发布 920
33.2.1 设置发布者和产品 920
33.2.2 启动发布向导 922
33.2.3 理解部署文件的结构 926
33.2.4 安装ClickOnce应用程序 926
33.2.5 更新ClickOnce应用程序 928
33.3 ClickOnce附加选项 928
33.3.1 发布版本 928
33.3.2 更新 929
33.3.3 文件关联 930
33.3.4 发布选项 931
33.4 小结 932

## HTML 5

## JQuery

## Angular

## React

## Vue.js

## Bootstrap学习总结

### Bootstrap 基础

#### 媒体查询（css3特性）

> @media not|only 媒体类型 and (媒体特性) {css 代码样式}

> css3中的媒体类型和媒体特性与bootsrap不太一样。

> 可以实现依据最小最大宽度（媒体类型）等设置不同css样式。

##### 媒体类型

> all	用于所有多媒体类型设备
> print	用于打印机
> screen	用于电脑屏幕，平板，智能手机等。
> speech	用于屏幕阅读器

##### 媒体特性

> aspect-ratio	定义输出设备中的页面可见区域宽度与高度的比率
> color	定义输出设备每一组彩色原件的个数。如果不是彩色设备，则值等于0
> color-index	定义在输出设备的彩色查询表中的条目数。如果没有使用彩色查询表，则值等于0
> device-aspect-ratio	定义输出设备的屏幕可见宽度与高度的比率。
> device-height	定义输出设备的屏幕可见高度。
> device-width	定义输出设备的屏幕可见宽度。
> grid	用来查询输出设备是否使用栅格或点阵。
> height	定义输出设备中的页面可见区域高度。
> max-aspect-ratio	定义输出设备的屏幕可见宽度与高度的最大比率。
> max-color	定义输出设备每一组彩色原件的最大个数。
> max-color-index	定义在输出设备的彩色查询表中的最大条目数。
> max-device-aspect-ratio	定义输出设备的屏幕可见宽度与高度的最大比率。
> max-device-height	定义输出设备的屏幕可见的最大高度。
> max-device-width	定义输出设备的屏幕最大可见宽度。
> max-height	定义输出设备中的页面最大可见区域高度。
> max-monochrome	定义在一个单色框架缓冲区中每像素包含的最大单色原件个数。
> max-resolution	定义设备的最大分辨率。
> max-width	定义输出设备中的页面最大可见区域宽度。
> min-aspect-ratio	定义输出设备中的页面可见区域宽度与高度的最小比率。
> min-color	定义输出设备每一组彩色原件的最小个数。
> min-color-index	定义在输出设备的彩色查询表中的最小条目数。
> min-device-aspect-ratio	定义输出设备的屏幕可见宽度与高度的最小比率。
> min-device-width	定义输出设备的屏幕最小可见宽度。
> min-device-height	定义输出设备的屏幕的最小可见高度。
> min-height	定义输出设备中的页面最小可见区域高度。
> min-monochrome	定义在一个单色框架缓冲区中每像素包含的最小单色原件个数
> min-resolution	定义设备的最小分辨率。
> min-width	定义输出设备中的页面最小可见区域宽度。
> monochrome	定义在一个单色框架缓冲区中每像素包含的单色原件个数。如果不是单色设备，则值等于0
> orientation	定义输出设备中的页面可见区域高度是否大于或等于宽度。
> resolution	定义设备的分辨率。如：96dpi, 300dpi, 118dpcm
> scan	定义电视类设备的扫描工序。
> width	定义输出设备中的页面可见区域宽度。


### Bootstrap 布局

#### 包装容器

> .container .container -{breakpoint} .container-fluid

#### 响应断点

> 当你须要搞定响应式布局时，一堆堆的媒体查询、大量的属性、属性值往往能够把你搞颠，SASS（或者诸如此类的预处理器）被觉得是处理响应式断点的最佳利器。

> 1.使用变量(With variables)
Bootstrap和Foundation採用这样的方式，首先定义变量，然后在媒体查询中使用变量。换句话说，你能够在配置文件或者其它地方定义变量以备使用。我们来看看Bootstrap怎么干的。
// Defining values
$screen-sm-min: 768px;
$screen-xs-max: ($screen-sm-min - 1);
$screen-md-min: 992px;
$screen-sm-max: ($screen-md-min - 1);
$screen-lg-min: 1200px;
$screen-md-max: ($screen-lg-min - 1);
 
// Usage
@media (max-width: $screen-xs-max) { ... }
@media (min-width: $screen-sm-min) { ... }
@media (max-width: $screen-sm-max) { ... }
@media (min-width: $screen-md-min) { ... }
@media (max-width: $screen-md-max) { ... }
@media (min-width: $screen-lg-min) { ... }
Foudation更进一步，使用跨范围的媒体查询，避免使用过多的max-width和min-width。
// Defining values
$small-range:   (0em, 40em);       /* 0, 640px */
$medium-range:  (40.063em, 64em);  /* 641px, 1024px */
$large-range:   (64.063em, 90em);  /* 1025px, 1440px */
$xlarge-range:  (90.063em, 120em); /* 1441px, 1920px */
$xxlarge-range: (120.063em);       /* 1921px */
 
// Defining media queries
$screen:       "only screen" !default;
$landscape:    "#{$screen} and (orientation: landscape)" !default;
$portrait:     "#{$screen} and (orientation: portrait)" !default;
$small-up:     $screen !default;
$small-only:   "#{$screen} and (max-width: #{upper-bound($small-range)})" !default;
$medium-up:    "#{$screen} and (min-width:#{lower-bound($medium-range)})" !default;
$medium-only:  "#{$screen} and (min-width:#{lower-bound($medium-range)}) and (max-width:#{upper-bound($medium-range)})" !default;
$large-up:     "#{$screen} and (min-width:#{lower-bound($large-range)})" !default;
$large-only:   "#{$screen} and (min-width:#{lower-bound($large-range)}) and (max-width:#{upper-bound($large-range)})" !default;
$xlarge-up:    "#{$screen} and (min-width:#{lower-bound($xlarge-range)})" !default;
$xlarge-only:  "#{$screen} and (min-width:#{lower-bound($xlarge-range)}) and (max-width:#{upper-bound($xlarge-range)})" !default;
$xxlarge-up:   "#{$screen} and (min-width:#{lower-bound($xxlarge-range)})" !default;
$xxlarge-only: "#{$screen} and (min-width:#{lower-bound($xxlarge-range)}) and (max-width:#{upper-bound($xxlarge-range)})" !default;
 
// Usage
@media #{$small-up}     { ... }
@media #{$small-only}   { ... }
@media #{$medium-up}    { ... }
@media #{$medium-only}  { ... }
@media #{$large-up}     { ... }
@media #{$large-only}   { ... }
@media #{$xlarge-up}    { ... }
@media #{$xlarge-only}  { ... }
@media #{$xxlarge-up}   { ... }
@media #{$xxlarge-only} { ... }
两种方法各有一个不爽的地方，在Bootstrap里每次都要使用max-width，在Foundation里我们须要使用插值变量这样的又丑又烦的方式。显示我们须要想办法解决这些问题。

> 2.使用独立Mixin(With a standalone mixin)《media queries in Sass 3.2》是CSS-Tricks里最火的文章之中的一个，在这篇文章里Chris Coyier在借鉴a former idea by Mason Wendell和a former idea by Jeff Croft两文的基础上，怎样使用sass实现响应式布局的断点管理。

命名断点是非常重要的，由于能够为抽象的数字赋予意义（你知道767px是什么意思吗，我不知道，直到我去使用小屏幕的时候才知道）。为什么Bootstrap和Foundation要使用变量呢，不也是为了给抽象的数字起个名字吗？
所以我们定义个mixin，接收断点名作唯一的參数，返回媒体查询的内容。准备好了吗？走起。
@mixin respond-to($breakpoint) {
  @if $breakpoint == "small" {
    @media (min-width: 767px) {
      @content;
    }
  }
 
  @else if $breakpoint == "medium" {
    @media (min-width: 992px) {
      @content;
    }
  }
 
  @else if $breakpoint == "large" {
    @media (min-width: 1200px) {
      @content;
    }
  }
}
然后，我们这样使用mixin。
@include respond-to(small) { ... }
@include respond-to(medium) { ... }
@include respond-to(large) { ... }
这种方法是极好的（甄嬛体，老外也看？），原因有二：抽象数据有意义，大量断点集中管理。假设你想把“992px”改成“970px”，你不须要爬过每个css文件，而仅仅需更新mixin，然后所有更新。
可是也还有两个问题：
a.断点不easy从mixin里拿出来，放到配置文件中去。
b.冗余太多。

> 3. 可配置的mixin(With a configurable mixin  )

<为了解决上面的两个问题，我们须要从断点mixin中抽出一个列表，仅仅剩下mixin核心，然后这个列表就能够随便移动，或者扔到配置文件中。
然后，使用sass 3.3+中的maps，我们能够方便的使用关联的属性和属性值。
$breakpoints: (
  'small'  : 767px,
  'medium' : 992px,
  'large'  : 1200px
);
然后原来的mixin进行相应的改动
@mixin respond-to($breakpoint) {
  // Retrieves the value from the key
  $value: map-get($breakpoints, $breakpoint);
 
  // If the key exists in the map
  @if $value != null {
    // Prints a media query based on the value
    @media (min-width: $value) {
      @content;
    }
  }
 
  // If the key doesn't exist in the map
  @else {
    @warn "Unfortunately, no value could be retrieved from `#{$breakpoint}`. "
        + "Please make sure it is defined in `$breakpoints` map.";
  }
}
我们在改动mixin的同一时候也进行了一些提高，不要小看这些提高，我们加上了错误处理，假设在maps中没有找到断点值，将会弹出一个错误提示，这将便于我们开发过程中的调试。
我们让mixin变得更加精简，能非常好的处理错误，同一时候我们去掉了一个功能——推断属性是否是你想要的（min-width,max-width,min-height等），这在移动优先的网页中没问题，由于我们仅仅须要min-width。可是，假设须要查询其它属性，我们须要把这个功能加回来。为了达到这个目的，我想到了一个非常优雅的解决方式，同一时候并不添加复杂性。
$breakpoints: (
  'small'  : ( min-width:  767px ),
  'medium' : ( min-width:  992px ),
  'large'  : ( min-width: 1200px )
);
  
@mixin respond-to($name) {
  // If the key exists in the map
  @if map-has-key($breakpoints, $name) {
    // Prints a media query based on the value
    @media #{inspect(map-get($breakpoints, $name))} {
      @content;
    }
  }
 
  // If the key doesn't exist in the map
  @else {
    @warn "Unfortunately, no value could be retrieved from `#{$breakpoint}`. "
        + "Please make sure it is defined in `$breakpoints` map.";
  }
}
在这里，我们主要做了三个事情
a. 检查查询的断点在map中存在不存在
b.假设存在，打印相应的媒体查询。
c.假设不在，进行错误提示。
简单吧，假设我们回想前面的两个缺陷，已经不再有WET(Write Everything Twice))问题，也不再有不灵活的媒体查询。可是另一个问题，不支持复杂的媒体查询。复杂指的是涉及多个组件的查询（e.g. screen and (min-width: 767px)）。我们上面这些方案除了第一种变量之外都不能非常好的解决问题。

> 4. 使用外部工具(With an external tool)

```
最后一个相同重要的是，假设不想创建自己的mixin，你能够使用外部的工具处理响应式布局的断点，有非常多sass的扩展在这个方面做得非常好。
SassMQ by Kaelig
Breakpoint by Mason Wendell and Sam Richard
Breakup by Ben Scott
 	SassMQ	Breakpoint	Breakup
MQ type	*-width	any	any
No Query fallback	yep	yep	yep
API complexity	simple	very simple	medium
Code complexity	very simple	complexe	simple
Extra	Debug mode	Singularity.gs	—
基本上是这样，假设发现有没有涉及的，记得一定告诉我。
SassMQ
// Configuration
$mq-responsive: true;
$mq-static-breakpoint: desktop;
$mq-breakpoints: (
  mobile:  320px,
  tablet:  740px,
  desktop: 980px,
  wide:    1300px
);
 
// Example
selector {
  @include mq($from: mobile) {
    property: value;
  }
}
BreakPoints
$high-tide: 500px;
$ex-presidents: 600px 800px;
$surfboard-width: max-width 1000px;
$surfboard-height: (min-height 1000px) (orientation portrait);
 
selector {
  @include breakpoint($high-tide) {
    property: value;
  }
}
Breakup
$breakup-breakpoints: (
  'thin' '(max-width: 35.999em)',
  'wide' '(min-width: 36em)',
  'full' '(min-width: 61em)'
);
 
selector {
  @include breakup-block('thin') {
    property: value;
  }
}
```

#### 堆叠顺序 z-index


#### 网格系统

> 12列的网格 col-2 列占用2/12的宽度 



### Bootstrap 版式

#### 文档案

#### 图片

#### 表格

#### 代码


### Bootstrap 通用样式

#### 文本

#### 颜色

#### 边框

#### 定位浮动

#### 代码弹性盒子

#### 其它 对齐等


### Bootstrap 组件

#### 按钮

#### 按钮组

#### 下拉

#### 媒体对象

#### 表单

#### 进度条

#### 导航栏

#### 列表组

#### 面包屑 

> 显示导航层次位置 如 “首页-> 文学-> 中国文学”

#### 分页

#### 加载指示器（转圈圈）

#### 按钮卡片

###  Sass

#### 变量

#### 嵌套归斥责

#### 导入

#### SASS 混合器 混合器继承

> 混合器 Sass中的混合器类似于js的函数，将一段代码定义成混合器以实现代码的重用  编译后其实会转换成正常的css

> 声明混合器：@mixin mixName 

> 调用混合器  @include minName 如

@mixin border-round{
    -moz-border:1px solid red;
    -webkit-border:1px solid red;
    border:1px solid red
}
#top{
    @include border-round;
}

//编译后
#top {
  -moz-border: 1px solid red;
  -webkit-border: 1px solid red;
  border: 1px solid red; }

> 混合器css规则 混合器中也可以包含css规则

@mixin testmix{
    list-style:none;
    li{
        color:red;
        padding:30px;
    }
    >.top{
        background:red
    }
}

ul.parent{
    border:1px solid red;
    @include testmix;
}
//编译后
ul.parent {
  border: 1px solid red;
  list-style: none; 
}
  ul.parent li {
    color: red;
    padding: 30px; 
}
  ul.parent > .top {
    background: red;
 }

> 混合器传参 混合器可以像函数一样传递参数 混合器传参数

@mixin test($color,$size,$hoverColor){
    color:$color;
    border:$size solid red;
    &:hover{
        color:$hoverColor
    }
}

#top{
    @include test(red,1px,blue);
}
//编译后
#top {
  color: red;
  border: 1px solid red; 
}
  #top:hover {
    color: blue; 
}

/*# 

当然这里有个问题，混合器里面的参数不允许颠倒位置，如果你记不清他们什么位置可以使用键值的方式明确指定

@mixin test($color,$size,$hoverColor){
    color:$color;
    border:$size solid red;
    &:hover{
        color:$hoverColor
    }
}

#top{
    @include test($size:1px,$hoverColor:blue,$color:red);
}
//编译后
#top {
  color: red;
  border: 1px solid red;
  }
#top:hover {
    color: blue;
  }

> 参数默认值 混合器允许你定义参数默认值 如下

@mixin test($normal,$hover:red){
    color:$normal;
    background-color:$hover
}
#top{
    @include test(skyblue,orange);
}
//编译后
#top {
  color: skyblue;
  background-color: orange;
  }
  //不指定color
@mixin test($normal,$hover:red){
    color:$normal;
    background-color:$hover
}
#top{
    @include test(skyblue);
}
//编译后
  
#top {
  color: skyblue;
  background-color: red; }

> Sass继承 Sass中也可实现继承类似面向对象思想子类继承父类，sass可以继承多个父类 这个”父类“可以是类，id 标签 状态等。 继承语法 @extend name 如

.error{
    color:red;
    font-size:15px;
}
.danger-error{
    @extend .error;
    font-size:20px;
}
//编译后
.error, .danger-error {
  color: red;
  font-size: 15px;
}

.danger-error {
  font-size: 20px; 
}

当然父类也可包含css规则

.error{
    color:red;
    font-size:15px;
    >.te{
        padding:10px
    }
}
.danger-error{
    @extend .error;
    font-size:20px;
}
//编译后
.error, .danger-error {
  color: red;
  font-size: 15px; 
}
.error > .te, .danger-error > .te {
    padding: 10px;
  }

.danger-error {
  font-size: 20px; 
 }

> 组合继承

.error a{
    color:red;
    font-size:10px;
}
.danger{
    @extend .error;
    color:orange;
}
//编译后
.error a, .danger a {
  color: red;
  font-size: 10px; 
}

.danger {
  color: orange; 
}


> 继承多个

.one{
    color:red;
}
.two{

    border:1px solid red;
}
.three{
    @extend .one;
    @extend .two;
    //或者这样写@extend .one,.two
    //
    background:blue;
}
//编译后
.one, .three {
  color: red; 
}
.two, .three {
  border: 1px solid red;
}
.three {
  background: blue;
}


> 继承局限性 继承不支持组合 很多选择器不支持继承如包选择器 .one tow 相邻选择器 .one+.two

%继承 有些时候我们希望被用来继承的代码不要渲染到页面上只作为继承使用。 定义方法 父类名前+%

%test{
    border:1px solid red;
}
#main{
    @extend %test;
}
//编译后
#main {
  border: 1px solid red; 
}


#meng a%long{
    color:blue;
    border:1px solid red;
}

.notice{
    @extend %long;
}
//编译后
#meng a.notice {
  color: blue;
  border: 1px solid red; 
}

继承在指令的作用域如（@media） 在指令内部无法继承到指令外部的类，指令外部继承指令内部的类无法达到预期效果

.one{
    height:400px;
}

@media print{
    .two{
        @extend .one
    }
    width:300px;
}

> 编译时报错 继承注意事项

> 不能过量使用继承，因为所有类继承了父类，父类改变就会影响子类
 
继承只会在生成css时复制选择器，而不会复制大段的css属性  如果不小心会让生成css中包含大量的选择器复制  避免这种情况的最好办法：  不要在继承css规则中使用后代选择器如
 
 .dsf{}
 .foo .bar {
 @extend dsf //不推荐
 }



##  Font Awesome

## Asp.net core MVC 一些总结

### Router

#### property router

> [Route("app/[controller]/actions/[action]/{id:weekday?}")]

#### 设置路由中间件
```
app.UseMvc(routes =>
            {
                routes.MapRoute(
                    name: "default",
                    template: "{controller=Home}/{action=Index}/{id?}");
            });
```

> 常规路由：routes.MapRoute(name: "default",template: "{controller=Home}/{action=Index}/{id?}");  这是一个常规路由

#### 多路由 

```
app.UseMvc(routes =>
            {
                routes.MapRoute("blog", "blog/{*article}",
                    defaults: new { Controller = "Blog", Action = "Index" });
                routes.MapRoute(
                    name: "default",
                    template: "{controller=Home}/{action=Index}/{id?}");
            });
```


#### 高级路由

```
app.UseMvc(routes => {
                routes.MapRoute(
                    name: "areas",
                    template: "{area:exists}/{controller=Home}/{action=Index}");

                routes.Routes.Add(new LegacyRoute(
                    routes.DefaultHandler,
                    "/articles/Windows_3.1_Overview.html",
                    "/old/.NET_1.0_Class_Library"));

                routes.MapRoute(
                    name: "default",
                    template: "{controller=Home}/{action=Index}/{id?}");

                routes.MapRoute(
                    name: "out",
                    template: "outbound/{controller=Home}/{action=Index}");
            });
```


### Session

```
using System;
using Microsoft.AspNetCore.Http;
using Microsoft.Extensions.DependencyInjection;
using Newtonsoft.Json;
using SportsStore.Infrastructure;

namespace SportsStore.Models
{

    public class SessionCart : Cart
    {

        public static Cart GetCart(IServiceProvider services)
        {
            ISession session = services.GetRequiredService<IHttpContextAccessor>()?
                .HttpContext.Session;
            SessionCart cart = session?.GetJson<SessionCart>("Cart")
                ?? new SessionCart();
            cart.Session = session;
            return cart;
        }

        [JsonIgnore]
        public ISession Session { get; set; }

        public override void AddItem(Product product, int quantity)
        {
            base.AddItem(product, quantity);
            Session.SetJson("Cart", this);
        }

        public override void RemoveLine(Product product)
        {
            base.RemoveLine(product);
            Session.SetJson("Cart", this);
        }

        public override void Clear()
        {
            base.Clear();
            Session.Remove("Cart");
        }
    }
}

```


### 授权认证管理

#### 认证
```
using System.Threading.Tasks;
using Microsoft.AspNetCore.Authorization;
using Microsoft.AspNetCore.Identity;
using Microsoft.AspNetCore.Mvc;
using SportsStore.Models.ViewModels;
using SportsStore.Models;

[Authorize]
public class AccountController : Controller {
    private UserManager<IdentityUser> userManager;
    private SignInManager<IdentityUser> signInManager;

    public AccountController(UserManager<IdentityUser> userMgr,
            SignInManager<IdentityUser> signInMgr) {
        userManager = userMgr;
        signInManager = signInMgr;
        IdentitySeedData.EnsurePopulated(userMgr).Wait();
    }

    [AllowAnonymous]
    public ViewResult Login(string returnUrl) {
        return View(new LoginModel {
            ReturnUrl = returnUrl
        });
    }

    [HttpPost]
    [AllowAnonymous]
    [ValidateAntiForgeryToken]
    public async Task<IActionResult> Login(LoginModel loginModel) {
        if (ModelState.IsValid) {
            IdentityUser user =
                await userManager.FindByNameAsync(loginModel.Name);
            if (user != null) {
                await signInManager.SignOutAsync();
                if ((await signInManager.PasswordSignInAsync(user,
                        loginModel.Password, false, false)).Succeeded) {
                    return Redirect(loginModel?.ReturnUrl ?? "/Admin/Index");
                }
            }
        }
        ModelState.AddModelError("", "Invalid name or password");
        return View(loginModel);
    }

    public async Task<RedirectResult> Logout(string returnUrl = "/") {
        await signInManager.SignOutAsync();
        return Redirect(returnUrl);
    }
}
```

> rezor

```
@model LoginModel
@{
    ViewBag.Title = "Log In";
    Layout = "_AdminLayout";
}

<div class="text-danger" asp-validation-summary="All"></div>

<form asp-action="Login" asp-controller="Account" method="post">
    <input type="hidden" asp-for="ReturnUrl" />
    <div class="form-group">
        <label asp-for="Name"></label>
        <div><span asp-validation-for="Name" class="text-danger"></span></div>
        <input asp-for="Name" class="form-control" />
    </div>
    <div class="form-group">
        <label asp-for="Password"></label>
        <div><span asp-validation-for="Password" class="text-danger"></span></div>
        <input asp-for="Password" class="form-control" />
    </div>
    <button class="btn btn-primary" type="submit">Log In</button>
</form>

```

### DI

> services.AddSingleton<IRepository, MemoryRepository>(); 单实例

> services.AddTransient<IModelStorage, DictionaryStorage>(); 每一次获取的对象都不是同一个

> services.AddScoped 请求开始-请求结束 在这次请求中获取的对象都是同一个；不用申明静态类；

### Filters

#### 子类Controller拦截器要先于父类Controller拦截器执行

> 最先执行的是全局声明的MyActionOneAttribute拦截器

> 然后执行的是声明在子Controller类HomeController上的MyActionThreeAttribute拦截器

> 接着执行的是声明在父Controller类BaseController上的MyActionTwoAttribute拦截器

> 最后执行的是声明在子Controller类HomeController的Index方法上的MyActionFourAttribute拦截器

```
public class MyFilterAttribute : ResultFilterAttribute {
    private string message;

    public MyFilterAttribute(string msg) {
        message = msg;
    }

    public override void OnResultExecuting(ResultExecutingContext context) {
        WriteMessage(context, $"<div>Before Result:{message}</div>");
    }

    public override void OnResultExecuted(ResultExecutedContext context) {
        WriteMessage(context, $"<div>After Result:{message}</div>");
    }

    private void WriteMessage(FilterContext context, string msg) {
        byte[] bytes = Encoding.ASCII
            .GetBytes($"<div>{msg}</div>");

        // Synchronous operations are disallowed. Call WriteAsync or set AllowSynchronousIO to true instead.
        context.HttpContext.Response
            .Body.WriteAsync(bytes, 0, bytes.Length);
    }
}
```

> Usage:

```
    [MyFilter("This is the Controller-Scoped Filter", Order = 10)]
    public class HomeController : Controller {

        [MyFilter("This is the First Action-Scoped Filter", Order = 1)]
        [MyFilter("This is the Second Action-Scoped Filter", Order = -1)]
        public ViewResult Index() => View("Message",
            "This is the Index action on the Home controller");
    }
```


#### 授权过滤器 AuthorizeAttribute

```
 public class HttpsOnlyAttribute : Attribute, IAuthorizationFilter {

        public void OnAuthorization(AuthorizationFilterContext context) {
            if (!context.HttpContext.Request.IsHttps) {
                context.Result =
                    new StatusCodeResult(StatusCodes.Status403Forbidden);
            }
        }
    }
```

#### 资源过滤器 IResourceFilter

```
public class CustomerResourceFilterAttribute : Attribute, IResourceFilter
    {
        private static Dictionary<string,object> cacheDic=new Dictionary<string, object>();
        public void OnResourceExecuting(ResourceExecutingContext context)
        {
            var path=context.HttpContext.Request.Path; 
            if (cacheDic.ContainsKey(path))
            {
                context.Result = (IActionResult)cacheDic[path];
            }
            Console.WriteLine("CustomerResourceFilterAttribute.OnResourceExecuting");
        }
        public void OnResourceExecuted(ResourceExecutedContext context)
        {
            var path = context.HttpContext.Request.Path;
            cacheDic[path] = context.Result;
            Console.WriteLine("CustomerResourceFilterAttribute.OnResourceExecuted");
        }
 
         
    }
```

#### 异常过滤器 IExceptionFilter

```
public class RangeExceptionAttribute : ExceptionFilterAttribute {

        public override void OnException(ExceptionContext context) {
            if (context.Exception is ArgumentOutOfRangeException) {
                context.Result = new ViewResult() {
                    ViewName = "Message",
                    ViewData = new ViewDataDictionary(
                        new EmptyModelMetadataProvider(),
                        new ModelStateDictionary()) {
                        Model = @"The data received by the
                                application cannot be processed"
                    }
                };
            }
        }
    }
```

#### 操作过滤器 ActionFilterAttribute

```
public class ProfileAttribute : ActionFilterAttribute {
        private Stopwatch timer;
        private double actionTime;

        public override async Task OnActionExecutionAsync(
                ActionExecutingContext context,
                ActionExecutionDelegate next) {

            timer = Stopwatch.StartNew();

            await next();

            actionTime = timer.Elapsed.TotalMilliseconds;
        }

        public override async Task OnResultExecutionAsync(
                ResultExecutingContext context,
                ResultExecutionDelegate next) {

            await next();

            timer.Stop();
            string result = "<div>Action time: "
                + $"{actionTime} ms</div><div>Total time: "
                + $"{timer.Elapsed.TotalMilliseconds} ms</div>";
            byte[] bytes = Encoding.ASCII.GetBytes(result);

            await context.HttpContext.Response.Body.WriteAsync(bytes,
                0, bytes.Length);
        }
    }
```

```
public class ViewResultDiagnostics : IActionFilter {
        private IFilterDiagnostics diagnostics;

        public ViewResultDiagnostics(IFilterDiagnostics diags) {
            diagnostics = diags;
        }

        public void OnActionExecuting(ActionExecutingContext context) {
            // do nothing - not used in this filter
        }

        public void OnActionExecuted(ActionExecutedContext context) {
            ViewResult vr;
            if ((vr = context.Result as ViewResult) != null) {
                diagnostics.AddMessage($"View name: {vr.ViewName}");
                diagnostics.AddMessage($@"Model type: 
                    {vr.ViewData.Model.GetType().Name}");
            }
        }
    }
```

#### 结果过滤器 ResultFilterAttribute

```
     public class MessageAttribute : ResultFilterAttribute {
        private string message;

        public MessageAttribute(string msg) {
            message = msg;
        }

        public override void OnResultExecuting(ResultExecutingContext context) {
            WriteMessage(context, $"<div>Before Result:{message}</div>");
        }

        public override void OnResultExecuted(ResultExecutedContext context) {
            WriteMessage(context, $"<div>After Result:{message}</div>");
        }

        private void WriteMessage(FilterContext context, string msg) {
            byte[] bytes = Encoding.ASCII
                .GetBytes($"<div>{msg}</div>");

            // Synchronous operations are disallowed. Call WriteAsync or set AllowSynchronousIO to true instead.
            context.HttpContext.Response
                .Body.WriteAsync(bytes, 0, bytes.Length);
        }
    }
```

```
 public class ViewResultDetailsAttribute : ResultFilterAttribute {

        public override async Task OnResultExecutionAsync(
                ResultExecutingContext context,
                ResultExecutionDelegate next) {

            Dictionary<string, string> dict = new Dictionary<string, string> {
                ["Result Type"] = context.Result.GetType().Name,
            };

            ViewResult vr;
            if ((vr = context.Result as ViewResult) != null) {
                dict["View Name"] = vr.ViewName;
                dict["Model Type"] = vr.ViewData.Model.GetType().Name;
                dict["Model Data"] = vr.ViewData.Model.ToString();
            }

            context.Result = new ViewResult {
                ViewName = "Message",
                ViewData = new ViewDataDictionary(
                        new EmptyModelMetadataProvider(),
                        new ModelStateDictionary()) {
                    Model = dict
                }
            };

            await next();
        }
    }
```

#### 结果过滤器 IFilterDiagnostics

```
     public interface IFilterDiagnostics {
        IEnumerable<string> Messages { get; }
        void AddMessage(string message);
    }

    public class DefaultFilterDiagnostics : IFilterDiagnostics {
        private List<string> messages = new List<string>();

        public IEnumerable<string> Messages => messages;

        public void AddMessage(string message) =>
            messages.Add(message);
    }
```

#### IAsyncResultFilter

```
    public class DiagnosticsFilter : IAsyncResultFilter {
        private IFilterDiagnostics diagnostics;

        public DiagnosticsFilter(IFilterDiagnostics diags) {
            diagnostics = diags;
        }

        public async Task OnResultExecutionAsync(
                ResultExecutingContext context,
                ResultExecutionDelegate next) {

            await next();

            foreach (string message in diagnostics?.Messages) {
                byte[] bytes = Encoding.ASCII
                    .GetBytes($"<div>{message}</div>");
                await context.HttpContext.Response.Body
                    .WriteAsync(bytes, 0, bytes.Length);
            }
        }
    }
```


```
 public class TimeFilter : IAsyncActionFilter, IAsyncResultFilter {
        private ConcurrentQueue<double> actionTimes = new ConcurrentQueue<double>();
        private ConcurrentQueue<double> resultTimes = new ConcurrentQueue<double>();
        private IFilterDiagnostics diagnostics;

        public TimeFilter(IFilterDiagnostics diags) {
            diagnostics = diags;
        }

        public async Task OnActionExecutionAsync(
                ActionExecutingContext context, ActionExecutionDelegate next) {

            Stopwatch timer = Stopwatch.StartNew();
            await next();
            timer.Stop();
            actionTimes.Enqueue(timer.Elapsed.TotalMilliseconds);
            diagnostics.AddMessage($@"Action time: 
                {timer.Elapsed.TotalMilliseconds} 
                Average: {actionTimes.Average():F2}");
        }

        public async Task OnResultExecutionAsync(
                ResultExecutingContext context, ResultExecutionDelegate next) {

            Stopwatch timer = Stopwatch.StartNew();
            await next();
            timer.Stop();
            resultTimes.Enqueue(timer.Elapsed.TotalMilliseconds);
            diagnostics.AddMessage($@"Result time: 
                {timer.Elapsed.TotalMilliseconds}
                Average: {resultTimes.Average():F2}");
        }
    }
```


### Controllers

> [HttpGet("object/{format?}")]
>        [FormatFilter]

#### WebAPI
```
    [Route("api/[controller]")]
    public class ContentController : Controller {

        [HttpGet("string")]
        public string GetString() => "This is a string response";

        [HttpGet("object/{format?}")]
        [FormatFilter]
        //[Produces("application/json", "application/xml")]
        public Reservation GetObject() => new Reservation {
            ReservationId = 100,
            ClientName = "Joe",
            Location = "Board Room"
        };

        [HttpPost]
        [Consumes("application/json")]
        public Reservation ReceiveJson([FromBody] Reservation reservation) {
            reservation.ClientName = "Json";
            return reservation;
        }

        [HttpPost]
        [Consumes("application/xml")]
        public Reservation ReceiveXml([FromBody] Reservation reservation) {
            reservation.ClientName = "Xml";
            return reservation;
        }
    }
```

#### Controller

##### 所有的动作结果都继承自ActionResult基类 ASP.NET MVC框架支持六种标准类型的动作结果：

> 动作名称 概述 方法名

> ViewResult 视图内容，HTML或标记 View

> EmptyResult 空内容

> RedirectResult 重定向到新的URL

> Redirect RedirectToRouteResult 重定向到新的控制器

> RedirectToAction/RedirectToRoute JsonResult 返回一个JSON（Javascript Object Notation）内容 Json ContentResult 返回文本内容 Content

```
[Route("api/[controller]")]
    public class ReservationController : Controller {
        private IRepository repository;

        public ReservationController(IRepository repo) => repository = repo;

        [HttpGet]
        public IEnumerable<Reservation> Get() => repository.Reservations;

        [HttpGet("{id}")]
        public Reservation Get(int id) => repository[id];

        [HttpPost]
        public Reservation Post([FromBody] Reservation res) =>
            repository.AddReservation(new Reservation {
                ClientName = res.ClientName,
                Location = res.Location
            });

        [HttpPut]
        public Reservation Put([FromBody] Reservation res) =>
            repository.UpdateReservation(res);

        [HttpPatch("{id}")]
        public StatusCodeResult Patch(int id,
                [FromBody]JsonPatchDocument<Reservation> patch) {
            Reservation res = Get(id);
            if (res != null) {
                patch.ApplyTo(res);
                return Ok();
            }
            return NotFound();
        }

        [HttpDelete("{id}")]
        public void Delete(int id) => repository.DeleteReservation(id);
    }
```

#### Rezor View
```
@model IEnumerable<Reservation>
@{  Layout = "_Layout"; }

<form id="addform" asp-action="AddReservation" method="post">
    <div class="form-group">
        <label for="ClientName">Name:</label>
        <input class="form-control" name="ClientName" />
    </div>
    <div class="form-group">
        <label for="Location">Location:</label>
        <input class="form-control" name="Location" />
    </div>
    <div class="text-center panel-body">
        <button type="submit" class="btn btn-sm btn-primary">Add</button>
    </div>
</form>

<table class="table table-sm table-striped table-bordered m-2">
    <thead><tr><th>ID</th><th>Client</th><th>Location</th></tr></thead>
    <tbody>
        @foreach (var r in Model) {
            <tr>
                <td>@r.ReservationId</td>
                <td>@r.ClientName</td>
                <td>@r.Location</td>
            </tr>
        }
    </tbody>
</table>

```

```
services.AddMvc()
    .AddXmlDataContractSerializerFormatters()
    .AddMvcOptions(opts => {
        opts.EnableEndpointRouting = false;
        opts.FormatterMappings.SetMediaTypeMappingForFormat("xml",
            new MediaTypeHeaderValue("application/xml"));
        opts.RespectBrowserAcceptHeader = true;
        opts.ReturnHttpNotAcceptable = true;
    });
```


### ViewComponent

```
 public class PageSize : ViewComponent {

        public async Task<IViewComponentResult> InvokeAsync() {
            HttpClient client = new HttpClient();
            HttpResponseMessage response
                = await client.GetAsync("http://apress.com");
            return View(response.Content.Headers.ContentLength);
        }
    }
```


### Taghelper 可以扩展一些自定义的标记 其实就是后台生成html代码的一种形式

> 扩展标记，可以从后台进行前端Html的配置

> HtmlTargetElement 属性中配置那些html元素，那些样式起作用

> 定义一个Taghelper  formbutton 设置其属性
```
    [HtmlTargetElement("button", Attributes = "bs-button-color", ParentTag = "div")]
    [HtmlTargetElement("a", Attributes = "bs-button-color", ParentTag = "div")]
    [HtmlTargetElement("formbutton")]
    public class LYFButtonTagHelper : TagHelper {

        public string BsButtonColor { get; set; } = "primary";

        public override void Process(TagHelperContext context,
                                     TagHelperOutput output) {

            output.Attributes.SetAttribute("class", $"btn btn-{BsButtonColor}");
        }
    }
```

> View中用法

```
<formbutton>hello</formbutton>
```

> 本质上所有的mvc视图元素都是来自Taghelper 比如form

```
<form method="post" asp-controller="Home" asp-action="Create"
      asp-antiforgery="true">
    <div class="form-group">
        <label asp-for="Name"></label>
        <input class="form-control" asp-for="Name" />
    </div>
    <div class="form-group">
        <label asp-for="Country"></label>
        <select class="form-control" asp-for="Country" asp-items="ViewBag.Countries">
            <option disabled selected value="">Select a Country</option>
        </select>
    </div>
    <div class="form-group">
        <label asp-for="Population"></label>
        <input class="form-control" asp-for="Population" />
    </div>
    <div class="form-group">
        <label asp-for="Notes"></label>
        <textarea class="form-control" asp-for="Notes"></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Add</button>
    <a class="btn btn-primary" href="/Home/Index">Cancel</a>
</form>

```

### SignalR

> 什么是 SignalR？

> > ASP.NET Core SignalR 是一个开放源代码库，可用于简化向应用添加实时 Web 功能。 实时 Web 功能使服务器端代码能够将内容推送到客户端。

> 适合 SignalR 的候选项：

> > 需要从服务器进行高频率更新的应用。 示例包括游戏、社交网络、投票、拍卖、地图和 GPS 应用。

> > 仪表板和监视应用。 示例包括公司仪表板、即时销售更新或旅行警报。

> > 协作应用。 协作应用的示例包括白板应用和团队会议软件。

> > 需要通知的应用。 社交网络、电子邮件、聊天、游戏、旅行警报和很多其他应用都需使用通知。

> > SignalR 提供用于创建服务器到客户端远程过程调用 (RPC) 的 API。 RPC 从服务器端 .NET Core 代码调用客户端上的函数。 提供多个受支持的平台，其中每个平台都有各自的客户端 SDK。 因此，RPC 调用所调用的编程语言有所不同。

> 以下是 ASP.NET Core SignalR 的一些功能：

> > 自动处理连接管理。

> > 同时向所有连接的客户端发送消息。 例如聊天室。

> > 向特定客户端或客户端组发送消息。

> > 对其进行缩放，以处理不断增加的流量。

> > SignalR 中心协议

> > 源托管在 GitHub 上的存储库中SignalR。

> 传输

> > SignalR 支持以下用于处理实时通信的技术（按正常回退的顺序）：

> > WebSockets
> > Server-Sent Events
> > 长轮询

> > SignalR 自动选择服务器和客户端能力范围内的最佳传输方法。

> 中心

> > SignalR 使用 中心 在客户端和服务器之间进行通信。

> > Hub 是一种高级管道，允许客户端和服务器相互调用方法。 SignalR 自动处理跨计算机边界的调度，并允许客户端调用服务器上的方法，反之亦然。 可以将强类型参数传递给方法，从而支持模型绑定。 SignalR 提供两个内置中心协议：基于 JSON 的文本协议和基于 MessagePack 的二进制协议。 与 ON 相比 JS，MessagePack 通常会创建较小的消息。 旧版浏览器必须支持 XHR 级别 2 才能提供 MessagePack 协议支持。

> > 中心通过发送包含客户端方法的名称和参数的消息来调用客户端代码。 作为方法参数发送的对象使用配置的协议进行反序列化。 客户端尝试将名称与客户端代码中的方法匹配。 当客户端找到匹配项时，它会调用该方法并将反序列化的参数数据传递给它。


> 不支持 ECMAScript 6 的浏览器 (ES6)

> > SignalR 面向 ES6。 对于不支持 ES6 的浏览器，请将库转译为 ES5。 有关详细信息，请参阅使用 ES6 入门 – 使用 Traceur 和 Babel 将 ES6 转为 ES5。

> SignalR 简单示例

> > 创建 Web 应用项目

> > > 创建 ASP.NET Core Web 应用

> > > 在“配置新项目”对话框中，为“项目名称”输入 SignalRChat。 请务必将项目命名为 SignalRChat（包括匹配大写），以便命名空间与教程中的代码匹配。

> > 添加 SignalR 客户端库

> > > ASP.NET Core 共享框架中包含 SignalR 服务器库。 JavaScript 客户端库不会自动包含在项目中。 对于此教程，使用库管理器 (LibMan) 从 unpkg 获取客户端库。 unpkg 是一个快速的全局内容分发网络，适用于 npm 上的所有内容。

> > > 在“解决方案资源管理器”>中，右键单击项目，然后选择“添加”“客户端库”。

> > > 在“添加客户端库”对话框中：

> > > 为“提供程序”选择“unpkg”

> > > 对于“库”，请输入 @microsoft/signalr@latest。

> > > 选择“选择特定文件”，展开“dist/browser”文件夹，然后选择 signalr.js 和 signalr.min.js。

> > > 将“目标位置”设置为 wwwroot/js/signalr/。

> > > 选择“安装” 。

> > > “添加客户端库”对话框 - 选择库

> > > LibMan 创建 wwwroot/js/signalr 文件夹并将所选文件复制到该文件夹。

> > 创建 SignalR 中心

> > > 中心是一个类，用作处理客户端 - 服务器通信的高级管道。

> > > 在 SignalRChat 项目文件夹中，创建 Hubs 文件夹。

> > > 在 Hubs 文件夹中，使用以下代码创建 ChatHub 类：

> > > C#

```
using Microsoft.AspNetCore.SignalR;

namespace SignalRChat.Hubs
{
    public class ChatHub : Hub
    {
        public async Task SendMessage(string user, string message)
        {
            await Clients.All.SendAsync("ReceiveMessage", user, message);
        }
    }
}

```

> > > ChatHub 类继承自 SignalRHub。 Hub 类管理连接、组和消息。

> > > 可通过已连接客户端调用 SendMessage，以向所有客户端发送消息。 本教程后面部分将显示调用该方法的 JavaScript 客户端代码。 SignalR 代码是异步模式，可提供最大的可伸缩性。

> > 配置 SignalR

> > > 必须将 SignalR 服务器配置为将 SignalR 请求传递给 SignalR。 将以下突出显示的代码添加到 Program.cs 文件。

C#

```
using SignalRChat.Hubs;

var builder = WebApplication.CreateBuilder(args);

// Add services to the container.
builder.Services.AddRazorPages();
builder.Services.AddSignalR();

var app = builder.Build();

// Configure the HTTP request pipeline.
if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Error");
    // The default HSTS value is 30 days. You may want to change this for production scenarios, see https://aka.ms/aspnetcore-hsts.
    app.UseHsts();
}

app.UseHttpsRedirection();
app.UseStaticFiles();

app.UseRouting();

app.UseAuthorization();

app.MapRazorPages();
app.MapHub<ChatHub>("/chatHub");

app.Run();
```

> > > 以上突出显示的代码将 SignalR 添加到 ASP.NET Core 依赖关系注入和路由系统。

> > 添加 SignalR 客户端代码

> > > CSHTML

```
@page
<div class="container">
    <div class="row p-1">
        <div class="col-1">User</div>
        <div class="col-5"><input type="text" id="userInput" /></div>
    </div>
    <div class="row p-1">
        <div class="col-1">Message</div>
        <div class="col-5"><input type="text" class="w-100" id="messageInput" /></div>
    </div>
    <div class="row p-1">
        <div class="col-6 text-end">
            <input type="button" id="sendButton" value="Send Message" />
        </div>
    </div>
    <div class="row p-1">
        <div class="col-6">
            <hr />
        </div>
    </div>
    <div class="row p-1">
        <div class="col-6">
            <ul id="messagesList"></ul>
        </div>
    </div>
</div>
<script src="~/js/signalr/dist/browser/signalr.js"></script>
<script src="~/js/chat.js"></script>
```

> > > JavaScript

```
"use strict";

var connection = new signalR.HubConnectionBuilder().withUrl("/chatHub").build();

//Disable the send button until connection is established.
document.getElementById("sendButton").disabled = true;

connection.on("ReceiveMessage", function (user, message) {
    var li = document.createElement("li");
    document.getElementById("messagesList").appendChild(li);
    // We can assign user-supplied strings to an element's textContent because it
    // is not interpreted as markup. If you're assigning in any other way, you 
    // should be aware of possible script injection concerns.
    li.textContent = `${user} says ${message}`;
});

connection.start().then(function () {
    document.getElementById("sendButton").disabled = false;
}).catch(function (err) {
    return console.error(err.toString());
});

document.getElementById("sendButton").addEventListener("click", function (event) {
    var user = document.getElementById("userInput").value;
    var message = document.getElementById("messageInput").value;
    connection.invoke("SendMessage", user, message).catch(function (err) {
        return console.error(err.toString());
    });
    event.preventDefault();
});
```

## Tensorflow

## C# 调用 Tensorflow

> https://github.com/migueldeicaza/TensorFlowSharp

'''
When to use TensorFlowSharp
TensorFlowSharp is a good runtime to run your existing models, and is mostly a straight binding to the underlying TensorFlow runtime. Most people will want to use a higher-level library for interfacing with TensorFlow.

The library was designed to blend in the .NET ecosystem and use the .NET naming conventions.

I strongly recommend that you use TensorFlow.NET which takes a different approach than TensorFlowSharp, it uses the Python naming convention and has a much broader support for the higher level operations that you are likely to need - and is also actively maintained.

TensorFlowSharp
TensorFlowSharp are .NET bindings to the TensorFlow library published here:

https://github.com/tensorflow/tensorflow

This surfaces the C API as a strongly-typed .NET API for use from C# and F#.

The API surfaces the entire low-level TensorFlow API, it is on par with other language bindings. But currently does not include a high-level API like the Python binding does, so it is more cumbersome to use for those high level operations.

You can prototype using TensorFlow or Keras in Python, then save your graphs or trained models and then load the result in .NET with TensorFlowSharp and feed your own data to train or run.

The current API documentation is here.

Using TensorFlowSharp
Installation
The easiest way to get started is to use the NuGet package for TensorFlowSharp which contains both the .NET API as well as the native libraries for 64-bit Linux, Mac and Windows using the CPU backend.

You can install using NuGet like this:

nuget install TensorFlowSharp
Or select it from the NuGet packages UI on Visual Studio.

On Visual Studio, make sure that you are targeting .NET 4.6.1 or later, as this package uses some features of newer .NETs. Otherwise, the package will not be added. Once you do this, you can just use the TensorFlowSharp nuget

Alternatively, you can download it directly.

Using TensorFlowSharp
Your best source of information right now are the SampleTest that exercises various APIs of TensorFlowSharp, or the stand-alone samples located in "Examples".

This API binding is closer design-wise to the Java and Go bindings which use explicit TensorFlow graphs and sessions. Your application will typically create a graph (TFGraph) and setup the operations there, then create a session from it (TFSession), then use the session runner to setup inputs and outputs and execute the pipeline.

Something like this:

using (var graph = new TFGraph ())
{
    // Load the model
    graph.Import (File.ReadAllBytes ("MySavedModel"));
    using (var session = new TFSession (graph))
    {
        // Setup the runner
        var runner = session.GetRunner ();
        runner.AddInput (graph ["input"] [0], tensor);
        runner.Fetch (graph ["output"] [0]);

        // Run the model
        var output = runner.Run ();

        // Fetch the results from output:
        TFTensor result = output [0];
    }
}
If your application is sensitive to GC cycles, you can run your model as follows. The Run method will then allocate managed memory only at the first call and reuse it later on. Note that this requires you to reuse the Runner instance and not to change the shape of the input data:

// Some input matrices
var inputs = new float[][,] {
    new float[,] { { 1, 2 }, { 3, 4 } },
    new float[,] { { 2, 4 }, { 6, 8 } }
};

// Assumes all input matrices have identical shape
var shape = new long[] { inputs[0].GetLongLength(0), inputs[0].GetLongLength(1) };
var size = inputs[0].Length * sizeof(float);

// Empty input and output tensors
var input = new TFTensor(TFDataType.Float, shape, size);
var output = new TFTensor[1];

// Result array for a single run
var result = new float[1, 1];

using (var graph = new TFGraph())
{
    // Load the model
    graph.Import(File.ReadAllBytes("MySavedModel"));
    using (var session = new TFSession(graph))
    {
        // Setup the runner
        var runner = session.GetRunner();
        runner.AddInput(graph["input"][0], input);
        runner.Fetch(graph["output"][0]);

        // Run the model on each input matrix
        for (int i = 0; i < inputs.Length; i++)
        {
            // Mutate the input tensor
            input.SetValue(inputs[i]);

            // Run the model
            runner.Run(output);

            // Fetch the result from output into `result`
            output[0].GetValue(result);
        }
    }
}
In scenarios where you do not need to setup the graph independently, the session will create one for you. The following example shows how to abuse TensorFlow to compute the addition of two numbers:

using (var session = new TFSession())
{
    var graph = session.Graph;

    var a = graph.Const(2);
    var b = graph.Const(3);
    Console.WriteLine("a=2 b=3");

    // Add two constants
    var addingResults = session.GetRunner().Run(graph.Add(a, b));
    var addingResultValue = addingResults.GetValue();
    Console.WriteLine("a+b={0}", addingResultValue);

    // Multiply two constants
    var multiplyResults = session.GetRunner().Run(graph.Mul(a, b));
    var multiplyResultValue = multiplyResults.GetValue();
    Console.WriteLine("a*b={0}", multiplyResultValue);
}
Here is an F# scripting version of the same example, you can use this in F# Interactive:

#r @"packages\TensorFlowSharp.1.4.0\lib\net471\TensorFlowSharp.dll"

open System
open System.IO
open TensorFlow

// set the path to find the native DLL
Environment.SetEnvironmentVariable("Path", 
    Environment.GetEnvironmentVariable("Path") + ";" + __SOURCE_DIRECTORY__ + @"/packages/TensorFlowSharp.1.2.2/native")

module AddTwoNumbers = 
    let session = new TFSession()
    let graph = session.Graph

    let a = graph.Const(new TFTensor(2))
    let b = graph.Const(new TFTensor(3))
    Console.WriteLine("a=2 b=3")

    // Add two constants
    let addingResults = session.GetRunner().Run(graph.Add(a, b))
    let addingResultValue = addingResults.GetValue()
    Console.WriteLine("a+b={0}", addingResultValue)

    // Multiply two constants
    let multiplyResults = session.GetRunner().Run(graph.Mul(a, b))
    let multiplyResultValue = multiplyResults.GetValue()
    Console.WriteLine("a*b={0}", multiplyResultValue)
Working on TensorFlowSharp
If you want to work on extending TensorFlowSharp or contribute to its development read the CONTRIBUTING.md file.

Please keep in mind that this requires a modern version of C# as this uses some new capabilities there. So you will want to use Visual Studio 2017.

Possible Contributions
Build More Tests
Would love to have more tests to ensure the proper operation of the framework.

Samples
The binding is pretty much complete, and at this point, I want to improve the API to be easier and more pleasant to use from both C# and F#. Creating samples that use Tensorflow is a good way of finding easy wins on the usability of the API, there are some here:

https://github.com/tensorflow/models

Packaging
Mobile: we need to package the library for consumption on Android and iOS.

Documentation Styling
The API documentation has not been styled, I am using the barebones template for documentation, and it can use some work.

Issues
I have logged some usability problems and bugs in Issues, feel free to take on one of those tasks.

Documentation
Much of the online documentation comes from TensorFlow and is licensed under the terms of Apache 2 License, in particular all the generated documentation for the various operations that is generated by using the tensorflow reflection APIs.

Last API update: Release 1.9
'''

## gRPC 

### gRPC 概述

```
gRPC 是一种与语言无关的高性能远程过程调用 (RPC) 框架。

gRPC 的主要优点是：

现代高性能轻量级 RPC 框架。
协定优先 API 开发，默认使用协议缓冲区，允许与语言无关的实现。
可用于多种语言的工具，以生成强类型服务器和客户端。
支持客户端、服务器和双向流式处理调用。
使用 Protobuf 二进制序列化减少对网络的使用。
这些优点使 gRPC 适用于：

效率至关重要的轻量级微服务。
需要多种语言用于开发的 Polyglot 系统。
需要处理流式处理请求或响应的点对点实时服务。


 GRPC是google开源的一个高性能、跨语言的RPC框架，基于HTTP2协议，基于protobuf 3.x，基于Netty 4.x +。GRPC与thrift、avro-rpc等其实在总体原理上并没有太大的区别，简而言之GRPC并没有太多突破性的创新。（如下描述，均基于JAVA语言的实现）

    对于开发者而言：

    1）需要使用protobuf定义接口，即.proto文件

    2）然后使用compile工具生成特定语言的执行代码，比如JAVA、C/C++、Python等。类似于thrift，为了解决跨语言问题。

    3）启动一个Server端，server端通过侦听指定的port，来等待Client链接请求，通常使用Netty来构建，GRPC内置了Netty的支持。

    4）启动一个或者多个Client端，Client也是基于Netty，Client通过与Server建立TCP长链接，并发送请求；Request与Response均被封装成HTTP2的stream Frame，通过Netty Channel进行交互。
```

### gRPC 服务项目模板

```
对 .proto 文件的 C# 工具支持
gRPC 使用协定优先方法进行 API 开发。 在 .proto 文件中定义服务和消息：

ProtoBuf

复制
syntax = "proto3";

service Greeter {
  rpc SayHello (HelloRequest) returns (HelloReply);
}

message HelloRequest {
  string name = 1;
}

message HelloReply {
  string message = 1;
}

通过在项目中包含 .proto 文件，可自动生成用于服务、客户端和消息的 .NET 类型：

将包引用添加到 Grpc.Tools 包。
将 .proto 文件添加到 <Protobuf> 项目组。

XML
<ItemGroup>
  <Protobuf Include="Protos\greet.proto" />
</ItemGroup>
有关 gRPC 工具支持的详细信息，请参阅使用 C# 的 gRPC 服务。

ASP.NET Core 上的 gRPC 服务
gRPC 服务可以托管在 ASP.NET Core 上。 这些服务与日志记录、依赖关系注入 (DI)、身份验证和授权等 ASP.NET Core 功能完全集成。

将 gRPC 服务添加到 ASP.NET Core 应用
gRPC 需要 Grpc.AspNetCore 包。 若要了解如何在 .NET 应用中配置 gRPC，请查看配置 gRPC。
```

### ASP.NET Core gRPC 服务项目模板提供了一个入门版服务：

```
public class GreeterService : Greeter.GreeterBase
{
    private readonly ILogger<GreeterService> _logger;

    public GreeterService(ILogger<GreeterService> logger)
    {
        _logger = logger;
    }

    public override Task<HelloReply> SayHello(HelloRequest request,
        ServerCallContext context)
    {
        _logger.LogInformation("Saying hello to {Name}", request.Name);
        return Task.FromResult(new HelloReply 
        {
            Message = "Hello " + request.Name
        });
    }
}
GreeterService 继承自 GreeterBase 类型，后者是从 .proto 文件的 Greeter 服务生成的。 Startup.csProgram.cs 中的客户端可以访问该服务：

app.MapGrpcService<GreeterService>();
若要详细了解 ASP.NET Core 上的 gRPC 服务，请参阅使用 ASP.NET Core 的 gRPC 服务。

```

### 使用 .NET 客户端调用 gRPC 服务

```
gRPC 客户端是从 .proto 文件生成的具体客户端类型。 具体 gRPC 客户端具有转换为 .proto 文件中 gRPC 服务的方法。

var channel = GrpcChannel.ForAddress("https://localhost:5001");
var client = new Greeter.GreeterClient(channel);

var response = await client.SayHelloAsync(
    new HelloRequest { Name = "World" });

Console.WriteLine(response.Message);
gRPC 客户端是使用通道创建的，该通道表示与 gRPC 服务的长期连接。 可以使用 GrpcChannel.ForAddress 创建通道。

有关创建客户端、调用不同服务方法的详细信息，请参阅使用 .NET 客户端调用 gRPC 服务。
```

## Php

### Pyplot，画出各种你想要的图

> https://blog.csdn.net/qq_42257666/article/details/122439666

## Python

## Java

## 低代码平台

> 低代码开发平台（LCDP）是无需编码（0代码）或通过少量代码就可以快速生成应用程序的开发平台。通过可视化进行应用程序开发的方法，使具有不同经验水平的开发人员可以通过图形化的用户界面，使用拖拽组件和模型驱动的逻辑来创建网页和移动应用程序。低代码开发平台（LCDP）的正式名称直到2014年6月才正式确定，整个低代码开发领域却可以追溯到更早前第四代编程语言和快速应用开发工具。

### Microsoft Platform 

> 其包括 Power Apps, Power Apps Sutdio ,Power Apps Mobile, Power Platform Admin Center。

> Power BI 商业表格 Power Apps 创建app Power Pages 网页 Power Automate 自动化流程 Power Virtual Agents。 聊天机器人

> PCF（Power Apps Component Framework） 为程序员提供利用代码开发自定义组件。

> Microsoft Dataverse 存储和管理业务应用程序使用的数据

> 流程自动化。

## 工业自动化

### 变频器

### 伺服

### 可编程逻辑控制器

### 人机交互 HMI

### 传感器

### 电机

### PAC智能控制器

### CNC控制器

### 仪表

### 基于PC的控制器

### 识别

### 工业机器人机械臂系统

## 工业软件

### 自动化软件

#### TIA Portal

> 用于集成自动化项目的主要组件和功能的工程组态系统。

#### 控制器软件

> STEP 7产品系列用于SIMATIC S7控制器系统的组态、编程、测试和诊断。

#### 人机界面软件

> HMI 软件包括面板组态软件、基于 PC 的可视化软件以及 SCADA 系统。

#### SCADA软件

> 从过程可视化到工厂智能或基础设施项目的开放式系统的软件解决方案。

#### 用于能源管理的软件

> 能源管理软件包括现场层的能量数据记录到管理层的公司范围能量分析。


COMOS 工厂工程软件
COMOS 工厂工程软件

制造运营管理软件

产品生命周期管理软件

SIMIT 仿真软件
适用于 SIRIUS 开关装置的软件
适用于 SIRIUS 开关装置的软件
XHQ 运营智能软件
XHQ 运营智能软件

面向过程工业的西门子工业套件
PlantSight 
PlantSight 

## 备注

> 最后修改时间：2023-04-18 16:48