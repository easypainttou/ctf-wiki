# Android 分析小策略

# 关键代码定位

在Android

AndroidManifest.xml文件

- 软件包名
- apk主活动，隐藏程序没有主Activity

Application在 java层启动最早，

## 字符串定位法

通过在程序程序运行过程中出现的字符串来定位相应的函数。字符串有可能被直接硬编码在程序中，也有可能通过字符串id来索引。

这一方法过去一般情况下还可以，但是现在的话，有可能字符串会被分开或者说首先被加密，在运行的过程中被动态解密。

我们可能关注的字符串可能有

- 程序报错信息
- 服务
- 广播

## 敏感API

- 字符串定位--定位关键函数
  - ​
- 特征函数定位
  - 控件的事件函数---onclick，show
  - 网络函数---HttpGet、HttpPost、HttpUriRequest、socket
  - 发送短信
  - 打电话
  - 定位
  - 等等



- 需要了解android中操作对应的API
- ZJDROID

## 钩子

- xposed
- cydia

## monitor

- 运行log，程序 运行产生的，系统运行产生的
- 线程跟踪
- 方法调用链

## 手动log信息

## 动态调试