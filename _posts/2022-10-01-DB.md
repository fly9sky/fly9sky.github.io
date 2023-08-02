---
layout: post
title: 数据库
description: 各种数据库Oracle、Sql Server相关知识学习梳理
date: 2022-10-01 09:01:01
updatedate: 2022-05-24 13:51:01
---

- [数据库基础](#数据库基础)
  - [锁](#锁)
    - [数据库角度](#数据库角度)
      - [\* 独占锁（Exclusive Lock）](#-独占锁exclusive-lock)
      - [共享锁（Shared Lock）](#共享锁shared-lock)
      - [更新锁（Update Lock）](#更新锁update-lock)
    - [程序员角度](#程序员角度)
      - [乐观锁（Optimistic Lock）](#乐观锁optimistic-lock)
      - [悲观锁（Pessimistic Lock）](#悲观锁pessimistic-lock)
  - [数据库中事务的 ](#数据库中事务的)
    - [ACID 原则](#acid-原则)
      - [原子性 (Atomicity)：](#原子性-atomicity)
      - [一致性 (Consistency)：](#一致性-consistency)
      - [隔离性(Isolation)：](#隔离性isolation)
      - [持久性(Durability)：](#持久性durability)
- [NoSQL](#nosql)
  - [键值数据库](#键值数据库)
  - [文档数据库](#文档数据库)
  - [列族数据库](#列族数据库)
  - [图数据库](#图数据库)
- [Oracle](#oracle)
  - [数据库结构](#数据库结构)
    - [体系结构](#体系结构)
      - [实例](#实例)
      - [数据库](#数据库)
        - [数据文件](#数据文件)
        - [控制文件](#控制文件)
        - [日志文件](#日志文件)
    - [服务器结构](#服务器结构)
      - [系统全局区](#系统全局区)
        - [数据高速缓冲区](#数据高速缓冲区)
        - [重做日志缓冲区](#重做日志缓冲区)
        - [共享池](#共享池)
        - [Large Pool](#large-pool)
      - [后台进程](#后台进程)
        - [DBWn](#dbwn)
        - [LGWR](#lgwr)
        - [SMON](#smon)
        - [PMON](#pmon)
        - [ARCH](#arch)
        - [......](#)
      - [程序全局区](#程序全局区)
    - [数据字典](#数据字典)
      - [数据字典构成](#数据字典构成)
        - [USER\_](#user_)
        - [ALL\_](#all_)
        - [DBA\_](#dba_)
        - [V$\_](#v_)
        - [GV\_](#gv_)
      - [常用数据字典](#常用数据字典)
  - [SQL语言](#sql语言)
    - [DDL](#ddl)
      - [create](#create)
        - [常用数据类型](#常用数据类型)
        - [表](#表)
        - [主键](#主键)
        - [外键](#外键)
        - [约束](#约束)
        - [索引](#索引)
        - [视图](#视图)
        - [序列](#序列)
        - [同义词](#同义词)
      - [drop](#drop)
      - [alter](#alter)
    - [DML](#dml)
      - [insert](#insert)
        - [插入数据](#插入数据)
        - [复制表数据](#复制表数据)
      - [update](#update)
      - [merge](#merge)
      - [delete](#delete)
      - [truncate](#truncate)
    - [DQL](#dql)
      - [select](#select)
        - [from子句](#from子句)
        - [投影](#投影)
        - [where子句](#where子句)
        - [基本函数](#基本函数)
        - [集合操作](#集合操作)
        - [子查询](#子查询)
    - [DCL](#dcl)
    - [TCL](#tcl)
  - [PL/SQL](#plsql)
    - [概述](#概述)
    - [PL/SQL编程](#plsql编程)
      - [基本语言块](#基本语言块)
      - [字符集](#字符集)
      - [注释](#注释)
      - [数据类型](#数据类型)
      - [变量和常量](#变量和常量)
      - [表达式和运算符](#表达式和运算符)
      - [流程控制](#流程控制)
        - [if-then-elsif-then-else](#if-then-elsif-then-else)
        - [case-when-else](#case-when-else)
        - [loop-exit](#loop-exit)
        - [for-loop](#for-loop)
        - [while-loop](#while-loop)
    - [过程和函数](#过程和函数)
      - [过程](#过程)
      - [函数](#函数)
    - [错误处理](#错误处理)
      - [预定义异常](#预定义异常)
        - [DUP\_VAL\_ON\_INDEX](#dup_val_on_index)
        - [LOGIN\_DENIED](#login_denied)
        - [NO\_DATA\_FOUND](#no_data_found)
        - [TOO\_MANY\_ROWS](#too_many_rows)
        - [ZERO\_DIVIDE](#zero_divide)
        - [VALUE\_ERROR](#value_error)
        - [CASE\_NOT\_FOUND](#case_not_found)
      - [自定义异常](#自定义异常)
        - [RAISE](#raise)
      - [异常函数](#异常函数)
        - [SQLCODE](#sqlcode)
        - [QLERRM](#qlerrm)
    - [包](#包)
      - [包头](#包头)
      - [包体](#包体)
      - [重载](#重载)
    - [集合](#集合)
      - [三种类型](#三种类型)
        - [index-by表](#index-by表)
        - [嵌套表](#嵌套表)
        - [可变数组](#可变数组)
      - [属性和方法](#属性和方法)
        - [COUNT](#count)
        - [DELETE](#delete-1)
        - [EXISTS](#exists)
        - [EXTEND](#extend)
        - [FIRST/LAST](#firstlast)
        - [NEXT/PRIOR](#nextprior)
    - [游标](#游标)
      - [显示游标](#显示游标)
      - [隐式游标](#隐式游标)
      - [游标for循环](#游标for循环)
      - [游标变量](#游标变量)
  - [数据库管理](#数据库管理)
    - [管理控制文件](#管理控制文件)
    - [管理日志文件](#管理日志文件)
    - [管理表空间和数据文件](#管理表空间和数据文件)
    - [模式对象管理](#模式对象管理)
    - [表分区和索引分区](#表分区和索引分区)
    - [用户管理与安全](#用户管理与安全)
    - [数据完整性和数据约束](#数据完整性和数据约束)
  - [数据库优化](#数据库优化)
    - [系统调整](#系统调整)
    - [SQL语句优化](#sql语句优化)
      - [常用优化技巧](#常用优化技巧)
        - [不要用\*代替列名](#不要用代替列名)
        - [用truncate代替delete](#用truncate代替delete)
        - [在确保完整性的情况下多用commit语句](#在确保完整性的情况下多用commit语句)
        - [尽量减少表查询的次数](#尽量减少表查询的次数)
        - [用not exists代替in/not in](#用not-exists代替innot-in)
        - [用not exists代替distinct](#用not-exists代替distinct)
        - [有效利用共享游标](#有效利用共享游标)
        - [以合理的方式使用函数](#以合理的方式使用函数)
      - [表的连接方法](#表的连接方法)
        - [选择from表的顺序](#选择from表的顺序)
        - [选择驱动表](#选择驱动表)
        - [where子句的连接顺序](#where子句的连接顺序)
      - [有效使用索引](#有效使用索引)
        - [索引列的选择](#索引列的选择)
        - [复合索引有时比单列索引有更好的性能](#复合索引有时比单列索引有更好的性能)
        - [避免对大表的全表扫描](#避免对大表的全表扫描)
        - [监视索引是否被使用](#监视索引是否被使用)
      - [优化器](#优化器)
      - [执行计划管理](#执行计划管理)
      - [SQL重演](#sql重演)
  - [备份与恢复](#备份与恢复)
    - [RMAN(Recovery Manager)工具](#rmanrecovery-manager工具)
    - [闪回技术](#闪回技术)
      - [flashback](#flashback)
      - [show recyclebin](#show-recyclebin)
    - [数据导入/导出](#数据导入导出)
      - [导出exp](#导出exp)
      - [导入imp](#导入imp)
  - [数据库集群技术](#数据库集群技术)
    - [RAC应用](#rac应用)
    - [ASM](#asm)
    - [容灾和数据卫士](#容灾和数据卫士)
    - [故障诊断](#故障诊断)
  - [商业智能与数据仓库](#商业智能与数据仓库)
    - [多维数据库](#多维数据库)
    - [数据挖掘](#数据挖掘)
  - [数据库事务隔离级别](#数据库事务隔离级别)
    - [已提交读模式](#已提交读模式)
    - [串行模式](#串行模式)
    - [只读模式](#只读模式)
- [SQL Server](#sql-server)
  - [DDL](#ddl-1)
  - [DML](#dml-1)
  - [存储过程](#存储过程)
  - [索引](#索引-1)
    - [聚集索引](#聚集索引)
    - [非聚集索引](#非聚集索引)
  - [数据优化](#数据优化)
  - [并发](#并发)
  - [灾难恢复](#灾难恢复)
  - [RAC](#rac)
  - [行列转换](#行列转换)
    - [行转列PIVOT](#行转列pivot)
    - [列转行UNPIVOT](#列转行unpivot)
  - [SQL 事务隔离级别:](#sql-事务隔离级别)
    - [read uncommited（读取未提交数据），](#read-uncommited读取未提交数据)
    - [read commited（读取已提交数据）读取的默认方式，](#read-commited读取已提交数据读取的默认方式)
    - [repeatable read（可重复读），](#repeatable-read可重复读)
    - [serializable（可序列化），](#serializable可序列化)
    - [snapshot（快照），](#snapshot快照)
    - [read commited snapshot（已经提交读隔离）](#read-commitedsnapshot已经提交读隔离)
    - [Sql Server 事务隔离级别的查看及更改](#sql-server-事务隔离级别的查看及更改)
- [LiteDB：本地化NOSQL](#litedb本地化nosql)
  - [特点](#特点)
  - [LiteDB使用基本案例](#litedb使用基本案例)
    - [创建实体类](#创建实体类)
    - [使用Demo](#使用demo)
  - [使用场景](#使用场景)
  - [LiteDB的技术细节](#litedb的技术细节)
    - [LiteDB的工作原理](#litedb的工作原理)
    - [LiteDB的查询](#litedb的查询)
    - [LiteDB的查询示例](#litedb的查询示例)

## 数据库基础

### 锁

#### 数据库角度

##### * 独占锁（Exclusive Lock）

> 独占锁锁定的资源只允许进行锁定操作的程序使用，其它任何对它的操作均不会被接受。

> 执行数据更新命令，即INSERT、 UPDATE 或DELETE 命令时，SQL Server 会自动使用独占锁。

> 但当对象上有其它锁存在时，无法对其加独占锁。独占锁一直到事务结束才能被释放。

##### 共享锁（Shared Lock）

> 共享锁锁定的资源可以被其它用户读取，但其它用户不能修改它。

> 在SELECT 命令执行时，SQL Server 通常会对对象进行共享锁锁定。

> 通常加共享锁的数据页被读取完毕后，共享锁就会立即被释放。

##### 更新锁（Update Lock）

> 更新锁是为了防止死锁而设立的。当SQL Server 准备更新数据时，它首先对数据对象作更新锁锁定，这样数据将不能被修改，但可以读取。等到SQL Server 确定要进行更新数据操作时，

> 它会自动将更新锁换为独占锁。但当对象上有其它锁存在时，无法对其作更新锁锁定。

#### 程序员角度

##### 乐观锁（Optimistic Lock）

> 乐观锁假定在处理数据时，不需要在应用程序的代码中做任何事情就可以直接在记录上加锁、即完全依靠数据库来管理锁的工作。

> 一般情况下，当执行事务处理时SQL Server会自动对事务处理范围内更新到的表做锁定。

##### 悲观锁（Pessimistic Lock）

> 悲观锁对数据库系统的自动管理不感冒，需要程序员直接管理数据或对象上的加锁处理，并负责获取、共享和放弃正在使用的数据上的任何锁。

### 数据库中事务的 

#### ACID 原则

##### 原子性 (Atomicity)：

> 事务的原子性是指一个事务中包含的一条语句或者多条语句构成了一个完整的逻辑单元，这个逻辑单元具有不可再分的原子性。这个逻辑单元要么一起提交执行全部成功，要么一起提交执行全部失败。

##### 一致性 (Consistency)：

> 可以理解为数据的完整性，事务的提交要确保在数据库上的操作没有破坏数据的完整性，比如说不要违背一些约束的数据插入或者修改行为。一旦破坏了数据的完整性，SQL Server 会回滚这个事务来确保数据库中的数据是一致的。

##### 隔离性(Isolation)：

> 与数据库中的事务隔离级别以及锁相关，多个用户可以对同一数据并发访问而又不破坏数据的正确性和完整性。但是，并行事务的修改必须与其它并行事务的修改相互独立，隔离。但是在不同的隔离级别下，事务的读取操作可能得到的结果是不同的。

##### 持久性(Durability)：

> 数据持久化，事务一旦对数据的操作完成并提交后，数据修改就已经完成，即使服务重启这些数据也不会改变。相反，如果在事务的执行过程中，系统服务崩溃或者重启，那么事务所有的操作就会被回滚，即回到事务操作之前的状态。

## NoSQL

### 键值数据库

> Redis

> BerkeleyDB

> Memcached

> Project Voldemort

> Riak

> LevelDB

### 文档数据库

> MongoDB

> CouchDB

> RavenDB

> Terrastore

> OrientDB

### 列族数据库

> HBase

> Amazon SimpleDB

> Cassdndra

> Hypertable

> BigTable(google)

### 图数据库

> FlockDB

> HyperGraphDB

> Infinite Graph

> Neo4J

> OrientDB

## Oracle

### 数据库结构

#### 体系结构

##### 实例

> 一般情况下Oracle数据库都是一个数据库包含一个实例

##### 数据库

###### 数据文件

####### 表空间

> SYSTEM表空间

> SYSAUX表空间

> 撤销表空间

> USERS表空间

####### 数据文件

> 系统数据

> 用户数据

####### 说明

> 表空间是一个数据库的逻辑区域

> 每个表空间由一个或多个数据文件组成

> 一个数据文件只能属于一个表空间

###### 控制文件

###### 日志文件

####### 重做日志文件

####### 归档日志文件

#### 服务器结构

##### 系统全局区

###### 数据高速缓冲区

###### 重做日志缓冲区

###### 共享池

###### Large Pool

##### 后台进程

###### DBWn

###### LGWR

###### SMON

###### PMON

###### ARCH

###### ......

##### 程序全局区

#### 数据字典

> 存放整个数据库实例重要信息的一组表，多数表归sys用户所有

##### 数据字典构成

###### USER_

> 记录用户对象信息

###### ALL_

> 记录用户的对象信息及被授权访问的对象信息

###### DBA_

> 包含数据库实例的所有对象信息

###### V$_

> 当前实例的动态视图

###### GV_

> 分布式环境下所有实例的动态视图

##### 常用数据字典

> DBA_TABLES(=TABS)

> DBA_TAB_COLUMNS(=COLS)

> DBA_VIEWS

> DBA_SYNONYMS(=SYN)

> DBA_SEQUENCES(=SEQ)

> DBA_CONSTRAINTS

> DBA_INDEXES(=IND)

> DBA_IND_COLUMNS

> DBA_TRIGGERS

> DBA_SOUCE

> DBA_SEGMENTS

> DBA_EXTENTS

> DBA_OBJECTS

### SQL语言

#### DDL

##### create

###### 常用数据类型

> varchar2(n)：变长字符串n<=4000

> char(n)：定长字符串n<=2000

> number(p,s)：p表示精度，s表示小数位数，最大位数是38位

> date：时问日期（7字节）

> binary_float：浮点型，32位

> binary_double：双精度型，64位

> blob：大二进制对象，<=4G

> clob：大字符串对象，<=4G

> bfile：外部的二进制文件

###### 表

###### 主键

> 在创建表时定义主键

> 使用alter table语句定义主键

> 使用alter table修改主键状态

###### 外键

> 在创建表时定义外键

> 使用alter table语句定义外键

> 使用alter table修改外键状态

###### 约束

> check约束

> not null约束

> unique约束

###### 索引

###### 视图

###### 序列

###### 同义词

##### drop

##### alter

#### DML

##### insert

###### 插入数据

###### 复制表数据

> create table…as select…

> insert into…select

##### update

##### merge

##### delete

##### truncate

#### DQL

##### select

###### from子句

###### 投影

###### where子句

####### 比较运算符

> =

> <>

> <

> <=

> >=

> LIKE

> %

> _

> 布尔操作

> OR

> AND

> NOT

> BETWEEN…AND…IN

> order by子句

> asc

> desc

> distinct

> 算数运算：

> +

> -

> *

> /

###### 基本函数

> 字符函数

> concat(c1,c2)

> length(c)

> lower(c)/upper(c)

> ltrim(c)/rtrim(c)/trim(c)

> replace(c1,c2,c3)

> substr(c1,i,j)

> 数字函数

> abs(n)

> acos(n)/asin(n)/atan(n)/cos(n)/sin(n)/tan(n)

> ceil(n)/floor(n)

> exp(n)/ln(n)

> power(n1,n2)

> round(n1,n2)

> sign(n)

> sqrt(n)

> 日期函数

> add_months(d,i)

> last_day(d)

> month_between(d1,d2)

> new_time(d,tz1,tz2)

> sysdate

> 转换函数

> convert(c,dset,sset)

> to_char(x,fmt)

> to_date(c,fmt)

> 分组函数/聚合函数

> AVG

> MAX

> MIN

> SUM

> COUNT

> STDDEV

> VARIANCE

> group by

> having子句

###### 集合操作

> UNION

> INTERSECT

> MINUS

###### 子查询

> 表连接

> 内连接 inner join

> 外连接

> 左外连接

> 右外连接

> 全外连接

> case语句

> decode函数

#### DCL

> grant

> revoke

#### TCL

> commit

> rollback

> savepoint

### PL/SQL

#### 概述

#### PL/SQL编程

##### 基本语言块

##### 字符集

##### 注释

##### 数据类型

##### 变量和常量

##### 表达式和运算符

##### 流程控制

###### if-then-elsif-then-else

###### case-when-else

###### loop-exit

###### for-loop

###### while-loop

#### 过程和函数

##### 过程

##### 函数

#### 错误处理

##### 预定义异常

###### DUP_VAL_ON_INDEX

###### LOGIN_DENIED

###### NO_DATA_FOUND

###### TOO_MANY_ROWS

###### ZERO_DIVIDE

###### VALUE_ERROR

###### CASE_NOT_FOUND

##### 自定义异常

###### RAISE

##### 异常函数

###### SQLCODE

###### QLERRM

#### 包

##### 包头

##### 包体

##### 重载

#### 集合

##### 三种类型

###### index-by表

###### 嵌套表

###### 可变数组

##### 属性和方法

###### COUNT

###### DELETE

###### EXISTS

###### EXTEND

###### FIRST/LAST

###### NEXT/PRIOR

#### 游标

##### 显示游标

##### 隐式游标

##### 游标for循环

##### 游标变量

### 数据库管理

#### 管理控制文件

#### 管理日志文件

#### 管理表空间和数据文件

#### 模式对象管理

#### 表分区和索引分区

#### 用户管理与安全

#### 数据完整性和数据约束

### 数据库优化

#### 系统调整

#### SQL语句优化

##### 常用优化技巧

###### 不要用*代替列名

###### 用truncate代替delete

###### 在确保完整性的情况下多用commit语句

###### 尽量减少表查询的次数

###### 用not exists代替in/not in

###### 用not exists代替distinct

###### 有效利用共享游标

###### 以合理的方式使用函数

##### 表的连接方法

###### 选择from表的顺序

####### 小表放在最右

###### 选择驱动表

###### where子句的连接顺序

####### 能够过滤掉最多记录的的条件放在最右

##### 有效使用索引

###### 索引列的选择

####### where从句频繁使用的列

####### 频繁用于表连接的列

####### 不要将频繁修改的列用作索引

####### 用于函数中的列应当考虑建立函数索引

###### 复合索引有时比单列索引有更好的性能

###### 避免对大表的全表扫描

####### 导致全表扫描的情况

> 查询的表没有索引

> 需要返回所有的行

> 条件中有LIKE且使用了%

> 对索引列使用了函数

> 条件中有IS NULL或IS NOT NULL

###### 监视索引是否被使用

####### alter index idx_name monitoring usage;

##### 优化器

##### 执行计划管理

##### SQL重演

### 备份与恢复

#### RMAN(Recovery Manager)工具

#### 闪回技术

##### flashback

##### show recyclebin

#### 数据导入/导出

##### 导出exp

##### 导入imp

### 数据库集群技术

#### RAC应用

#### ASM

#### 容灾和数据卫士

#### 故障诊断

### 商业智能与数据仓库

#### 多维数据库

#### 数据挖掘

### 数据库事务隔离级别

#### 已提交读模式

> > SET TRANSACTION ISOLATION LEVEL＝READ COMMITTED;

> Oracle 默认使用的事务隔离级别。事务内执行的查询只能看到查询执行前（而非事务开始前）就已经提交的数据。Oracle 的查询永远不会读取脏数据（未提交的数据）。

> Oracle 不会阻止一个事务修改另一事务中的查询正在访问的数据，因此在一个事务内的两个查询的执行间歇期间，数据有可能被其他事务修改。举例来说，如果一个事务内同一查询执行两次，可能会遇到不可重复读取或不存在读取的现象。 

#### 串行模式

> > SET TRANSACTION ISOLATION LEVEL＝ SERIALIZABLE;

> 串行化隔离的事务只能看到事务执行前就已经提交的数据，以及事务内 INSERT ， UPDATE ，及 DELETE 语句对数据的修改。串行化隔离的事务不会出现不可重复读取或不存在读取的现象。 

#### 只读模式

> > SET TRANSACTION＝ READ ONLY;

> 只读事务只能看到事务执行前就已经提交的数据，且事务中不能执行 INSERT ， UPDATE ，及 DELETE 语句。


## SQL Server

### DDL

### DML

### 存储过程

### 索引

#### 聚集索引

#### 非聚集索引

### 数据优化

### 并发

### 灾难恢复

### RAC

### 行列转换

#### 行转列PIVOT

#### 列转行UNPIVOT

### SQL 事务隔离级别:

> > 1、用于控制并发用户如何读写数据的操做。

> > 2、读操作默认使用共享锁；写操作需要使用排它锁。

> > 3、读操作能够控制他的处理的方式，写操作不能控制它的处理方式

> read uncommited（读取未提交数据），

> read commited（读取已提交数据）读取的默认方式，

> repeatable read（可重复读），

> serializable（可序列化），

> snapshot（快照），

> read commited 

> snapshot（已经提交读隔离）（后两个是sql server 2005 里面 引入的）。

> > 隔离的强度依次递增。

> > 隔离级别越高,读操作的请求锁定就越严格,

> > 锁的持有时间久越长;所以隔离级别越高,

> > 一致性就越高,并发性就越低,同时性能也相对影响越大.

#### read uncommited（读取未提交数据），

> > read uncommitted：最低的隔离级别：查询的时候不会请求共享锁，

> 所以不会和排它锁产生冲突（不会等待排它锁执行完），

> 查询效率非常高，速度飞快。但是缺点：会查到“脏数据”

> （排它锁的事务已经将数据修改，还没提交，这个时候查询到的数据 是已经更改过的。如果事务回滚，就是“脏数据”）

> 优点：查询效率非常高，速度非常快。

> 缺点：会产生“脏数据”

> 适用性：

> 适用于 像聊天软件的 聊天记录，会是软件的运行速度非常快。 但是不适用于 商务软件。尤其是银行

set transaction isolation level read uncommitted;

#### read commited（读取已提交数据）读取的默认方式，

> > 读取的默认隔离级别就是read committed 和上面正好相反。

> 如果上面情况，采用read committed 隔离级别查询的话查到的就是还没有更改之前的数据。

> set transaction isolation level read committed;

#### repeatable read（可重复读），

> > 查询的时候会加上共享锁，但是查询完成之后，共享锁就会被撤销。

> 比如一些购票系统，如果查到票了，当买的时候就没有，这是不行的。

> 所以要在查询到数据之后做一些延迟共享锁，进而阻塞排它锁来修改。

> （如果查询的事务没有提交，不会释放共享锁，这个时候独占锁就不能访问这条数据）

> 注意：

> 1、repeatable 只会锁定查询的数据 ，而 其他行数据还可以进行 修改（更新、删除）（下面那条语句共享锁只会锁定 shipperid为4 的行）

> 2、其他进行插入数据，并且插入的数据满足第一次开始事务时的 查询的筛选条件的时候；

> 第二次查询的时候就会将新插入的数据 查询出来。这就叫做“幻读”（解决幻读，需要更高级别的隔离，就是下面的serializable）

> set transaction isolation level repeatable read;

#### serializable（可序列化），

> > 更高级的 隔离。用户解决“幻读”（上面提到的）。

> 就是使用上面的（repeatable read） 加上共享锁 并不撤销，如果锁定的 一行数据，

> 那么 其他的进程 还可以对 其他的数据进行操作，也可以 进行新增和删除的操作。

> 所以如果想要在查询的时候，不能对整张表进行任何操作，

> 那么就要 将表的结构也 锁定  （就需要使用 更强的 锁定）

> set transaction isolation level serializable;

#### snapshot（快照），

> > 为数据产生一个临时数据库，当sql server 数据更新之前将当前数据库复制到 tempdb数据库里面，

> 查询就是从tempdb数据库中查询，但是不能再 使用 snapshot 线程的事务内执行 修改操作，

> 因为不能修改 旧版本数据库（tempdb），会报错。

> snapshot隔离级别，读操作 不适用 共享锁，使用的是“行版本控制”，

> 所以读数据的性能效率很高，但是修改操作性能就降低的很多。

> 因为是将 数据库 中的数据 复制到 tempdb 数据库中，所以不会产生 幻读。

> set transaction isolation level snapshot;

> >带来两个问题：

> > 1、当 另外一个事务 已经提交，但是这边的查询到数据还是没有修改。因为 每次查询到的快照是针对于 本次回话对应的那个 transaction 的，因为在这个事务里面是没有修改的，所以查询到的数据是没有修改的。

> > 2、（更新问题）因为 那边的数据已经是 飞凤公司了，但是这里还是  联邦,所以,在这个事务里面是不能对表进行修改,因为访问的是临时数据库,想要对 数据库修改是不可能的（sql server 就会报错，阻止修改） 

#### read commited snapshot（已经提交读隔离）

> > 读取的默认隔离级别就是read committed 和上面正好相反。

> 如果上面情况，采用read committed 隔离级别查询的话查到的就是还没有更改之前的数据。

> alter database ssdemo set read_committed_snapshot on;

#### Sql Server 事务隔离级别的查看及更改

> 根据自身 Sql Server 的情况来自定义 事务隔离级别，将会更加的满足需求，或提升性能。例如，对于逻辑简单的 Sql Server,完全可以使用 read uncommitted 模式，来减少死锁，减少堵塞， 提升性能和响应。对于此种应用场景应该是蛮多的，但是却没有一个全局设置，你妹呀！

> 这个功能真的很强大，但是不知道微软为什么把它的最大作用域定义为 当前链接，蛋疼，真的很蛋疼，没法全局设置，下面也尽可能详细的解释如何少设置，多舒服的使用吧

> 查看 当前 Sql Server 事务隔离级别 的设置：

> DBCC Useroptions -> isolation level 这一项的 Value 既是当前的设置值

> 但是我不得不说，这个命令几乎是废物，为什么呢，因为 事务隔离级别 的作用域是 当前链接，也就是，你查看的是当前链接的 级别，但是sql server 同时 150+ 个链接是很正常的，其他链接呢，你说蛋疼不，我X

> 设置Sql Server 事务隔离级别

> Sql Server 事务隔离级别 的设置也同样很蛋疼，很纠结，很恶心。但是稍微好一点的是，其设置可以在多个场合，多种方式设置，稍微弥补了一点点.

1. Transact-SQL 语句中的设置

> 就是在当前 SQL 语句中，设置的事务隔离级别只影响当前 sql 语句, 有两种方式：

> > -- the first method

> > select * from Table1 with(nolock) 

> > -- the second method

> > SET TRANSACTION ISOLATION LEVEL Read UnCommitted;

> > select * from Table1 

> > 这种方式比较灵活，可以重点语句重点对待，缺点就是 要设置的实在是太多了，因为这种方式的作用域实在是太小了啊啊啊啊

1. ADO.NET 中的设置

> 使用 System.Data.SqlClient 托管命名空间的 ADO.NET 应用程序可以调用 SqlConnection.BeginTransaction 方法并将 IsolationLevel 选项设置为 Unspecified、Chaos、ReadUncommitted、ReadCommitted、RepeatableRead、Serializable 或 Snapshot。

就是 SqlConnection 中设置了，代码如下：

System.Data.SqlClient.SqlConnection con = new SqlConnection();

con.BeginTransaction(IsolationLevel.ReadUncommitted);

这种方式有点就是作用域范围变大了；缺点就是要在 C## 设置，最要命的是，如果用了ORM，如何让我设置！！！！！！！！！！！！！

当然，还有其他的设置，详情请参考：调整事务隔离级别

这就是蛋疼的功能，如此好的功能，却如此蛋疼的设置，没有一个全局的设置，强烈建议 微软 把 事务隔离级别 的设置放到 sp_configure 里面去

Sql Server 事务隔离级别的解释：

事务指定一个隔离级别，该隔离级别定义一个事务必须与其他事务所进行的资源或数据更改相隔离的程度。隔离级别从允许的并发副作用（例如，脏读或幻读）的角度进行描述。

事务隔离级别控制：

读取数据时是否占用锁以及所请求的锁类型。

占用读取锁的时间。

引用其他事务修改的行的读取操作是否：

在该行上的排他锁被释放之前阻塞其他事务。

检索在启动语句或事务时存在的行的已提交版本。

读取未提交的数据修改。

选择事务隔离级别不影响为保护数据修改而获取的锁。事务总是在其修改的任何数据上获取排他锁并在事务完成之前持有该锁，不管为该事务设置了什么样的隔离级别。对于读取操作，事务隔离级别主要定义保护级别，以防受到其他事务所做更改的影响。

较低的隔离级别可以增强许多用户同时访问数据的能力，但也增加了用户可能遇到的并发副作用（例如脏读或丢失更新）的数量。相反，较高的隔离级别减少了用户可能遇到的并发副作用的类型，但需要更多的系统资源，并增加了一个事务阻塞其他事务的可能性。应平衡应用程序的数据完整性要求与每个隔离级别的开销，在此基础上选择相应的隔离级别。最高隔离级别（可序列化）保证事务在每次重复读取操作时都能准确检索到相同的数据，但需要通过执行某种级别的锁定来完成此操作，而锁定可能会影响多用户系统中的其他用户。最低隔离级别（未提交读）可以检索其他事务已经修改、但未提交的数据。在未提交读中，所有并发副作用都可能发生，但因为没有读取锁定或版本控制，所以开销最少。

ISO 标准定义了下列隔离级别，SQL Server 数据库引擎支持所有这些隔离级别：

未提交读（隔离事务的最低级别，只能保证不读取物理上损坏的数据）

已提交读（数据库引擎的默认级别）

可重复读

可序列化（隔离事务的最高级别，事务之间完全隔离）

隔离级别

脏读

不可重复读

幻读

未提交读

是

是

是

已提交读

否

是

是

可重复读

否

否

是

快照

否

否

否

可序列化

否

否

否

## LiteDB：本地化NOSQL

> LiteDB是一个小型的.NET平台开源的NoSQL类型的轻量级文件数据库。特点是小和快，dll文件只有200K大小，而且支持LINQ和命令行操作，数据库是一个单一文件，类似Sqlite。

> > 官方网站：http://www.litedb.org/

### 特点

> 1.NoSQL文件存储。这是和传统关系型数据库的主要区别；支持实体类的字段更新；

> 2.类似MongoDB的简单API；

> 3.完全使用C#代码,在.NET 4.0环境下编写，核心dll小巧,只有168K;

> 4.支持ACID事务处理；

> 5.可以进行写入失败的恢复；

> 6.存储到文件或者数据流中（类似MongoDB的GridFS）;

> 7.类似Sqlite的单一文件存储；

> 8.支持文件索引，可以进行快速搜索；可以直接存储文件；

> 9.支持Linq查询；【这也许是C#编写最直接的好处】;

> 10.支持命令行操作数据库，官方提供了一个Shell command line;

> 11.完全开源和免费，包括商业使用；

> Serverless NoSQL 文档存储

> 类似于 MongoDB 的简单 API

> 100% C## 代码，支持.NET 3.5 / .NET 4.0 / NETStandard 1.3 / NETStandard 2.0，单 DLL (小于 300kb)

> 支持线程和进程安全

> 支持文档/操作级别的 ACID

> 支持写失败后的数据还原 (日志模式)

> 可使用 DES (AES) 加密算法进行数据文件加密

> 可使用特性或 fluent 映射 API 将你的 POCO类映射为 BsonDocument

> 可存储文件与流数据 (类似 MongoDB 的 GridFS)

> 单数据文件存储 (类似 SQLite)

> 支持基于文档字段索引的快速搜索 (每个集合支持多达16个索引)

> 支持 LINQ 查询

> Shell 命令行 - 试试这个在线版本

> 相当快 - 这里是与 SQLite 的对比结果

> 开源，对所有人免费 - 包括商业应用

### LiteDB使用基本案例

#### 创建实体类

```
public class Customer
{

  public int Id { get; set; }

  public string Name { get; set; }

  public string[] Phones { get; set; }

  public bool IsActive { get; set; }

}
```

#### 使用Demo

> 使用过程首先要添加dll应用，以及引入命名空间：

> using LiteDB;

> 下面是测试代码，会在当前目录下创建一个sample.db的数据库文件：

//打开或者创建新的数据库

```
using (var db = new LiteDatabase("sample.db"))

{

  //获取 customers 集合，如果没有会创建，相当于表

  var col = db.GetCollection<Customer>("customers");

  //创建 customers 实例

  var customer = new Customer

  {

    Name = "John Doe",

    Phones = new string[] { "8000-0000", "9000-0000" },

    IsActive = true

  };

  // 将新的对象插入到数据表中，Id是自增，自动生成的

  col.Insert(customer);

  // 更新实例

  customer.Name = "Joana Doe";

  //保存到数据库

  col.Update(customer);

  // 使用对象的属性，这个方法生成索引，来进行检索

  col.EnsureIndex(x => x.Name);

  //使用LINQ语法来检索

  var results = col.Find(x => x.Name.StartsWith("Jo"));

}

```

> 上述过程很清楚，根据注释理解几乎不用费神。

### 使用场景

> 1.桌面或者本地小型的应用程序

> 2.小型web应用程序

> 3.单个数据库账户或者单个用户数据的存储

> 4.少量用户的并发写操作的应用程序

### LiteDB的技术细节

#### LiteDB的工作原理

> LiteDB是虽然单个文件类型的数据库，但是数据库有很多信息，例如索引，集合，文件等。为了管理这些信息，LiteDB实现了数据库页的概念。

> > 页 是一个拥有4096 字节的 存储相同信息的地址块。也是操作磁盘文件(读写)的最小单元。LiteDB有6种页类型。其作用也不一样，分布是：Header Page，Collection Page，Index Page， Data Page，Extend Page，Empty Page。

> > Data Page的作用是存储核心的数据，是以序列化后的BSON格式来存储。

> > 值得注意的是，如果存储的数据太大，超过page大小，数据块就会使用一个指针指向Extend Page。

> 在上面的代码中，我们初始化数据库是这样的：

> > var db = new LiteDatabase("MyData.db");

> 这种情况比较好用，可以打开或者创建新的数据库，同样也可以使用连接名称来获取，例如：

> > var db = new LiteDatabase("userdb");

> > 这样会直接从connectionStrings找到这个名称的连接。包括了文件名称，使用模式，以及版本信息。一般情况下直接使用第一种即可。LiteDB的数据库连接完整形式是：filename=C:\Path\mydb.db; journal=false; version=5　　

#### LiteDB的查询

> LiteDB的查询必须在相关的查询字段上使用索引，如果没有索引，会默认去创建索引。上面例子中就是创建字段的索引，并查询。LiteDB中查询有2种方法：

> > 1.使用静态的帮助类Query;

> > 2.使用Linq方式，就是类似Demo的方法;

> LiteDB使用Query的查询方式有以下一些方法，详细讲解几个重要的，其他几个大家理解一下，也应该不难，如果有不准确的地方，还请指正： 

> > Query.All 返回所有的数据，可以使用指定的索引字段进行排序

> > Query.EQ 查找返回和指定字段值相等的数据

> > Query.LT/LTE 查找< 或 <= 某个值的数据

> > Query.GT/GTE 查找> 或 >= 某个值的数据

> > Query.Between 查找在指定区间范围内的数据

> > Query.In - 和SQL的in类似吧，查找和列表中值相等的数据

> > Query.Not - 和EQ相反，是不等于某个值的数据

> > Query.StartsWith 查找以某个字符串开头的数据

> > Query.Contains 查找保护某个字符串的数据，这个查询只扫描索引

> > Query.And 2个查询的交集

> > Query.Or 2个查询结果的并集

```
var results = collection.Find(Query.EQ("Name", "John Doe"));

var results = collection.Find(Query.GTE("Age", 25));

var results = collection.Find(Query.And(

  Query.EQ("FirstName", "John"), Query.EQ("LastName", "Doe")

));

var results = collection.Find(Query.StartsWith("Name", "Jo"));
```

> > 注意LiteDB不支持这种表达式：CreationDate == DueDate。

> 下面介绍使用Linq的查询的几个主要方法：

> > FindAll: 查找表或者集合中所有的结果记录

> > FindOne:返回第一个或者默认的结果

> > FindById: 通过索引返回单个结果

> > Find: 使用查询表达式或者linq表达式查询返回结果

```
collection.EnsureIndex(x => x.Name);

var result = collection

  .Find(Query.EQ("Name", "John Doe")) 

  .Where(x => x.CreationDate >= x.DueDate.AddDays(-5)) 

  .OrderBy(x => x.Age)

  .Select(x => new

  { 

    FullName = x.FirstName + " " + x.LastName, 

    DueDays = x.DueDate - x.CreationDate 

  });
```

> 当然还有一些方法如：Count() , Exists(),Min() , Max()等方法。。比较好理解。看看linq表达式的查询案例：

```
var collection = db.GetCollection<Customer>("customer");

var results = collection.Find(x => x.Name == "John Doe");

var results = collection.Find(x => x.Age > 30);

var results = collection.Find(x => x.Name.StartsWith("John") && x.Age > 30);
```


#### LiteDB的查询示例

```
namespace DEVGIS.FA.FAOutTest.Views

{

  

  /// <summary>

  /// SelectDevices.xaml 的交互逻辑

  /// </summary>

  public partial class TestLiteDB

  {

    public TestLiteDB() : base("")

    {

    InitializeComponent();

    this.Loaded += TestLiteDB_Loaded;

    }

    private void TestLiteDB_Loaded(object sender, RoutedEventArgs e)

    {

     InitDB();

    }

    public void InitDB()

    {

      using (var db = new LiteDatabase("sample.db"))

      {

        //获取 customers 集合，如果没有会创建，相当于表

        var col = db.GetCollection<Customer>("customers");

        //创建 customers 实例

        var customer = new Customer

        {

          Name = "John Doe",

          Phones = new string[] { "8000-0000", "9000-0000" },

          IsActive = true

        };

        // 将新的对象插入到数据表中，Id是自增，自动生成的

        col.Insert(customer);

        // 更新实例

        customer.Name = "Joana Doe";

        //保存到数据库

        col.Update(customer);

        // 使用对象的属性，这个方法生成索引，来进行检索

        col.EnsureIndex(x => x.Name);

        //使用LINQ语法来检索

        var results = col.Find(x => x.Name.StartsWith("Jo"));

        tbContent.Text = JsonConvert.SerializeObject(results);

      }

    }

  }

}
```