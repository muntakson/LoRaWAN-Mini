# LoRaWAN-Mini
Low cost arduino compatible board with RFM95 module for LoRaWAN application development.
* A very simple board based on Arduino Pro Mini (ATmega328p-3.3v-8MHz)
* Bootloader same as Arduino Pro Mini (ATmega328p-3.3v-8MHz). Fuse setting - L-fuses=0xFF, H-fuses=0xDA, E-fuses=0x05 
![board_image](https://github.com/LowPowerDesignLab/LoRaWAN-Mini/blob/master/img/lorawan_mini.png)

## Hardware
### Setting up LoRaWAN-Mini for LoRaWAN Applications (LoRa-PHY with LoRaWAN protocol)
#### Arduino and RFM95 connections for LoRaWAN
  ~ | Arduino | RFM95 | ~
------|-----------  | ---------- | -------
MISO  |  D12        | MISO | SPI data out 
MOSI  |  D11        | MOSI | SPI data in
SCK   |  D13        | SCK  | SPI clock
SS    |  D10        | NSS  | SPI chip select  
INT0  |  D2         | DIO0 | ~
~     |  D7         | DIO1 | **Required (close jumper)**
~     |  D8         | DIO2 | **Required (close jumper)**
~     |  D9         | RESET | **Required (close jumper)**
#### List of Library Tested
| Library Name | Status |
|--------------|--------|
| [Arduino-LMIC](https://github.com/matthijskooijman/arduino-lmic) | :ballot_box_with_check: |

### Setting up LoRaWAN-Mini for non-LoRaWAN Applications (LoRa-PHY without LoRaWAN protocol)
#### Arduino and RFM95 connections for LoRaWAN
  ~ | Arduino | RFM95 | ~
------|-----------  | ---------- | -------
MISO  |  D12        | MISO | SPI data out 
MOSI  |  D11        | MOSI | SPI data in
SCK   |  D13        | SCK  | SPI clock
SS    |  D10        | NSS  | SPI chip select  
INT0  |  D2         | DIO0 | ~
~     |  D7         | DIO1 | **Not Required (open jumper)**
~     |  D8         | DIO2 | **Not Required (open jumper)**
~     |  D9         | RESET | **Not Required (open jumper)**

#### List of Library Tested
| Library Name |
|--------------|
| [RadioHead by AirSpayce](https://github.com/hallard/RadioHead) |
| [MySensor](https://github.com/mysensors/MySensors) |

#### Power
