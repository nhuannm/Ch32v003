systemtick, RF24, SERVOR ==> https://github.com/MangnimitMCU/CH32V003F4P6/tree/main

https://github.com/sshahryiar/CH32-RISC-V-Tutorials/tree/main
#NF24
https://github.com/MangnimitMCU/CH32V003F4P6_NRF24
#2025-09-12
- PA1/A0/ADC_Channel_0, PA2/A1/ADC_Channel_1 2 chân này dùng để kết nối dao động ngoài 48Mhz. Nếu muốn sử dụng để ADC phải tắt chức năng lấy dao động ngoài là HSE, chỉ chạy HSI
- ==> Trong system_ch32v00x.c phải khai báo HSI
  * Uncomment the line corresponding to the desired System clock (SYSCLK) frequency (after 
* reset the HSI is used as SYSCLK source).
* If none of the define below is enabled, the HSI is used as System clock source. 
//#define SYSCLK_FREQ_8MHz_HSI    8000000
//#define SYSCLK_FREQ_24MHZ_HSI   HSI_VALUE
//#define SYSCLK_FREQ_48MHZ_HSI   48000000 //nếu dùng PA1, PA2 làm IO
//#define SYSCLK_FREQ_8MHz_HSE    8000000
//#define SYSCLK_FREQ_24MHz_HSE   HSE_VALUE
//#define SYSCLK_FREQ_48MHz_HSE   48000000 //default

Trong CH32FUN khai báo funconf.h
#ifndef _FUNCONFIG_H
#define _FUNCONFIG_H
#define FUNCONF_USE_UARTPRINTF 1  // Enable UART printf
#define FUNCONF_UART_PRINTF_BAUD 9600
#define FUNCONF_USE_HSI 1 //dùng PA1, PA2 như IO
#define FUNCONF_SYSTICK_USE_HCLK 1
#define SSD1306_128X64
#define I2C_PINOUT_DEFAULT
#define I2C_PINOUT_DEFAULT
#define CH32V003           1

#endif
///

###
ch32v003 rất nhiều ứng dụng:
http://blog.livedoor.jp/yokoshima_m/archives/cat_400619.html

Curious Scientist https://youtu.be/LcPfUYLC9L4?si=t3wY9MH_6RQ6ghd_
# Ch32v003
https://github.com/cnlohr/ch32fun/issues/152
https://github.com/74th/ch32v003-book-code
https://github.com/cnlohr/ch32fun
https://github.com/wagiminator/ATtiny412-BatteryCapacityTester
https://github.com/shakir-abdo/ch32v003-gps
https://github.com/ADBeta/CH32V003_lib_uart/tree/main
https://github.com/ohdarling/CH32V003-USBMeter
https://github.com/MoonFox2006/CH32V003_INA226/tree/main

https://github.com/kzkmy/CH32V003_SSD1306_Example

https://github.com/c3am/resistive-BMS
https://github.com/shakir-abdo/CH32V003J4M6-uart/tree/main/src
https://github.com/Keisuke-Hongyo/IRReciver/tree/main/src

điều khiển motor qua serial
https://github.com/ycan78/CH32V003F4P6

nrf24l01

https://git.c3pb.de/ahorn/ch32v003fun/-/tree/4d74869c009ebe2cc2d7c2c892cf9212bf9e90d8/examples/spi_24L01_tx

encoder dùng ch32v03m4 output i2c
https://github.com/wagiminator/CH32V003-I2C-Knob.git



##https://github.com/sshahryiar/CH32-RISC-V-Tutorials
https://github.com/MoonFox2006 //CH32v003, esp32, arduino
https://github.com/ichiro-art/ch32v003_ds1307_clock

https://github.com/sshahryiar/CH32-RISC-V-Tutorials/blob/main/OW_and_Timer_Interrupt/User/DS18B20.c
https://github.com/roboter/Hardware/tree/main/WCH
