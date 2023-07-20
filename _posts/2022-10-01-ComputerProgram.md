---
layout: post
title: 计算机编程
description: 计算机科学相关学习内容总结,各种编程语言以及计算机数据结构等总结梳理
date: 2022-10-01 09:01:01
updatedate: 2023-07-20 11:31:01
---

- [计算机史话](#计算机史话)
- [数据结构与算法](#数据结构与算法)
  - [数据结构](#数据结构)
    - [逻辑结构](#逻辑结构)
    - [线性结构](#线性结构)
  - [算法](#算法)
  - [指针与数组](#指针与数组)
  - [字符串与模式匹配](#字符串与模式匹配)
  - [链表](#链表)
  - [递归](#递归)
  - [集合与字典](#集合与字典)
  - [排序](#排序)
- [HTML 5](#html-5)
- [JQuery](#jquery)
  - [GET](#get)
  - [POST](#post)
  - [AJAX](#ajax)
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
- [gRPC](#grpc)
  - [gRPC 概述](#grpc-概述)
  - [gRPC 服务项目模板](#grpc-服务项目模板)
  - [ASP.NET Core gRPC 服务项目模板提供了一个入门版服务：](#aspnet-core-grpc-服务项目模板提供了一个入门版服务)
  - [使用 .NET 客户端调用 gRPC 服务](#使用-net-客户端调用-grpc-服务)
- [Php](#php)
  - [Pyplot，画出各种你想要的图](#pyplot画出各种你想要的图)
- [Python](#python)
  - [语言特点](#语言特点)
    - [跨平台](#跨平台)
      - [可远行于](#可远行于)
        - [各大操作系统](#各大操作系统)
    - [解释型脚本语言](#解释型脚本语言)
      - [内建](#内建)
        - [高级的数据结构](#高级的数据结构)
    - [面向对象的语言](#面向对象的语言)
      - [便于](#便于)
        - [数据和逻辑](#数据和逻辑)
    - [动态语言](#动态语言)
      - [变量本身](#变量本身)
        - [类型不固定](#类型不固定)
        - [可随意转换](#可随意转换)
        - [不需要声明](#不需要声明)
    - [不用考虑](#不用考虑)
      - [内存问题](#内存问题)
    - [可处理的数据量](#可处理的数据量)
      - [无限制](#无限制)
    - [默认编码](#默认编码)
      - [UTF-8](#utf-8)
  - [运行程序](#运行程序)
    - [两种模式](#两种模式)
      - [脚本式编程](#脚本式编程)
        - [一次性执行](#一次性执行)
      - [交互式编程](#交互式编程)
        - [逐行输入](#逐行输入)
    - [远行脚本](#远行脚本)
      - [命令行/终端模式](#命令行终端模式)
        - [python \*.py](#python-py)
      - [Linux下可执行脚本](#linux下可执行脚本)
        - [首行添加](#首行添加)
        - [赋予权限](#赋予权限)
        - [运行脚本](#运行脚本)
      - [IPython](#ipython)
        - [%run \*.py](#run-py)
  - [代码格式](#代码格式)
    - [缩进](#缩进)
      - [用【缩进深度】区分](#用缩进深度区分)
        - [语句【代码块】](#语句代码块)
    - [行长](#行长)
      - [每行不超过80字符](#每行不超过80字符)
    - [空行](#空行)
      - [将程序的不同部分分开](#将程序的不同部分分开)
    - [\\ ](#)
      - [继续上一行](#继续上一行)
      - [跨行特例](#跨行特例)
        - [闭合操作符](#闭合操作符)
        - [三引号](#三引号)
    - [;](#-1)
      - [在同一行](#在同一行)
        - [连接多个语句](#连接多个语句)
    - [:](#-2)
      - [分开代码块(组)](#分开代码块组)
        - [头\&体](#头体)
  - [变量](#变量-1)
    - [内涵](#内涵)
      - [存储了一个值](#存储了一个值)
        - [与【变量】相关联的信息](#与变量相关联的信息)
    - [命名规则](#命名规则)
      - [只能包含](#只能包含)
        - [字母、数字和下划线](#字母数字和下划线)
      - [不能](#不能)
        - [以【数字】打头](#以数字打头)
        - [包含【空格】](#包含空格)
        - [使用python保留字：用于【特殊用途】的单词](#使用python保留字用于特殊用途的单词)
      - [建议](#建议)
        - [简短又具有描述性](#简短又具有描述性)
        - [使用【小写字母】](#使用小写字母)
        - [慎用](#慎用)
  - [变量赋值](#变量赋值)
    - [赋值符](#赋值符)
      - [=](#-3)
    - [增量赋值](#增量赋值)
      - [+=](#-4)
    - [多重赋值](#多重赋值)
      - [x=y=z=1](#xyz1)
    - [多元赋值](#多元赋值)
      - [x,y,z=1,2,'a'](#xyz12a)
        - [\*var收集多余的值](#var收集多余的值)
      - [通常【元组】需要【小括号】](#通常元组需要小括号)
      - [建议](#建议-1)
        - [加上【小括号】以增加【可读性】](#加上小括号以增加可读性)
        - [(x,y,z)=(1,2,'a')](#xyz12a-1)
    - [变量交换](#变量交换)
      - [x,y=y,x](#xyyx)
- [LabView](#labview)
  - [LabⅥEW基础知识](#labⅵew基础知识)
  - [前面板设计](#前面板设计)
  - [程序框图与程序结构](#程序框图与程序结构)
  - [数值字符串与布尔运算](#数值字符串与布尔运算)
  - [数组、矩阵与簇](#数组矩阵与簇)
      - [数组、矩阵和簇控件](#数组矩阵和簇控件)
      - [列表框、树形控件和表格](#列表框树形控件和表格)
      - [容器控件](#容器控件)
      - [实例——数组分类](#实例数组分类)
      - [数组的组成](#数组的组成)
      - [实例——创建数组控件](#实例创建数组控件)
      - [实例——创建多维数组控件](#实例创建多维数组控件)
      - [数组函数](#数组函数)
      - [实例——比较数组](#实例比较数组)
      - [实例——选项卡数组](#实例选项卡数组)
      - [簇的组成](#簇的组成)
      - [创建簇](#创建簇)
      - [实例——创建簇控件](#实例创建簇控件)
      - [实例——调整“簇”控件顺序](#实例调整簇控件顺序)
      - [簇函数](#簇函数)
      - [实例——使用“捆绑”函数创建“簇”控件](#实例使用捆绑函数创建簇控件)
      - [创建矩阵](#创建矩阵)
      - [矩阵函数](#矩阵函数)
      - [实例——创建矩阵控件](#实例创建矩阵控件)
      - [实例——矩阵变换](#实例矩阵变换)
    - [综合实例——矩形的绘制](#综合实例矩形的绘制)
  - [数据图形显示](#数据图形显示)
  - [数学函数](#数学函数)
  - [波形运算](#波形运算)
    - [信号生成](#信号生成)
  - [文件管理](#文件管理)
  - [数据采集](#数据采集)
  - [通信技术](#通信技术)
- [认证授权](#认证授权)
  - [认证](#认证)
  - [Token](#token)
    - [SAML](#saml)
    - [JWT](#jwt)
    - [SSO 与CAS](#sso-与cas)
  - [授权](#授权)
    - [OAuth 授权](#oauth-授权)

## 计算机史话

> 阿兰图灵是通用计算机的提出者，但是在有些问题上效率十分低下。

> 图灵机，又称图灵计算机指一个抽象的机器，是，英国数学家艾伦・麦席森・图灵(1912―-1954年)于1936年提出的一种抽象的计算模型，即将人们使用纸笔进行数学运算的过程进行抽象，由一个虚拟的机器替代人类进行数学运算。它有一条无限长的纸带，纸带分成了一个一个的小方格，每个方格有不同的颜色。有一个机器头在纸带上移来移去。机器头有一组内部状态，还有一些固定的程序。在每个时刻，机器头都要从当前纸带上读入一个方格信息，然后结合自己的内部状态查找程序表，根据程序输出信息到纸带方格上，并转换自己的内部状态，然后进行移动

> 最早的存储指令结构计算机模型实际是由ENIAC创建者埃可特和莫奇利，冯诺依曼与以上二位共同商议，1944年9月起草了《EDVAC报告书一号草案》，并署名，且为埃可特和莫奇利留了署名位置，但戈德斯塔提前发表了这份报告导致埃可特和莫奇利没有书名，所以现在存储程序计算机的逻辑结构成了广为人知的“冯诺依曼体系结构”。明确提出了，存储程序，顺序执行指令，使用二进制开关电路。并且这个体系产生了两个新的工程学科，计计算机体系结构和软件工程。冯诺依曼把计算机硬件划分为：CA（中央运算单元）CC（中央控制单元）M（内存）I（输入设备）O（输出设备。）

> 第一台冯诺依曼体系计算机1948年6月研制出原型机"Baby"由英国团队研制出来。

> 二战期间英国的计算机水平非常厉害，但是英国政府隐瞒了计算机方面研究的成就，包括阿兰图林一度不为人所知，因此导致美国冯诺依曼体系结构成了以后计算机的主要设计思想。

> 香农定律是关于信道容量的计算的一个经典定律，可以说是信息论的基础。

> Bug 一次是女程序员葛蕾丝霍普引入。

## 数据结构与算法

### 数据结构

#### 逻辑结构

> 集合结构

> 线性结构

> 树形结构

> 图形结构

#### 线性结构

> 顺序存储结构

> 链式存储结构

### 算法

> 算法复杂度

> >（O(n)渐进表示法）

> > 时间复杂度

> > 空间复杂度

### 指针与数组

> 指针

> > 内存与地址

> > 指针的语法

> > 使用指针变量

> > 函数与参数传递

> 数组

> > 结构型数据类型

> > 数组定义与初始化

> > 数组与指针

> > 数组的抽象数据类型

> 动态内存管理

> > 关键词new 和delete

> > 避免内存错误

### 字符串与模式匹配

> 文本的匹配

> > BF 算法

> > MP 算法

> > KMP 算法

> > BM 算法

> > BMH 算法

> 文本的模糊匹配

> > 全局编辑距离

> > 局部***佳对准

> > N 元距离模型

### 链表

> 单向链表

> > 单向链表的结构

> > 单向链表的操作算法

> > 有序链表的合并算法

> 单向循环链表

> > 单向循环链表的结构

> > 单向循环链表的实现

> > 约瑟夫环的问题

> > 魔术师发牌问题

> > 拉丁方阵的问题

> 双向循环链表

> > 双向循环链表的结构

> > 双向循环链表的实现

> > 维吉尼亚加密法问题

> 游标类的设计与实现

> > 游标类的结构

> > 游标类的实现

> > 遍历

> > 元素的插入与删除

> 先进先出与后进先出

> 排队的智慧

> 优先级队列--兼谈页面置换算法

### 递归

> 递归的概念，定义，原则，递归和非递归的转化

> 分治法

> > > 分治法简述

> > > 汉诺塔问题

> > > 传染病问题

> 回溯法

> > > 回溯法简述

> > > 迷宫问题

> > > 八皇后问题

> 树

> > 花开二枝分外香--二叉树及相关算法

> > > 二叉树的定义

> > > 二叉树的性质

> > > 二叉树的实现

> > > 二叉树的遍历算法

> > > 二叉树线索化算法

> > 从树到森林

> > > 树的存储表示

> > > 树的实现

> > > 树与森林的遍历算法

> > > 森林与二叉树的转换

> > 哈夫曼树--***优二叉树编码算法

> > > 哈夫曼编码

> > > 构造哈夫曼树

> > > 哈夫曼编码的实现

> 堆

> > 堆的概念

> > 堆的建立

> > 堆的操作

> 图

> > 图的存储与表示

> > > 图的邻接矩阵表示

> > > 图的邻接表表示

> > > 两种表示法的比较

> > 图的遍历

> > > 欧拉路径与欧拉回路

> > > 哈密尔顿路径与哈密尔顿回路

> > > 广度优先遍历算法

> > > 深度优先遍历算法

> > 最短短路径问题

> > > 固定起点***短路径问题

> > > 非固定起点***短路径问题

> > > ***短路径的动态规划解法

> > 图的最小生成树

> > > 图的最小生成树的定义

> > > 克鲁斯卡尔算法

> > > 普里姆算法

> 树形搜索结构

> > 二叉搜索树

> > > 二叉搜索树的概念

> > > 二叉搜索树的操作

> > > 二叉搜索树的实现

> > > 二叉搜索树的分析

> > 自平衡的二叉搜索树--**L 树

> > > **L 树的概念

> > > **L 树的旋转

> > > **L 树的实现

> > 树中亦有"红与黑"

> > > 红黑树的概念

> > > 红黑树的操作

> > > 红黑树的实现

> > 基于Trie 树的单词检索

> > > Trie 树的概念

> > > Trie 树的表示

> > > Trie 树的实现

### 集合与字典

> 集合的概念，运算，实现

> > 位向量集合

> > 单链表集合

> 字典

> > 字典的概念

> > 搜索运算

> 散列

> > 散列的概念

> > 散列函数

> > 字符串散列

> > 处理散列冲突

> 不相交集

> > 不相交集的概念

> > 不相交集的实现

> > 犯罪团伙的问题

> > 路径压缩的实现

> STL 中的set

### 排序

> 插入排序

> > 直接插入排序

> > 二分插入排序

> > 希尔排序

> 选择排序

> > 直接选择排序

> > 堆排序

> 交换排序

> > 冒泡排序

> > 鸡尾酒排序

> > 快速排序

> 归并排序

> 计数排序

> 线性表

> > 顺序表(增，删，查，改，销毁)

> > > 静态顺序表

> > > 动态顺序表

> 链表(增，删，查，改，销毁)

> > 单链表

> > > 无头双链表

> > > 有头单链表

> > 双链表

> > > 无头双链表

> > > 有头双链表

> > > 无头循环双链表

> > > 有头循环双链表

> > 三链表

> > 链表的逆序

> > > 无头链表的删除和插入

> > > 链表带环问题

> 栈和队列

> > 栈和队列的创建

> > 栈和队列的初始化

> > 栈的增容

> > 入栈，出栈，入队，出队

> > 取得栈顶，队头和队尾元素

> > 求栈和队列的大小，判断栈和队列是否为空

> > 栈

> 一种特殊的线性表，其只允许在固定的一端进行插入和删除元素操作

> > 顺序队列

> > >顺序栈

> > >链式栈

> > >栈的应用

> 队列

> > 循环队列

> > 优先级队列

> > 队列的应用

> 树形结构

> > 节点

> > 节点的度

> > 叶节点

> > 分支节点

> > 祖先节点

> > 双亲节点

> > 兄弟节点

> > 孩子节点

> > 树的深度

> > 树的表示方法

> > > 双亲表示法

> > > 孩子表示法

> > > 双亲孩子表示法

> > > 孩子兄弟表示法

> > > 树的存储形式

> > > > 二叉树

> > 二叉树的存储

> > > 顺序存储结构

> > > 链式存储结构

> > 二叉树的基本操作

> > > 二叉树的创建

> > > 二叉树的遍历(递归和非递归)

> > > > 前序遍历

> > > > 中序遍历

> > > > 后序遍历

> > > > 后序遍历

> > > 二叉树的增、删、查、改、销毁

> > > 线索化二叉树

> > > > 堆

> > 堆的概念,创建

> > > 大堆

> > > 小堆

> > > 堆的插入和删除

> > > 堆的应用

> > > > 优先级队列

> > > > 海量数据top K问题

> > > > 堆排序（高校排序算法）

> > > > huffman树

> 搜索

> > 线性查找

> > > 顺序查找：从前往后依次遍历O(n)

> > > 顺序有序查找：二分查找O(log(N))

> > > 索引顺序表

> > 树形查找

> > > 二叉树结构

> 二叉搜索树

> 平衡树

 > AVL树

 > 红黑树

> > > 多叉树结构

> B-树

> B+树

> B*树

> > 哈希查找

> > > 哈希表

> > > > 哈希冲突及解决方法

> > > 哈希函数

> > > > 哈希冲突——开散列

> > > > 哈希冲突——闭散列

> > > 哈希表变形

> > > > 哈希表变形——位图

> > > > 哈希表变形——布隆过滤器

> 排序

> > 插入排序

> > > 直接插入排序

> > > 希尔排序

> > 选择排序

> > > 选择排序

> > > 堆排序

> > 交换排序

> > > 冒泡排序

> > > 快速排序

> > 归并排序

## HTML 5

## JQuery

### GET

> $.get('/data.ashx?type=all', '', function (data) {

>             //alert(JSON.stringify(data));

>             //将获得得数据原路发回进行测试

> })      

### POST

> $.post("/data.ashx?type=add", JSON.stringify(data[0]), function (rs, textStatus) {

>                 alert(JSON.stringify(rs));

>             }, "json");

### AJAX

> > 此方式比较详细可以调用POST，也可以GET ,以上GET POST 则非常简单。

> $.ajax({

>     url: "/data.ashx?type=add",

>     type: "POST",

>     data: JSON.stringify(data[0]),

>     contentType: "application/json; charset=utf-8",

>     dataType: "json",

>     success: function (rs) {

>         alert(JSON.stringify(rs));

>     }

> });

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

$small-range:  (0em, 40em);    /* 0, 640px */

$medium-range: (40.063em, 64em); /* 641px, 1024px */

$large-range:  (64.063em, 90em); /* 1025px, 1440px */

$xlarge-range: (90.063em, 120em); /* 1441px, 1920px */

$xxlarge-range: (120.063em);    /* 1921px */

 

// Defining media queries

$screen:    "only screen" !default;

$landscape:  "#{$screen} and (orientation: landscape)" !default;

$portrait:   "#{$screen} and (orientation: portrait)" !default;

$small-up:   $screen !default;

$small-only:  "#{$screen} and (max-width: #{upper-bound($small-range)})" !default;

$medium-up:  "#{$screen} and (min-width:#{lower-bound($medium-range)})" !default;

$medium-only: "#{$screen} and (min-width:#{lower-bound($medium-range)}) and (max-width:#{upper-bound($medium-range)})" !default;

$large-up:   "#{$screen} and (min-width:#{lower-bound($large-range)})" !default;

$large-only:  "#{$screen} and (min-width:#{lower-bound($large-range)}) and (max-width:#{upper-bound($large-range)})" !default;

$xlarge-up:  "#{$screen} and (min-width:#{lower-bound($xlarge-range)})" !default;

$xlarge-only: "#{$screen} and (min-width:#{lower-bound($xlarge-range)}) and (max-width:#{upper-bound($xlarge-range)})" !default;

$xxlarge-up:  "#{$screen} and (min-width:#{lower-bound($xxlarge-range)})" !default;

$xxlarge-only: "#{$screen} and (min-width:#{lower-bound($xxlarge-range)}) and (max-width:#{upper-bound($xxlarge-range)})" !default;

 

// Usage

@media #{$small-up}   { ... }

@media #{$small-only}  { ... }

@media #{$medium-up}  { ... }

@media #{$medium-only} { ... }

@media #{$large-up}   { ... }

@media #{$large-only}  { ... }

@media #{$xlarge-up}  { ... }

@media #{$xlarge-only} { ... }

@media #{$xxlarge-up}  { ... }

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

> 3. 可配置的mixin(With a configurable mixin )

<为了解决上面的两个问题，我们须要从断点mixin中抽出一个列表，仅仅剩下mixin核心，然后这个列表就能够随便移动，或者扔到配置文件中。

然后，使用sass 3.3+中的maps，我们能够方便的使用关联的属性和属性值。

$breakpoints: (

 'small' : 767px,

 'medium' : 992px,

 'large' : 1200px

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

 'small' : ( min-width: 767px ),

 'medium' : ( min-width: 992px ),

 'large' : ( min-width: 1200px )

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

 mobile: 320px,

 tablet: 740px,

 desktop: 980px,

 wide:  1300px

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

### Sass

#### 变量

#### 嵌套归斥责

#### 导入

#### SASS 混合器 混合器继承

> 混合器 Sass中的混合器类似于js的函数，将一段代码定义成混合器以实现代码的重用 编译后其实会转换成正常的css

> 声明混合器：@mixin mixName 

> 调用混合器 @include minName 如

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

 

继承只会在生成css时复制选择器，而不会复制大段的css属性 如果不小心会让生成css中包含大量的选择器复制 避免这种情况的最好办法： 不要在继承css规则中使用后代选择器如

 

 .dsf{}

 .foo .bar {

 @extend dsf //不推荐

 }

## Font Awesome

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

```

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

```

XML

```

<ItemGroup>

 <Protobuf Include="Protos\greet.proto" />

</ItemGroup>

```

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

### 语言特点

#### 跨平台

##### 可远行于

###### 各大操作系统

#### 解释型脚本语言

##### 内建

###### 高级的数据结构

#### 面向对象的语言

##### 便于

###### 数据和逻辑

####### 相分离

#### 动态语言

##### 变量本身

###### 类型不固定

###### 可随意转换

###### 不需要声明

#### 不用考虑

##### 内存问题

#### 可处理的数据量

##### 无限制

#### 默认编码

##### UTF-8

### 运行程序

#### 两种模式

##### 脚本式编程

###### 一次性执行

####### 源代码脚本

##### 交互式编程

###### 逐行输入

####### 再执行

#### 远行脚本

##### 命令行/终端模式

###### python *.py

##### Linux下可执行脚本

###### 首行添加

####### #!/usr/local/bin/python

####### #!/usr/bin/env python

###### 赋予权限

####### chmod 755 *.py

###### 运行脚本

####### *.py

##### IPython

###### %run *.py

### 代码格式

#### 缩进

##### 用【缩进深度】区分

###### 语句【代码块】

#### 行长

##### 每行不超过80字符

#### 空行

##### 将程序的不同部分分开

#### \ 

##### 继续上一行

##### 跨行特例

###### 闭合操作符

####### [],{},()

###### 三引号

####### 常用于【多行注释】

#### ;

##### 在同一行

###### 连接多个语句

#### :

##### 分开代码块(组)

###### 头&体

### 变量

#### 内涵

##### 存储了一个值

###### 与【变量】相关联的信息

#### 命名规则

##### 只能包含

###### 字母、数字和下划线

##### 不能

###### 以【数字】打头

###### 包含【空格】

###### 使用python保留字：用于【特殊用途】的单词

####### 关键字

####### 函数名

##### 建议

###### 简短又具有描述性

###### 使用【小写字母】

###### 慎用

####### 小写字母l

####### 大写字母O

####### 易与1&0混淆

### 变量赋值

#### 赋值符

##### =

#### 增量赋值

##### +=

#### 多重赋值

##### x=y=z=1

#### 多元赋值

##### x,y,z=1,2,'a'

###### *var收集多余的值

##### 通常【元组】需要【小括号】

##### 建议

###### 加上【小括号】以增加【可读性】

###### (x,y,z)=(1,2,'a')

#### 变量交换

##### x,y=y,x

## LabView

### LabⅥEW基础知识

> LabⅥEW编程环境

> > 前面板

> > 程序框图

> > 菜单栏

> > 工具栏

> > 项目浏览器窗口

> Xcontrol

> > XControl对于用户来说，和普通的控件没有区别，但XControl对于开发者来说，除了有自定义外观外，还能自定义行为。

> > 可以将控件的功能封装起来，使其和应用程序代码分离。同时有助于重用。

> 创建XControl

> > 新建XCtrl：

> > Data.ctl: 指定了XCtrl的数据类型；

> > State.ctl: 指定了除数据类型之外其他影响XCtrl外观的信息，其他所有数据的定义放在此处；

> > Init.vi: 当XCtrl第一次被放置在前面板上或含有XCtrl的vi第一次被载入内存时，初始化显示状态。

> > 新建Method，定义XCtrl支持的方法（类似于类的成员函数），用于操作State中的数据；这里实现各种具体的操作。

> > 新建Property，定义了XCtrl的可读取属性（类似于LabVIEW类的accessor的工作），用于读取XCtrl中的数据；

> > 修改facade vi，用于定制XControl的外观，创建各种状态改变事件。

> > X控件的本质是为控件事先定义好一系列可以响应的事件，之后使用控件时，就可以在控件的属性或调用节点中看到这些事件，像操作普通控件一样，调用这些节点来执行特定操作。

> > 以LabVIEW自带的摄氏华氏温度转换XCtrl为例：

### 前面板设计

> 前面板

> >  “工具”选板

> >  图标/连接器

> >  选板可见性设置

>  前面板控件

> >  “控件”选板

> >  控件样式

>  对象的设置

> >  选择对象

> >  删除对象

> >  变更对象位置

> >  属性节点

>  设置前面板的外观

> >  改变对象的大小

> >  改变对象的颜色

> >  设置对象的字体

> 菜单设计

> > 菜单编辑器

> >  “菜单”函数

### 程序框图与程序结构

> 程序框图

> 循环结构

> >  For循环及并行循环

> >  移位寄存器

> >  While循环

> >  反馈节点

> 条件结构

> 顺序结构

> 事件结构

> 程序框图禁用结构

> 条件禁用结构

> 定时循环

> 定时循环和定时顺序结构

> 配置定时循环和定时顺序结构

> 同步开始定时结构和中止定时结构的执行

> 公式节点

> 程序逻辑的公式节点

### 数值字符串与布尔运算

> 数值控件

> 数值型控件

> 布尔型控件和单选按钮

> 字符串与路径控件

> 数值运算

> 数值函数

> 三角函数

> 字符串运算

> 字符串常量

> 字符串函数

> 其余运算

> 布尔运算

> 比较运算

> 定时运算

> 图形与声音运算

### 数组、矩阵与簇

> 数组控件

##### 数组、矩阵和簇控件

##### 列表框、树形控件和表格

##### 容器控件

##### 实例——数组分类

> 数组

##### 数组的组成

##### 实例——创建数组控件

##### 实例——创建多维数组控件

##### 数组函数

##### 实例——比较数组

##### 实例——选项卡数组

> 簇

##### 簇的组成

##### 创建簇

##### 实例——创建簇控件

##### 实例——调整“簇”控件顺序

##### 簇函数

##### 实例——使用“捆绑”函数创建“簇”控件

> 矩阵

##### 创建矩阵

##### 矩阵函数

##### 实例——创建矩阵控件

##### 实例——矩阵变换

#### 综合实例——矩形的绘制

### 数据图形显示

> 图形控件

> 图形和图表

> 下拉列表与枚举控件

> I/O控件

> 修饰控件

> 对象和应用程序的引用

> .NET与ActiveX控件

> 图表图形

> 波形图

> 波形图表

> > XY图

> > 强度图

> > 强度图表

> > 二维图形

> > 罗盘图

> > 误差线图

> > 羽状图

> > XY曲线矩阵

> > 三维图形

> > 三维曲面图

> > 三维参数图

> > 三维曲线图

> > 极坐标图

### 数学函数

> 数学函数运算

> 线性代数Ⅵ

> 特殊矩阵

> 矩阵的基本运算

> 矩阵的分解

> 特征值

> 线性方程组

> 初等与特殊函数

> 指数函数

> 双曲函数

> 离散数学

> 贝塞尔曲线

> Gamma函数

> 超几何函数

> 椭圆积分函数

> 指数积分函数

> 误差函数

> 椭圆与抛物函数

> 拟合Ⅵ

> 曲线拟合

> 拟合函数

> 内插与外推Ⅵ

> 概率与统计Ⅵ

> 累积分布函数（连续）

> 逆累积分布函数（连续

> 累积分布函数（离散）

> 逆累积分布函数（离散）

> 方差分析Ⅵ

> 很优化Ⅵ

> 微分方程Ⅵ

> 多项式Ⅵ

### 波形运算

> 波形数据

> 变体函数

> 时间标识

> 波形生成

> 基本函数发生器

> 正弦波形

> 公式波形

> 基本混合单频

> 混合单频与噪声波形

> 基本带幅值混合单频

> 混合单频信号发生器

> 均匀白噪声波形

> 周期性随机噪声波形

> 伯努利噪声波形

> 仿真信号

> 基本波形函数

> 获取波形成分

> 创建波形

> “设置波形属性”函数和“获取波形属性”函数

> “索引波形数组”函数

> “获取波形子集”函数

> 模拟波形

> 数字波形Ⅵ和函数

> 波形调理

> 数字FIR滤波器

> 数字IIR滤波器

> 按窗函数缩放

> 波形对齐（连续）

> 波形对齐（单次）

> 连续卷积（FIR）

> 滤波器

> 对齐和重采样

> 触发与门限

> 波形测量

> 基本平均直流——均方根

> 瞬态特性测量

> 提取单频信息

> 快速傅里叶变换频谱（幅度——相位）

> 频率响应函数（幅度——相位）

> 频谱测量

> 失真测量

> 幅值和电平测量

> 波形监测

> 信号生成与处理

> 信号生成

> 基于持续时间的信号发生器

> 混合单频与噪声

> 高斯调制正弦波

> 正弦信号

> 正弦波

> 均匀白噪声

> 任意波形发生器

> 信号运算

> 卷积和相关ExpressⅥ

> 缩放和映射

> 窗

> 滤波器

> 巴特沃斯滤波器

> 切比雪夫滤波器

> FIR加窗滤波器

> 贝塞尔滤波器

> 谱分析

> 变换

> FFT

> FHT

> 反FFT

> 反FHT

> 逐点

#### 信号生成

> 信号运算

> > 滤波器

> > 谱分析

> > 变换

> > 线性代数

### 文件管理

> 文件数据

> 路径

> 文件I/O格式

> 文件操作

> 文件常量

> 文件类型

> 文本文件

> 带分隔符电子表格文件

> 二进制文件

> 配置文件

> TDMS

> 存储/数据插件

> Zip文件

> XML格式

> 波形文件I/O函数

> 不错文件函数

> 数据记录文件的创建和读取

> 记录前面板数据

> 数据与XML格式间的相互转换

### 数据采集

> 数据采集基础

> DAQ功能概述

### 通信技术

> 串行通信技术

> 串行通信介绍

> ⅥSA配置串口

> DataSocket技术

> > 读取DataSocket

> > 写入DataSocket

> > 打开DataSocket

> > 关闭DataSocket

> TCP

> > TCP侦听

> > 打开TCP连接

> > 读取TCP数据

> > 写入TCP数据

> UDP通信

## 认证授权

### 认证

> Session-Cookie

Session-Cookie 的认证流程如下：用户先使用用户名和密码登录，登录完成后后端将用户信息存在session 中，把sessionId 写到前端的cookie 中，后面每次操作带着cookie 去后端，只要后端判断sessionId 没问题且没过期就不需要再次登录。

使用这种方式进行认证，开发者可能面临的主要问题如下：

cookie 安全性问题，攻击者可以通过xss 获取cookie 中的sessinId，使用 httpOnly 在一定程度上提高安全性

cookie 不能跨域传输

session 存储在服务器中，所以session 过多会耗费较大服务器资源

### Token

与上面的Session-Cookie 机制不同的地方在于，基于token 的用户认证是一种服务端无状态的认证方式，服务端可以不用存放token 数据，但是服务器可以验证token 的合法性和有效性。

使用token 进行认证的方式这里主要介绍两种：

#### SAML

> SAML (Security Assertion Markup Language) 

未登录的用户通过浏览器访问资源网站（Service Provider，简称SP）

SP 发现用户未登录，将页面重定向至IdP（Identity Provider）

IdP 验证请求无误后，提供表单让用户进行登录

用户登录成功后，IdP 生成并发送SAML token (一个很大的XML对象) 给SP

SP 对token 进行验证，解析获取用户信息，允许用户访问相关资源

#### JWT

JSON Web Token 入门教程（预计阅读时间：2mins）

简言之，JWT 就是一种在用户登录后生成token 并把token 放在前端，后端不需要维护用户的状态信息但是可以验证token 有效性的认证及状态管理方式。 


#### SSO 与CAS
接下来我们探讨一个企业应一定绕不过的课题：单点登录。

举例来说，华为云下有若干云服务。包含项目管理、代码托管、代码检查、流水线、编译构建、部署、自动化测试等众多微服务的DevCloud（软件开发云） 正是其中之一，用户如果在使用任意一个服务没有登录的时候都可以去同一个地方进行登录认证，登录之后的一段时间内可以无需登录访问所有其他服务。

在单点登录领域，CAS（Central Authentication Service，中文名是中央认证服务） 是一个被高频使用的解决方案。因此，这里介绍一下利用CAS 实现SSO。而CAS 的具体实现又可以依赖很多种协议，比如OpenID、OAuth、SAML 等，这里重点介绍一下CAS 协议。

CAS 协议中的几个重要概念
简单介绍一下CAS 协议中的几个重要概念，一开始看概念可能很模糊，可以先过一遍，再结合下面的流程图来理解。

CAS Server：用于认证的中心服务器

CAS Clients：保护CAS 应用，一旦有未认证的用户访问，重定向至CAS Server 进行认证

TGT & TGC：用户认证之后，CAS Server 回生成一个包含用户信息的TGT (Ticket Granting Ticket) 并向浏览器写一个cookie（TGC，Ticket Granting Cookie），有啥用后面流程会讲到

ST：在url 上作为参数传输的ticket，受保护应用可以凭借这个ticket 去CAS Server 确认用户的认证是否合法 

### 授权


#### OAuth 授权

OAuth 的设计本意更倾向于授权而不是认证，所以这一小节的标题写的是授权，但是其实在授权的同时也已经完成了认证。


OAuth 2 是一个授权框架，或称授权标准，它可以使第三方应用程序或客户端获得对HTTP服务上（例如 Google，GitHub ）用户帐户信息的有限访问权限。OAuth 2 通过将用户身份验证委派给托管用户帐户的服务以及授权客户端访问用户帐户进行工作。综上，OAuth 2 可以为 Web 应用 和桌面应用以及移动应用提供授权流程。

本文将从OAuth 2 角色，授权许可类型，授权流程等几方面进行讲解。

在正式讲解之前，这里先引入一段应用场景，用以与后文的角色讲解对应。

开发者A注册某IT论坛后，发现可以在信息栏中填写自己的 Github 个人信息和仓库项目，但是他又觉得手工填写十分麻烦，直接提供 Github 账户和密码给论坛管理员帮忙处理更是十分智障。
不过该论坛似乎和 Github 有不可告人的秘密，开发者A可以点击“导入”按钮，授权该论坛访问自己的 Github 账户并限制其只具备读权限。这样一来， Github 中的所有仓库和相关信息就可以很方便地被导入到信息栏中，账户隐私信息也不会泄露。
这背后，便是 OAuth 2 在大显神威。

2. OAuth2 角色
OAuth 2 标准中定义了以下几种角色：

资源所有者（Resource Owner）
资源服务器（Resource Server）
授权服务器（Authorization Server）
客户端（Client）
2.1 资源所有者（Resource Owner）
资源所有者是 OAuth 2 四大基本角色之一，在 OAuth 2 标准中，资源所有者即代表授权客户端访问本身资源信息的用户（User），也就是应用场景中的“开发者A”。客户端访问用户帐户的权限仅限于用户授权的“范围”（aka. scope，例如读取或写入权限）。

如果没有特别说明，下文中出现的"用户"将统一代表资源所有者。

2.2 资源/授权服务器（Resource/Authorization Server）
资源服务器托管了受保护的用户账号信息，而授权服务器验证用户身份然后为客户端派发资源访问令牌。

在上述应用场景中，Github 既是授权服务器也是资源服务器，个人信息和仓库信息即为资源（Resource）。而在实际工程中，不同的服务器应用往往独立部署，协同保护用户账户信息资源。

2.3 客户端（Client）
在 OAuth 2 中，客户端即代表意图访问受限资源的第三方应用。在访问实现之前，它必须先经过用户者授权，并且获得的授权凭证将进一步由授权服务器进行验证。

如果没有特别说明，下文中将不对"应用"，“第三方应用”，“客户端”做出区分。

3. OAuth 2 的授权流程
目前为止你应该对 OAuth 2 的角色有了些概念，接下来让我们来看看这几个角色之间的抽象授权流程图和相关解释。

请注意，实际的授权流程图会因为用户返回授权许可类型的不同而不同。但是下图大体上能反映一次完整抽象的授权流程。



Authrization Request
客户端向用户请求对资源服务器的authorization grant。
Authorization Grant（Get）
如果用户授权该次请求，客户端将收到一个authorization grant。
Authorization Grant（Post）
客户端向授权服务器发送它自己的客户端身份标识和上一步中的authorization grant，请求访问令牌。
Access Token（Get）
如果客户端身份被认证，并且authorization grant也被验证通过，授权服务器将为客户端派发access token。授权阶段至此全部结束。
Access Token（Post && Validate）
客户端向资源服务器发送access token用于验证并请求资源信息。
Protected Resource（Get）
如果access token验证通过，资源服务器将向客户端返回资源信息。