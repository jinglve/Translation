# Pixhawk Hardware

Pixhawk 是 PX4 飞行堆栈的标准微控制器平台。它在 NuttX 系统上运行 PX4 中间件。  a CC-BY-SA 3.0 许可开放硬件设计，所有图纸和设计文件都是可用的。 Pixfalcon 是 Pixhawk 的FPV 和类似平台较小版本。对于性能要求较高的或相机的无人机接口，高通晓龙行可能会更加合适。


## 快速摘要

-   主片上系统: STM32F437
    - CPU: 180 MHz，ARM Cortex M4内核，单精度FPU
    - RAM: 256 KB SRAM
-   失效保护片上系统: STM32F100
    - CPU: 24 MHz ARM Cortex M3内核
    - RAM: 8 KB SRAM
-   Wifi: ESP8266 外部
    - GPS: U-Blox 7/8 (Hobbyking) / U-Blox 6 (3D Robotics)
    -光流: PX4 光流单元
      - Hobbyking EU 版本 (433 MHz)]
-   Hobbyking US 版本 (915 MHz)
    - 3D Robotics 储藏 (GPS 和数传不捆绑)
-   配件:
    - 数字空速管
    - Hobbyking Wifi 数传
    - Hobbyking OSD + US数传 (915 MHz)
    - Hobbyking OSD + EU 数传 (433 MHz)

## 接口

- 一个I2C
- 一个 CAN (两个可选)
  - 1一个ADC
  - 四个 UART (二个光流控制)
  - 一个控制
  - 八路 PWM用来做手动控制
  - 6六路PWM / GPIO / PWM 输入
  - S.BUS / PPM / Spektrum 输入
  - S.BUS 输出

## 引出和原理图

简体中文  英语 丹麦语
板信息详细的记录在Pixhawk 项目网站上。
