# Bluetooth-remote-control-handling-car
STM32H750VBT6开发板，四个麦克纳姆轮，四个舵机；12个PWM通道、usart串口通信+蓝牙模块+DMA数据传输


小车的蓝牙模块和手机相连，通过DMA控制串口通信，接受手机APP返回的11位数据，
接受数据以及对应的功能映射如下:

手机APP	返回数据	功能映射
左摇杆的Y	r->rocker[0].y_position	麦轮的X
左摇杆的X	r->rocker[0].x_position	麦轮的Y
右摇杆的X	r->rocker[1].x_position	麦轮的Z
BUTTON1	r->Button[0]	舵机1角度加
BUTTON2	r->Button[1]	舵机1角度减
BUTTON3	r->Button[2]	舵机2角度加
BUTTON4	r->Button[3]	舵机2角度减
Switch1	r->Switch[0]	舵机3角度加
Switch2	r->Switch[1]	舵机3角度减
Switch3	r->Switch[2]	(=1)舵机4角度加,(=0)舵机4角度减
Switch4	r->Switch[3]	(=0)麦轮低转速，（=1）麦轮高转速

 
根据传回的数据完成以下功能：
1、	麦克纳姆轮正反转+PWM控制：
2、PWM控制舵机：
3、DMA串口通信：
