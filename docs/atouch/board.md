# 吃鸡开发板 硬件说明

<a id = "board"></a>

## 说明

* 串口指令（波特率115200 不加回车换行符）


| 命令 | 效果 | 说明 |
|:-----:|:-----:|:-----:|
| open | 打开串口传输模式 | 将会只传输状态和键鼠信息（关闭log） |
| close | 关闭串口传输模式 | 停止传输状态和键鼠信息 |
| slogn | 设置LOG级别 NONE | 停止输出任何LOG |
| sloge | 设置LOG级别 ERROR | 只输出 ERROR LOG |
| slogw | 设置LOG级别 WARN | 输出 WARN 及以上 LOG |
| slogi | 设置LOG级别 INFO | 输出 INFO 及以上 LOG |
| slogd | 设置LOG级别 DEBUG | 输出 DEBUG 及以上 LOG |
| slogv | 设置LOG级别 VERBOSE |  输出所有LOG |

* 上电默认LOG模式：INFO （slogi）  

<br/>