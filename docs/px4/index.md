# PX4硬件方案

<a id = "px4"></a>

## 简介

基于px4做的几款飞控硬件方案

## 硬件方案 

| 命名 | 方案 |
|:-----:|:-----:|
| GLPX4-F4 | 基于STM32F427VIT6 |
| GLPX4-H7 | 基于STM32H743VIH6 |
| GLPX4-R329 | 基于全志R329 |
| GLPX4-ESP32 | 基于ESP32 |

### GLPX4-F4 
* 主控: STM32F427VIT6
* IMU： MPU9250 ICM-20602
* 磁力计：LIS3MDL
* 气压计：MS5611
* 光流：PMW3901MB
* 激光：VL53L1X

### GLPX4-H7
* 主控：STM32H743VIH6
* IMU：MPU9250 ICM-20602
* 磁力计：LIS3MDL
* 气压计：MS5611

### GLPX4-R329
* 主控：全志R329
* IMU: ICM-20689 ICM-20602
* 磁力计：IST8310
* 气压计：MS5611
* PWM: PCA9685PW

### GLPX4-ESP32
* 主控： ESP32-D2WD
* IMU： MPU9250
* 光流：PMW3901MB
* 激光：VL53L1X

## 图片及演示视频

### GLPX4-R329
<iframe height="480" width="100%" src="//player.bilibili.com/player.html?aid=847546378&bvid=BV1UL4y1a76o&cid=394305751&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>  
<br />  

![px4](img/px4_2.jpg)  
<br />  

![px4](img/px4_4.jpg)  
<br />  

![px4](img/px4_5.jpg)  
<br />  

![px4](img/px4_6.jpg)  
<br />  

### GLPX4-F4
<iframe height="480" width="100%" src="//player.bilibili.com/player.html?aid=420006883&bvid=BV1d3411q7Dd&cid=394311072&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>  
<br />  

![px4](img/px4_0.jpg)  
<br />  

### GLPX4-H7
![px4](img/px4_1.jpg)  
<br />  

### GLPX4-ESP32
<iframe height="480" width="100%" src="//player.bilibili.com/player.html?aid=420001535&bvid=BV1N3411B7ig&cid=394308441&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>  
<br />  

![px4](img/px4_3.jpg)  
<br />  

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


## PX4 飞控稳定调试
* 首先在自稳模式下将PID参数调稳定，调试`Multicopter Rate Control`菜单下`MC_ROLLRATE_P`, `MC_ROLLRATE_I`, `MC_ROLLRATE_D`,`MC_PITCHRATE_P`,`MC_PITCHRATE_I`,`MC_PITCHRATE_D`这六个参数即可  
<br />  

* 自稳PID调试完成后，此时飞行会发现飞行器总是会朝某个方向“倾斜”飞行，此时最好先将机体各部位都固定稳定，中心最好在机体中心（电池位置最好也固定，不然电池的拆卸也是影响重心的一个要点）。然后调试`Sensors`菜单下的`SENS_BOARD_X_OFF`和`SENS_BOARD_Y_OFF`两个参数，最完美的状态是调试到roll和pitch不总是朝一个方向飞行，只会随机朝某个方向缓慢飞行  
<br />  

* 随后切换到offboard模式进行定位调试，如果设置指定高度后飞行器一直飞行不到指定高度，请增大`Multicopter Position Control`菜单下的`MPC_THR_HOVER`和`MPC_Z_P`参数  
<br />  

* 随后调试定位的参数，`Multicopter Position Control`菜单下的`MPC_XY_P`,`MPC_XY_TRAJ_P`,`MPC_XY_VEL_D_ACC`,`MPC_XY_VEL_I_ACC`,`MPC_XY_VEL_P_ACC`这几个参数，注意增大其中`MPC_XY_VEL_I_ACC`参数对减小偏移有显著效果
