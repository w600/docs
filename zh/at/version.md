# AT固件版本说明

![img](../.assets/at/version/version.png)

W600 系列wifi产品目前拥有两个版本的AT固件；

**兼容版AT固件** 和 **WM_AT固件** 是基于两个不同版本的SDK开发出来的，兼容版AT固件指的是兼容ESP系列AT指令的固件，WM_AT固件是由联盛德官方SDK编译而来。

如用户不确定手里的产品是哪一个版本的AT固件，可以通过一条指令做判断。

| 固件版本 | PC 发送 |  W600 回复  |
| :------: | :-----: | :---------: |
| 兼容版AT |   AT    |     OK      |
| 兼容版AT |   AT+   |    ERROR    |
|  WM_AT   |   AT    | -（无应答） |
|  WM_AT   |   AT+   |     OK      |

**兼容版AT固件**

兼容版AT固件兼容乐鑫ESP8266 AT 指令集；

该固件不开源，可参考 [兼容版AT指令开发入门指导](https://docs.w600.fun/?p=at/esp-start.md) ；

**WM_AT固件**

该固件可通过修改联盛德官方SDK的宏定义，编译后获取 （宏定义默认打开）；

首先，参考 [W600开发环境搭建](https://docs.w600.fun/?p=app/ide.md) 准备好开发环境，默认即AT固件，发送`AT+`回复`OK`；
