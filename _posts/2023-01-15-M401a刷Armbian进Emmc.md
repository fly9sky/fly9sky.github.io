---
layout: post
title: M401a刷Armbian进Emmc
description: M401a刷Armbian进Emmc
date: 2023-01-13 09:01:01
---

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
