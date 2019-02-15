# Zlib

## 1、介绍

Zlib 是一款免费的、通用的、合法的、不受任何限制的无损数据压缩库。这个 [zlib](https://github.com/RT-Thread-packages/zlib) 库是RT-thread针对官方 [zlib](https://github.com/madler/zlib) 的C库的移植， 有关 zlib 的更多信息，请参阅[官方说明](http://www.zlib.net/) 。

## 2、获取方式

-  Git方式获取：
  `git clone https://github.com/RT-Thread-packages/zlib.git`

-  env工具辅助下载：
  menuconfig package path：`RT-Thread online package` -> `miscellaneous package` -> `Zlib`

## 3、示例介绍

### 3.1 获取示例

### 3.2 运行示例

## 4、注意事项

### 4.1 与官方源码差异

本次移植基于 zlib 的 1.2.3 版本，该版本的[下载地址](https://github.com/madler/zlib/archive/v1.2.3.zip)请点击链接。

移植过程中对源代码进行了一定的修改，如下所示：

1. 对源码 `crc32.c` 文件的修改

在第 22 行添加如下代码：

```c
#define DYNAMIC_CRC_TABLE
```
2. 对源码 `zutil.c` 文件的修改

在 294 行到 316 行添加开启 `RT_USING_RTGUI` 宏时执行不同的内存分配和释放操作。

## 5、参考资料

- Zlib 官方网站：https://zlib.net/


