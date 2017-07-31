# Android 分析小策略

# 关键代码定位

在Android

AndroidManifest.xml文件

- 软件包名
- apk主活动，隐藏程序没有主Activity

Application在 java层启动最早，

## 字符串定位法

- 程序运行过程中出现的字符串，过去常用，
- 现在字符串
  - 会被拆分开，比较low
  - 可能会被加密，运行过程中动态解密

## 敏感API

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