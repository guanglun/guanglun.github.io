# PX4硬件方案

<a id = "px4"></a>

## 简介

基于px4做的几款飞控硬件方案

## 硬件方案 

* 基于STM32F427VIT6
* 基于STM32H743VIH6
* 基于全志R329
* 基于ESP32

### GLPX4_R329开机自启动
脚本auto_run.sh
```
nohup taskset -c 1 /root/px4/build/px4_raspberrypi_default/bin/px4 -s /root/px4/px4.config -d &> 1 > /root/px4/px4.log
```
添加至/etc/rc.local

### armbian添加isolcpus
vim /boot/armbianEnv.txt
添加：
```
extraargs=isolcpus=1
```

## 图片及演示视频

![px4](img/px4_0.jpg)  
<br />  

![px4](img/px4_1.jpg)  
<br />  

![px4](img/px4_2.jpg)  
<br />  

![px4](img/px4_3.jpg)  
<br />  
