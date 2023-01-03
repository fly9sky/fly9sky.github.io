---
layout: post
title: Openwrt上的AdGuardHome安装
date: 2023-01-02 10:01:01
description: Openwrt上的AdGuardHome安装总结
---

> Adguardhome是非常好的一款广告拦截软件。其原理就是对广告请求的dns进行拦截，当然了其功能十分强大，还需继续研究。这里只从简单的那幢说起。

> 安装  luci-app-adguardhome

> 更新核心 这里记住不需要单独去安装adguardhome更新核心后会自动安装。

> AdGuardHome 未运行未重定向 这时候在后台ssh执行

```
chmod 755 /etc/init.d/AdGuardHome
service AdGuardHome restart
```

> AdGuardHome 运行中未重定向 核心版本:v0.102.0 没有配置文件no core没有核心

```
这时候登录http://192.168.2.1:3000/install.html进行配置既可。，注意ip改成你自己的ip。
网页端口改 所有3000
dns服务 所有55你也可以自己改 默认的53端口已经被占用
```

> 配置成功后会有如下提示:

```
配置您的设备
为保证 AdGuard Home 可以开始正常工作，您需要在设备上对其进行配置。
AdGuard Home DNS 服务器正在监听以下地址:
127.0.0.1:55
192.168.0.50:55
192.168.2.1:55
[::1]:55
[fdad:ca6e:cd0b::1]:55


恭喜
AdGuardHome 运行中已重定向
```

> 这时候在openwrt后台查看 AdGuardHome 已经正常运行了。