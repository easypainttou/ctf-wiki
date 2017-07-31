---
title: android 安全
---

# Android 基础

## 基础知识

## Apk 打包流程

## Apk 文件结构

# android程序运行机制概述

分别介绍java层与native层。以及两者之间的关系。

## 概述

说明Android首先执行Application类（需要在AndroidManifest.xml文件中注明）的创建工作，然后在开始执行主Activity，继而根据各种各样的逻辑进行执行。

## java 虚拟机

### 历史发展

说明dalvik虚拟机最初其实不是JIT。什么时候引入，为什么引入，之后又在什么时候引入ART。为什么引入。

#### dalvik虚拟机

- 基本特点
- 如何运行
  - loadClassFromDex完成类的装载工作
  - 装载程序类
  - 验证字节码
  - 查找主活动
  - 初始化解释器
  - 执行字节流
    - 按方法
    - 按trace，即执行轨迹
  - 说明其实是C语言。
- JIT运行方式
  - method方式
  - trace方式，默认采用该方式。

#### art

### 区别

- 与java虚拟机区别

## 原生运行



# Android Java层相关介绍

java层-->insns

native层。 

## Smali语法

### 声明语句

其实大多数都并不存在于dex文件中。

#### 寄存器

#### 变量类型

#### 方法

#### 类

### 执行语句

#### Dalvik指令格式

#### 指令特点

#### 具体指令

## Android 可执行文件

### dex文件

### odex文件

# Android Native层相关介绍

## 基本操作原理

## so文件

so加载方法，加载过程。

## arm汇编

# Android逆向基本介绍

## 概述

有什么应用场景？

## 基本思路

为什么要按照下面的方法去做？？

方法与对象，**用什么方法对什么对象进行分析**？

## 逆向工具介绍

### 反编译工具

### 静态分析工具

### 动态分析工具

### hook框架

### 沙盒环境

## 静态分析

### 技巧

- 字符串定位--定位关键函数
  - 程序报错信息
  - 服务
  - 广播
- 特征函数定位
  - 控件的事件函数---onclick，show
  - 网络函数---HttpGet、HttpPost、HttpUriRequest、socket
  - 发送短信
  - 打电话
  - 定位
  - 等等

## 动态分析

为什么要动态分析呢？

- 静态分析解决不了的问题，需要动态分析加以辅助。
- 动态分析可以方便我们获取程序几乎每一条指令运行后的状态，方便我们理解其中的逻辑。在理解逻辑的同时，可以​
  - dump出我们想要的文件

动态分析方法，分别介绍。

### android层动态分析

smali

### native层动态分析



### 反调试

### 反反调试



## java层逆向

## native层逆向

Elf 可执行文件和共享目标文件都有的一个节是 .init_array(类似于PE文件格式的TLS)，它先于JNI_OnLoad或者main函数执行，主要用于给编译器生成初始化C或者C++运行时库，为后续代码准备运行时环境。.init_array 节中包含指针，这些指针指向了一些初始化代码，在分析linker 源码中，可以知道节的执行顺序一般为.preinit_array-> .init -> .init_array，在共享目标文件so中.preinit_array中函数是不会执行的，这里我们只说.init_array,很多APK加固方案都在这里有文章。	

- 如果函数是静态注册的话，一般来说，在ida的函数列表中就会有类似于“包名_函数名”的函数。
- 如果函数是动态注册的话，一般是在JNI_Onload函数进行注册使其与java层的函数相关联。此时，我们需要导入

# Android 协议分析

# Android hook与注入

# Android 加固

# Android 壳

## 壳

## 原理

attachBaseContext

onCreate

## 加壳

## 检测壳

## 脱壳



# Android 系统安全

# Android 取证分析



