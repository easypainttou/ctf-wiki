# android 环境搭建

## 运行环境

## 调试环境

# android调试

设置远程调试选项

Run->debug configurations -> Remote Java Applications ,Host为localhots，端口设置8700。

使用adb以debug的方式启动apk

adb shell am start -D -n packageName/ActivityName

 adb connect 127.0.0.1:21503

# jeb使用 

# 关键代码定位

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

