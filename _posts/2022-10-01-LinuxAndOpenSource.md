---
layout: post
title: LinuxAndOpenSource
description: Linux And OpenSource
date: 2022-10-01 09:01:01
---

## OpenSource主流开源协议

### GPL

> 最开放，只要引用GPL协议的软件必须开源免费，不适合商业软件 有5大自由 使用，复制，修改，衍生，收费。

### LGPL

> 较GPL 宽松

### BSD  

> 发布带源代码 则源代码必须遵循BSD

> 发布只有二进制则必须声明遵循了BSD协议

### Apache 

> 软件以及衍生品必须继续使用Apache许可。

> 修改了源代码则必须声明

> 基于他人源代码则必须保留原始代码的许可商标声明等。

> 类库保护，只正对引用的类库，而无须适用整个软件系统。

> 发布软件中有声明软件则需在此文件中注明基于Apache 和其他协议。

### MIT(MITL)

> 修改后的源代码需要保留作者的许可信息即可。

### Mozilla(MPL)

> 后续只开源使用的特定代码

> 多种协议可以混合使用

> 发布软件附带专门说明文件有原始的代码的修改时间和方式。

## Git in linux 

### Download and Install GithubCli

> https://github.com/cli/cli/releases

### Login 

> $ gh auth login (config use ssh,need your token from github config)

### Git helper 

> $ git clone git@github.com:devgis/MyWriting.git  //need your private key
> 提交修改 上传修改的代码后执行增加修改： 
> $ git add . 
> 增加修改信息： 
> $ git commit -m ‘修改lol清晰增加口径’ 
> 推送分支： 
> $ git push origin main
