# APP-ESS-2025-Example for PIC32CM5164JH01048
APP-ESS-2025 PIC32CM5164JH01048 的範例，除了 I2C， UART, CAN 的範例程式也包含電路圖
* APP-ESS-2025 是Microchip Taiwan 為了 2025 Microchip 科技論壇所開發的一款多功能實驗板，旨在於提供簡單並實用的開發工具，讓廣大的 Microchip 之友們可以用最精及實惠的方式，來體驗 Microchip 新型 MCU 的強大功能。
* APP-ESS-2025 EVB 上面預置的兩個 MCU 為 PIC32CM5164JH01048 以及 PIC16F13145

<img src="https://github.com/CalvinHoMicrochip/APP-ESS-2025-Example-for-PIC32CM5164JH01048/blob/main/APP_ESS_2025_Picture1.jpg" width="640px">
  
* PIC32CM5164JH01048 為 Microchip 最新的 Arm® Cortex®-M0+ MCU 具備以下特點 
  * 48 MHz 操作頻率 (2.46 CoreMark/MHz) 
  * Single-cycle 硬體乘法器 
  * 工作電壓 : 2.7 ~ 5.5V 
  * 512 KB Flash, 64KB SRAM  
  * 12-channel 的 DMA & Event System 
  * 多種 Security & Safety 功能，包含 Size-configurable immutable boot section in Flash for Secure Boot 
  * 2 個支援 CAN-FD 協議的Controller Area Network (CAN) Interfaces  
  * 完整的通信協定支援，包含 : USART, I2C, LIN Host/Client, SPI, RS485 ，PMBusTM, SMBusTM
* 正因如此，我們再次提供多個由淺入深的範例，包含以下的練習 :
  * PIC32CMJH_Startup : 最基礎的 Timer & GPIO 設定及使用
  * PIC32CMJH_基礎周邊範例 : UART & I2C 控制 OLED、MCP9800A5、Lighting Sensor 
  * APP_ESS_2025 出廠測試程式 - 包含 CAN Communication 的基礎實現
  * LIN Communication
* PIC32CMJH_基礎周邊範例 - 以下為此專案的 Harmony Project Builder 的使用物件
<img src="https://github.com/CalvinHoMicrochip/APP-ESS-2025-Example-for-PIC32CM5164JH01048/blob/main/PIC32CM5164JH_Harmony_Project1.jpg" width="640px">

* APP_ESS_2025 出廠測試程式
  *  這是延續 PIC32CMJH_基礎周邊範例，再加上 CAN0 通信的範例。CAN0 被規劃為使用 Classic CAN, 125K, Standard ID 來簡化使用 CAN 時的設定，建立基本概念
    *  PIC32CMJH 定時地將 ADC 所讀取的 VR 值以 CAN 的封包送出
    *  處此之外，PIC32CMJH 也持續的監看 CAN 的接收，將 CAN SID = 0x200 的封包接收並解析，然後將對方的 ADC 讀值顯示於 OLED 
