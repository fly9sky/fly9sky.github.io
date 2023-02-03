---
layout: post
title: OpenWrtDockerCloudDrive
description: OpenwrtX86的的相关资料遗迹使用x86docker 玩转 DockerCloudDrive
date: 2023-01-30 20:58:01
---

### 安装

### 软件源（23.03.3X86 要注意版本和处理器架构，不然可能会出现不兼容的问题）

> 从官方软件园下载相关.img文件,一定要注意平台架构。
> 启动WinPE，用DiskGenius删除索要安装硬盘的所有分区，确定。不要进行分区操作。
> 下载physdiskwrite和img文件放在一个目录下，然后cmd进入相关目录，执行 physdiskwrite -u xxx.img。 然后按需输入磁盘号和输入yes 。
> 完毕后重启，硬盘引导即可进入系统进行相关配置。

#### 阿里 （似乎缺少一些系统工具，例如block-mount ）

```
src/gz ali_core https://mirrors.aliyun.com/openwrt/releases/22.03.3/targets/x86/64/packages

src/gz ali_base https://mirrors.aliyun.com/openwrt/releases/22.03.3/packages/x86_64/base

src/gz ali_luci https://mirrors.aliyun.com/openwrt/releases/22.03.3/packages/x86_64/luci

src/gz ali_packages https://mirrors.aliyun.com/openwrt/releases/22.03.3/packages/x86_64/packages

src/gz ali_routing https://mirrors.aliyun.com/openwrt/releases/22.03.3/packages/x86_64/routing

src/gz ali_telephony https://mirrors.aliyun.com/openwrt/releases/22.03.3/packages/x86_64/telephony
```

#### 官方

> 速度比较慢，尤其是安装大点的软件更慢，建议国内软件园没有相关软件时切换到官方软件源，否则就不要使用官方软件源。

```
src/gz openwrt_core https://downloads.openwrt.org/releases/22.03.3/packages/x86_64/packages

src/gz openwrt_base https://downloads.openwrt.org/releases/22.03.3/packages/x86_64/base

src/gz openwrt_luci https://downloads.openwrt.org/releases/22.03.3/packages/x86_64/luci

src/gz openwrt_packages https://downloads.openwrt.org/releases/22.03.3/packages/x86_64/packages

src/gz openwrt_routing https://downloads.openwrt.org/releases/22.03.3/packages/x86_64/routing

src/gz openwrt_telephony https://downloads.openwrt.org/releases/22.03.3/packages/x86_64/telephony
```

### 系统存储控件的扩容（使用系统剩余未分区空间）

#### 安装 工具

> opkg update

> opkg install cfdisk fdisk e2fsprogs

> opkg install block-mount 官方的Openwrt默认不带这个

#### cfdisk 划分空间

> fdisk -l 可以检查是否划分成功

> mkfs.ext4 /dev/sda3 具体按你的分区

> block-mount 挂载 /sda3 作为根文件系统使用。 Save and Apply

#### 执行扩容脚本（block-mount挂在后又提示 mount /dev/sda3 /tmp/extroot这句种的设备改成你的就好了）

```
mkdir -p /tmp/introot
mkdir -p /tmp/extroot
mount --bind / /tmp/introot
mount /dev/sda3 /tmp/extroot
tar -C /tmp/introot -cvf - . | tar -C /tmp/extroot -xf -
umount /tmp/introot
umount /tmp/extroot
reboot
```

#### 使用外置硬盘跟这个过程一致只是你挂在的事另一块而已，注意设别名称即可

### 安装Docker 

> 在openwrt中挂载一个 /opt 分区作为储存Docker数据分区；

> 重启openwrt reboot 。

> 手动更新软件包 opkg update ；

> 手动安装Docker opkg install docker ，opkg install dockerd ；

> 手动启动运行Docker /etc/init.d/dockerd start ；

> 设置自启动，通过 ssh 输入 ln -s /etc/init.d/dockerd /etc/rc.d/S100docker 。


### Docker pull  clouddrive

> https://registry.hub.docker.com/r/cloudnas/clouddrive/tags

> arm32: docker pull cloudnas/clouddrive:arm32

> arm: docker pull cloudnas/clouddrive:arm64

> x86：docker pull cloudnas/clouddrive:amd64

### Run 

```
docker run -d --name clouddrive --restart unless-stopped -v /opt/CloudNAS:/CloudNAS:shared -v /opt/CloudNAS/Config:/Config -p 9798:9798 --privileged --device /dev/fuse:/dev/fuse cloudnas/clouddrive

root@OpenWrt:~# docker run -d --name clouddrive --restart unless-stopped -v /opt/CloudNAS:/CloudNAS:shared -v /opt/CloudNAS/Config:/Config -p 9798:9798 --privileged --device /dev/fuse:/dev/fuse cloudnas/clouddrive
74860fdddf7fcd95a33325750a9ee7a95836080d7abd25951458ad4848bcb9ca
docker: Error response from daemon: path /opt/CloudNAS is mounted on / but it is not a shared mount.
root@OpenWrt:~#  Error response from daemon: path /opt/CloudNAS is mounted on / but it is not a shared mount.

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

mount --make-shared /
mount --make-shared /Clouddrive


docker run -d \
--name clouddrive \
--restart unless-stopped \
-v /opt/Clouddrive:/CloudNAS:shared \
-v /opt/Clouddrive/Config:/Config \
--network host \
--pid host \
--privileged \
--device /dev/fuse:/dev/fuse \
cloudnas/clouddrive


```

> 有时候运行clouddrive容器会出现挂载私有问题 需要执行

```
mount --make-shared /
```

> 内核版本有问题出现过错误

```
24f9eb7da835: Extracting  14.97MB/14.97MB
CloudDrive failed to register layer: operation not supported
```

### 配置 smaba

> /etc/samba/smb.conf

```
[CloudDrive]

  path = /storage/Clouddrive/CloudDrive/

  available = yes

  browseable = yes

  public = yes

  writeable = yes

24f9eb7da835: Extracting  14.97MB/14.97MB

CloudDrive failed to register layer: operation not supported
```