---
layout: post
title: DockerCloudDrive
description: 使用x86docker 玩转 DockerCloudDrive
date: 2023-01-30 20:58:01
---

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