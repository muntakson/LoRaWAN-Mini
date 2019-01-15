# LoRaWAN-Mini
Arduino compatible LoRaWAN board based on RFM95 module
* Based on Arduino Pro Mini (ATmega328p-3.3v-8MHz)
![board_image](https://github.com/LowPowerDesignLab/LoRaWAN-Mini/blob/master/img/lorawan_mini.png)

## Hardware
  | Arduino Pin | RFM95 Pin |
------|-----------  | ---------- | -------
MISO  |  D12        | MISO | SPI data out 
MOSI  |  D11        | MOSI | SPI data in
SCK   |  D13        | SCK  | SPI clock
SS    |  D10        | NSS  | SPI chip select  
INT0  |  D2         | DIO0 |
      |  D7         | DIO1 | Optional
      |  D8         | DIO2 | Optional
      |  D9         | RESET | Optional 
