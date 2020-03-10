# Clover-EFI
Share Some Clover Configuration Files（分享一些黑苹果配置文件，主板ASUS Z370A）

![基本介绍.png](基本介绍.png)<br>
CPU： Intel QQM6 （Engineering Sample）<br>
主板: ASUS PRIME Z370-A (https://www.asus.com.cn/Motherboards/PRIME-Z370-A/)<br>
声卡: Realtek S1220A)<br>
有线网卡: Intel i219V2 <br>
显卡: 5700xt & 580(8g 2304sp，目前主显示器插在5700xt上)<br>

/------------------------------/
2020-03-10更新
经过我的测试，可以在AppStore里面直接从10.15.2更新到10.15.3。
也可以直接用10.15.3的镜像，然后覆盖EFI文件夹即可。
/------------------------------/

Bug： 
1.睡眠似乎有问题，会睡死，因此我的解决办法是直接关闭睡眠<br>
2.我的键盘是是用罗技G710+,是用调节音量滚轮时，音量大小变化极端灵敏，而且系统音量大小的动画会卡顿，尚不知道什么问题。<br>

更新1： <br>
蓝牙测试<br>
Xdobo x3 Pro只支持SBC （音箱只支持SBC）<br>
威泽W2-AM1 支持aptx <br>
使用蓝牙连接音箱和耳机后，发现罗技键盘调节音量滚轮，音量大小变化极端灵敏的bug消失了，不清楚是什么原因。

总结：
基于myd2898129的EFI修改，感谢myd2898129的前期工作，给我省去了大量的时间（源地址：http://bbs.pcbeta.com/viewthread-1829467-1-1.html)<br>
最开始是用myd2898129的EFI时出现 8 table load failures报错无法正常进入安装页面，经过查找后，发现需要做两个步骤：<br>
1.更新whatevergreen.kext到最新版本,我使用的版本为1.3.6<br>
2.在config.plist中的Boot-Arguments下添加agpdmod=pikera参数（没有Boot-Arguments参数可以自己添加，但是要注意上下文格式）<br>
（源地址：https://osx.cx/whatevergreen-kext-amd.html）<br>
(我已经做了这方面的处理，和我相同主板型号的直接使用即可，安装时尚未遇到其他的问题）<br>
3.主板上的USB 3.1 Gen2 未测试功能是否正常

![变频.png](变频.png)
![基本介绍.png](基本介绍.png)
![GPU.png](GPU.png)
![Audio.png](Audio.png)
![Display.png](Display.png)
