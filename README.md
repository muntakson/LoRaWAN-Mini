# LoRaWAN-Mini
Arduino compatible LoRaWAN board based on RFM95 module
* Based on Arduino Pro Mini (ATmega328p-3.3v-8MHz)
![board_image](https://github.com/LowPowerDesignLab/LoRaWAN-Mini/blob/master/img/lorawan_mini.png)

## Hardware
### Setting up LoRaWAN-Mini for LoRaWAN
#### Arduino and RFM95 connections for LoRaWAN
  ~ | Arduino | RFM95 | ~
------|-----------  | ---------- | -------
MISO  |  D12        | MISO | SPI data out 
MOSI  |  D11        | MOSI | SPI data in
SCK   |  D13        | SCK  | SPI clock
SS    |  D10        | NSS  | SPI chip select  
INT0  |  D2         | DIO0 | ~
~     |  D7         | DIO1 | Required (close jumper)
~     |  D8         | DIO2 | Required (close jumper)
~     |  D9         | RESET | Required (close jumper)
#### List of Library Tested
| Library Name |
|--------------|
| [Arduino-LMIC](https://github.com/matthijskooijman/arduino-lmic) |
