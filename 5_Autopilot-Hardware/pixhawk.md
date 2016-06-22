# pixhawk硬件


pixhawk是PX4飞控层的标准控制平台，它在Nuttx的操作系统上运行PX4的中间层。由于CC-BY-SA 3.0许可开放硬件设计，所有原理图和设计文件都是可提供的。对FPV racers和类似的平台来说pixfaclon是pixhawk的一个小版本。高通晓龙对于较高加工性能或者照相平台来说会有一个更合适的优选。

![pixhawk](../pictures/hardware/hardware-pixhawk.png)

## Quick Summary

-   Main System-on-Chip: [STM32F437](http://www.st.com/web/en/catalog/mmc/FM141/SC1169/SS1577/LN1789)
    - CPU: 180 MHz ARM Cortex M4 with single-precision FPU
    - RAM: 256 KB SRAM (L1)
-   Failsafe System-on-Chip: STM32F100
    - CPU: 24 MHz ARM Cortex M3
    - RAM: 8 KB SRAM
-   Wifi: ESP8266 external
    - GPS: U-Blox 7/8 (Hobbyking) / U-Blox 6 (3D Robotics)
    - Optical flow: [PX4 Flow unit](http://www.hobbyking.com/hobbyking/store/__66308__HK_Pilot32_Optical_Flow_Kit_With_Sonar.html)
    - Availability:
      - [Hobbyking EU version (433 MHz)](http://www.hobbyking.com/hobbyking/store/__80554__HKPilot32_Autonomous_Vehicle_32Bit_Control_Set_with_Telemetry_and_GPS_433Mhz_.html)
-   [Hobbyking US version (915 MHz)](http://www.hobbyking.com/hobbyking/store/__80555__HKPilot32_Autonomous_Vehicle_32Bit_Control_Set_with_Telemetry_and_GPS_915Mhz_.html)
    - [3D Robotics Store](https://store.3drobotics.com/products/3dr-pixhawk) (GPS and telemetry not bundled)
-   Accessories:
    - [Digital airspeed sensor](http://www.hobbyking.com/hobbyking/store/__62752__HKPilot_32_Digital_Air_Speed_Sensor_And_Pitot_Tube_Set.html)
    - [Hobbyking Wifi Telemetry](http://www.hobbyking.com/hobbyking/store/__87841__APM_Pixhawk_Wireless_Wifi_Radio_Module.html)
    - [Hobbyking OSD + US Telemetry (915 MHz)](http://www.hobbyking.com/hobbyking/store/__74651__Micro_HKPilot_Telemetry_Radio_Module_with_On_Screen_Display_OSD_unit_915MHz_.html)
    - [Hobbyking OSD + EU Telemetry (433 MHz)](http://www.hobbyking.com/hobbyking/store/__74650__Micro_HKPilot_Telemetry_Radio_Module_with_On_Screen_Display_OSD_unit_433MHz_.html)

## Connectivity

- 1x I2C
- 1x CAN (2x optional)
  - 1x ADC
  - 4x UART (2x with flow control)
  - 1x Console
  - 8x PWM with manual override
  - 6x PWM / GPIO / PWM input
  - S.BUS / PPM / Spektrum input
  - S.BUS output

## Pinouts and Schematics

The board is documented in detailed on the [Pixhawk project](https://pixhawk.org/modules/pixhawk) website.
