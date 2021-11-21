# 开源四旋翼飞行器GLDrone

<a id = "gldrone"></a>

## 简介

GLDrone是独立自制机架和电调飞控的开源项目，轴距在140左右的小机型，为室内飞行与室内编队实验而研发。

## 设计文件

[机架设计文件(使用Fusion360)](https://github.com/guanglun/GLDrone)  
[电调原理图PCB(立创EDA)](https://oshwhub.com/guanglun/gldrone_blheli_esc)  
[飞控原理图PCB(立创EDA)](https://oshwhub.com/guanglun/gldrone_px4)  
[修改后的PX4源码(见)](https://github.com/guanglun/PX4-Autopilot)  
机架设计文件Fusion360分享地址：[https://a360.co/30LNv4s](https://a360.co/30LNv4s)  

## 说明
* 电调设计参考[https://github.com/ckflight/ESC_BLDC_HARDWARE](https://github.com/ckflight/ESC_BLDC_HARDWARE)  
* 飞控为PX4 FMUv4 
* 由于电调飞控V1.1版本修改了V1.0版本发现的问题后未经打样测试，所以请谨慎使用！

## 存在的问题
* 警告！电调PCB由于四合一电调采用了模块复制，所以丝印只有MOTO4的正确，其他MOTO请参考MOTO4放置元器件！其中未连接的网络是由于复制过程中没有改网络编号所致，无需连接。
* 电调供给飞控的5V电源由于经过了在飞控PCB中经过了一个二极管导致压降至4.5V左右，应提高电调输出的电压。

## 图片及演示视频

![gldrone](img/gldrone1.jpg)   
<br />  
![gldrone](img/gldrone2.jpg)   
<br />  
![gldrone](img/gldrone3.jpg)   
<br />  
![gldrone](img/gldrone4.jpg)   
<br />  
![gldrone](img/gldrone5.jpg)   
<br />  
<iframe height="480" width="100%" src="//player.bilibili.com/player.html?aid=719184650&bvid=BV1cQ4y1U7HJ&cid=442156475&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>  
<br />  
<iframe height="480" width="100%" src="//player.bilibili.com/player.html?aid=891320934&bvid=BV1EP4y1L723&cid=432987595&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>  
<br />  
<iframe height="480" width="100%" src="//player.bilibili.com/player.html?aid=378817502&bvid=BV1vf4y1M7S2&cid=430310862&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>  