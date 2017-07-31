# Android 逆向基本介绍

目前来说，Android逆向主要应用于以下几个方向

1. app安全审查
2. 系统漏洞挖掘
3. 恶意代码杀查
4. 同行业竞品技术原理分析
5. 移除安全机制

# 基本思路

首先，我们需要明确一下Android逆向中的目的： **我们是希望分析出某一部分的程序的功能** 。那么我们自然也就有两个方面（方法与对象）可以考虑

- 分析方法，可以采用以下方式
  - 静态分析，对源代码进行逆向，然后阅读分析
  - 动态分析，对代码进行动态调试
  - 静态分析与动态分析结合，一般来说也都是以采用这种方法
- 分析对象，一般有以下两类对象
  - java层代码
  - 原生层代码

不难看出，其实我们要想分析Android程序，一些基本的java层的知识与原生层的知识还是有必要需要掌握的。

# 逆向工具介绍

## 反编译工具

其中反编译工具主要分为以下几类功能，**可以考虑画个图**

- 将dalvik字节码转换为smali代码
- 将dalvik字节码转化为jar包
- 将jar包转换为java代码

目前有以下几种工具

- Apktool/Shakaapktool，推荐后者，功能增强。
- smali/baksmali
- dex2jar
- enjarify
- Android逆向助手

## 静态分析工具

- jadx，分析java
- JEB
- Android Killer，分析smali等资源文件
- IDA PRO，分析so代码

## 动态分析工具

- JEB
- jdb
- Android Studio/Intellij IDEA
- gdb
- IDA Pro

## hook框架

- Cydia Substrate
- Xposed
- adbi
- Frida

## 沙盒环境

- DroidBox

参考

- 非虫 2016安全训练营