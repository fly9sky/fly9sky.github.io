---
layout: post
title:  计算机科学相关学习内容总结
description: 计算机科学相关学习内容总结,包括各种操作系统安装配置，各种编程语言学习等
date: 2022-10-01 09:01:01
---

- [计算机史话](#计算机史话)
- [Windows](#windows)
- [LinuxAndOpenSource](#linuxandopensource)
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
- [C# 调用 Tensorflow](#c-调用-tensorflow)
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

> Install :sudo apt-get -y install docker.io

> docker image ls # 列出当前环境下的镜像

> docker images   # 列出当前环境下的镜像

> docker image rm ididididid      # 安装id删除镜像

> 操作容器

> docker run -i -t --rm centos /bin/bash   # 启动一个centos容器并进入，此时容器是干干净净，没有一点东西的，do everything

> docker container kill container_id    # 杀掉这个容器，强行终止

> docker container rm container_id      # 删除这个容器

> docker container ls            # 查找当前容器

> docker ps // 查看所有正在运行容器

> docker stop containerId // containerId 是容器的ID

> docker ps -a // 查看所有容器

> docker ps -a -q // 查看所有容器ID

> docker stop $(docker ps -a -q) //  stop停止所有容器

> docker  rm $(docker ps -a -q) //   remove删除所有容器

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

> 最后修改时间：2023-03-15 14:46