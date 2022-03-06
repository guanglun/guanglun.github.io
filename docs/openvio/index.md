# OPENVIO使用说明

<a id = "openvio"></a>

## 简介

OPENVIO 一款脱胎于OPENMV的智能摄像头。

在OPENMV硬件基础上增加了USB2.0芯片(USB3315）和IMU芯片（MPU6050），除却兼容OPENMV固件外，还可以将摄像头原始图像（未压缩图像）和IMU九轴数据高速传输至PC，可以作为SLAM单目IMU方案研究的低廉传感器方案（如港科大的VINS-MONO）.多种接口方便扩展更多功能，比如扩展超声波或激光模块后作为PX4光流模块使用（暂未实现 还在研发中）。

## 源码和资料

[新架构OPENVIO-APP源码(github)](https://github.com/guanglun/openvio)【开发环境：Vscode Makefile】  

[新架构OPENVIO-BOOTLOADER源码(github)](https://github.com/guanglun/openvio_bootloader)【开发环境：Vscode Makefile】 

[新架构OPENVIO-APP源码(gitee)](https://gitee.com/guanglunking/openvio)【开发环境：Vscode Makefile】  

[新架构OPENVIO-BOOTLOADER源码(gitee)](https://gitee.com/guanglunking/openvio_bootloader)【开发环境：Vscode Makefile】  

[OPENVIO源码](https://gitee.com/guanglunking/OPENVIO_BOARD)【开发环境：Keil5】  

[OPENVIO PC上位机](https://gitee.com/guanglunking/OPENVIO_PC)【开发环境：QT5.6.0 qt-opensource-windows-x86-mingw492-5.6.0】  

[OPENVIO ROS源码](https://gitee.com/guanglunking/OPENVIO_ROS)

[淘宝店铺](https://item.taobao.com/item.htm?id=615919130291)  

## 与OPENMV固件兼容性说明
可以直接刷入OPENMV H7的官方固件使用，也就是说，摄像头的功能皆兼容。但是由于扩展接口不同，所以不对官方固件做兼容。  

| 三色LED | OV7725 | MT9V034 | 其他模块 |
|:-----:|:-----:|:-----:|:-----:|
| 仅兼容一颗 | 兼容 | 兼容 | 不兼容 |  

</br>

## 功能及研发进度
| 功能 | 进度 |
|:-----:|:-----:|
| OPENMV两款摄像头兼容 | 已完成 |
| SLAM VIO 单目IMU传感器功能 | 已完成 |
| 港科大VINS-MONO | 已完成 |
| PC上位机 | 正在研发 |
| 小Demo | 正在研发 |
| PX4光流 | 正在研发 |

</br>

## 已有模块及正在研发模块

| 模块 | 进度 |
|:-----:|:-----:|
| OV7725 | 已完成 |
| MT9V034 | 已完成 |
| 下载调试器模块 | 已完成 |
| 正面彩屏模块 | 正在研发 |
| 背面彩屏及锂电源模块 | 正在研发 |
| 超声波模块 | 正在研发 |


## 图片

### V1.0版本

![OPENVIO](img/v1.0-1.jpg)

![OPENVIO](img/v1.0-2.jpg)

### V1.2版本

![OPENVIO](img/v1.2-1.jpg)

### V1.3版本

![OPENVIO](img/v1.3-1.jpg)

![OPENVIO](img/v1.3-2.jpg)

![OPENVIO](img/v1.3-3.jpg)

### V1.4版本

![OPENVIO](img/v1.4-1.jpg)

![OPENVIO](img/v1.4-2.jpg)

### V1.5版本

![OPENVIO](img/v1.5-1.jpg)

![OPENVIO](img/v1.5-2.jpg)

![OPENVIO](img/OPENVIO.jpg)

![OPENVIO](img/OPENVIO1.jpg)

![OPENVIO](img/OPENVIO2.jpg)

![OPENVIO](img/OPENVIO3.jpg)

### V1.6版本

![OPENVIO](img/v1.6-0.jpg)

![OPENVIO](img/v1.6-1.jpg)

![OPENVIO](img/v1.6-2.jpg)

### PC上位机

![OPENVIO](img/OPENVIO_PC.png)

### VINS-Mono

![OPENVIO](img/Screenshot from 2020-08-04 12-59-07.png)

