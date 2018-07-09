----
**Smart-Lamp**
====
----
# **Content**
* [Introduction](#introduction)
  * [Function](#function)
  * [System Architecture](#architecture)
* [System Config](#config)
  * [Hardware](#hardware)
  * [Software](#software)
  * [Hardware Connection](#connection)
* [User Manual](#usermanual)
* [Video](#video)
----
# **Introduction** <div id='introduction'/>
This project designed a smart lamp which was based on ARC EM Starter Kit. The lamp can detect whether the user is using to turn on or off, automatically connect the server to report the real-time status, and manually and automatically adjust the brightness, remotely be controled by the APP console, record the user's usage time. The follow-up will add the functions of detecting the unhealthy work schedule of the user and correcting the user's incorrect sitting habits, which can help the user to effectively get rid of the health hazards brought by the high pressure of modern life, develop a good working habit,  and keep your body and eyes healthy.
本项目设计了一种基于ARC EM Starter Kit开发板的智能台灯，能够检测用户是否在使用而开关台灯，自动连接服务器报告台灯的实时状态，可以手动和自动调节台灯的亮度，通过APP远程控制台灯，记录用户的使用时间。后续会加入检测用户不健康工作作息规律、矫正用户不正确坐姿习惯的功能，帮助用户有效避免现代生活高压下带来的健康隐患，在有一个舒适的工作环境的同时，养成一种良好的工作作息习惯，保持身体与眼部的健康。<br>
## **Function** <div id='function'/>
* **自动开关台灯**<br>
When the human body is located at a distance of about 15cm from the infrared transceiver port and keeps the occlusion time for more than 3 seconds, the lamp can normally illuminate and enter the auto dimming mode by default. Similarly, the lamp will automatically turn off 3 seconds after the person leaves the lamp, avoiding the occasional behavioral instability of the user and causing the desk lamp to be frequently turned off.
在人体位于红外收发口15cm左右距离，并保持3秒以上的遮挡时间时，台灯能正常亮起并默认进入自动调光模式。同样的，在人离开灯附近3秒后，台灯才会自动关闭，避免用户偶尔的行为不稳定导致台灯频繁亮灭。
* **自动连接服务器上线**<br>
After restarting the lamp and the network, the lamp can automatically re-launch within 5 seconds.
在重启无线网络、重启后台服务器后，台灯均能在5s内重新自动上线。
* **自动调节台灯亮度**<br>
The lamp can realize stepless natural dimming in 8 different light intensity ranges, and there is no phenomenon that the user feels uncomfortable due to the light intensity jump and stroboscopic. In the automatic dimming mode, the lamp can adapt to the change of light intensity in the environment, and adjust the brightness in time, with better sensitivity.
台灯能在8档不同光照强度范围内实现无级自然调光，没有光强跳变、频闪等令用户感到不舒服的现象发生。自动调光模式下，台灯能自适应环境中的光强变化，及时进行亮度调节，灵敏度较好。
* **远程APP控制**<br>
The APP can support the frequent operation of the user, and there is no problem of wrong operation or invalid operation under the high-intensity round-trip conversion test.
APP控制能够支持用户的频繁操作，在高强度的来回调档测试下也不会出现错误操作、无效操作等问题。
## **System Architecture** <div id='architecture'/>
<img src="https://github.com/tyhucosiii/smart-lamp/blob/master/pictures/system.jpg" width = "500" alt="图片名称" align=center /> <br>

----
# **System Config** <div id='config'/>
## **Hardware** <div id='hardware'/>
* EMSK V2.2 ARCEM7D Starter Kit
* ESP8266 WIFI
* Infrared Ray Sensor
* Touchpad
* CM3232 Ambient Light Sensor <br>
<img src="https://github.com/tyhucosiii/smart-lamp/blob/master/pictures/esp8266.jpg" height = "150" alt="图片名称" align=center /><img src="https://github.com/tyhucosiii/smart-lamp/blob/master/pictures/ir.jpg" height = "150" alt="图片名称" align=center /><img src="https://github.com/tyhucosiii/smart-lamp/blob/master/pictures/touchpad.jpg" height = "150" alt="图片名称" align=center /><img src="https://github.com/tyhucosiii/smart-lamp/blob/master/pictures/cm3232.jpg" height = "150" alt="图片名称" align=center />

## **Software** <div id='software'/>
* ARC GNU Toolchain
* embARC Open Software Platform (OSP) 201709
* Serial Port Terminal eg. XCOM
* APP for Android
* Mini Program of Wechat 
## **Hardware Connection** <div id='connection'/>
<img src="https://github.com/tyhucosiii/smart-lamp/blob/master/pictures/all.jpg" height = "500" alt="图片名称" align=center /><br>
* ESP8266 connected to UART1 through PMOD1 of ARC EMSK模块通过开发板的Pmod1接口与UART1连接
* CM3232 connected to I2C through PMOD3 of ARC EMSK感光模块通过开发板的Pmod3接口与I²C接口连接
* Touchpad connected to UART emulator through PMOD3 of ARC EMSK触控板模块通过开发板的Pmod3接口与模拟UART连接
* Infrared Ray Sensor connected to GPIO through PMOD2 of ARC EMSK红外模块通过开发板的Pmod2接口与GPIO连接

----
# **User Manual** <div id='usermanual'/>
* The user configures the current network for the lamp through the APP and connects to the server.
用户通过移动客户端为台灯配置当前网络，连入服务器
* In the automatic control mode, the lamp can enter the automatic dimming while the user is nearby, which will automatically adjust the brightness according to the ambient light intensity.
自动控制模式下，用户靠近台灯就能进入自动调光，台灯会根据环境光强自动进行亮度调节
* In manual control mode, the user can manually adjust the brightness of the lamp through the touchpad button and exit the automatic mode.
手动控制模式下，用户可通过触控板按键手动调节台灯亮度，并退出自动模式
* The user can remotely control via mobile client可通过移动客户端进行远程控制

----
# **[Video]<div id='video'/>(https://v.youku.com/v_show/id_XMzcxMzE0NzA0NA==.html?spm=a2h3j.8428770.3416059.1)**
----
