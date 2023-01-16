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

> 经过漫长安装后系统在安装完成后会自动重启，可以关注路由器里边的设备列表，重启后IP地址会发生改变，重新登陆既可。进入后线关机，拔出U盘，重新启动既可。
