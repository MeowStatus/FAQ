# FAQ

## Q9：关于路由器不选Bridge（AP）桥接模式就不能正常联网

A9：存在一种可能，自用路由器并非直连光猫，而是通过一级路由器间接与光猫相连。自用路由器的局域网ip和一级路由器的局域网ip相同，导致了网络冲突。只需把自用路由器的局域网ip（华为路由器是192.168.3.1）更改网段即可。

## Q8：TF卡类型

A8：

| 容量分类 |     容量      | 支持的文件格式 |         兼容性         |
| :------: | :-----------: | :------------: | :--------------------: |
|   SDSC   |    1MB~2GB    |                |                        |
|   SDHC   |  (2GB，32GB]  |     FAT32      |                        |
|   SDXC   |  (32GB，2TB]  |     exFAT      | 不兼容SD和SDHC对应设备 |
|   SDUC   | （2TB，128TB] |                |                        |

## Q7：如何绕过文件查重检测（例如绕过JLC的拆单检测）

A7：可以更改文件的MD5值。如何更改自行百度。

## Q6：如何把方形图片变成圆形

A6：利用PPT。

1.插入->形状->椭圆；

2.按住shift，拖动鼠标左键画出正圆；

3.选中此圆形，单击工具栏中的“绘图->填充”；

4.下拉菜单中选择“本地图片”；

5.选择要插入的图片并填充；

6.将图片另存为文件。

## Q5：下载的字体文件如何安装

A5：选中字体包中的所有后缀为.ttf的文件，右键单击，选择“安装”即可。

## Q4：程序下载失败可能的玄学因素

A4：数据线必须伸展开，尽量减少弯折，更不能用轧带扎起来。

## Q3：隔离数字地和模拟地的方法

A3:

1、磁珠的等效电路相当于带阻滤波器，只对某频点的噪声有显著抑制作用，使用时需要预先估计噪点频率，以便选择适当型号。对于频率不确定或无法预知的情况，磁珠不适合使用。

2、电容的“隔直通交”作用会造成浮地。

3、电感体积大，杂散参数多，不稳定。

4、0Ω电阻相当于很窄的电流通道，能够有效的限制环路电流，使噪声得到抑制。电阻在所有频带上都有衰减作用（0Ω电阻也有阻抗），所以适合用以分割模拟地和电源地。

一、什么是电路中的“地”

“地”是电子技术中一个很重要的概念。“地”的经典定义是“作为电路或系统基准的等电位点或平面”。

“地”的分类与作用有很多种。在本问题中我们就不一一说明了。简单了解一下模拟地和数字地的作用。

模拟地：放大器、采样保持器、A/D转换器和比较器的零电位参考点。

数字地：也叫逻辑地，是数字电路的零点位参考点。



二、电路中的数字地和模拟地

电路中的数字地是数字电路零电位的公共基准地。

模拟地是模拟电路零电位的公共基准地。

二者都是作为零电位的公共基准地，但是数字电路工作在脉冲状态，且变化的速度比较快，因而数字地上的噪声比较大；模拟电路的模拟信号既容易受外界干扰，又容易产生干扰，所以对地的要求比较严格。

如果将数字地和模拟地混合使用，则模拟信号受数字信号的影响比较大。



三、0Ω电阻为什么可以分割数字地与模拟地

电路中，只要是地，最终都要接到一起，然后流入大地。

如果不接在一起就是“浮地”，存在压差，容易积累电荷，造成静电。

地是参考零电位，所有电压都是参考地得出的，地的标准要一致，所以各种地应短接在一起，人们认为大地能够吸收所有电荷，始终维持稳定，是最终的地参考点。

虽然有些板子没有接大地，但发电厂是接大地的，板子上的电源最终还是会返回发电厂入地。

如果把模拟地和数字地直接相连，会导致互相干扰。

不短接又不妥，由四种方法解决此问题：用磁珠连接；用电容连接；用电感连接；用0Ω电阻短接。


## Q2：USB速率分类
A2：
|USB版本|理论最大传输速率|速率称号|最大输出电流|推出时间|
|:----------:|:-------------:|:------:|:-------------:|:-------------:|
| USB 1.0 |1.5Mbps(192KB/s)|Low/Half-Speed|5V/500mA|1996/01|
| USB 1.1 |12Mbps(1.5MB/s)|Full-Speed|5V/500mA|1998/09|
| USB 2.0 |480Mbps(60MB/s)|High-Speed|5V/500mA|2000/04|
| USB 3.0|5Gbps(500MB/s)|Super-Speed|5V/900mA|2008/11 |
|USB 3.1 Gen 1|5Gbps(500MB/s)|Super-Speed|5V/900mA|2013/12|
| USB 3.1 Gen 2 |10Gbps(1280MB/s)|Super-speed+|20V/5A|2013/12|
## Q1：CP2102系列芯片插入电脑遇到 “Verifone USB to Modem” 问题。
A1：原因可能是芯片为翻新货，内部数据被修改，无法被正常驱动。解决方法为安装原厂驱动程序，具体操作如下图。
![1](https://raw.githubusercontent.com/MeowStatus/IMG/main/Images/202303181322217.jpg)
![2](https://raw.githubusercontent.com/MeowStatus/IMG/main/Images/202303181323892.png)

修复完成结果如图。
![3](https://raw.githubusercontent.com/MeowStatus/IMG/main/Images/202303181323350.jpg)