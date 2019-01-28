# LoRaWAN-Mini
Low cost arduino compatible MCU board with RFM95 module for LoRaWAN application development.
* A very simple board based on Arduino Pro Mini (ATmega328p-3.3v-8MHz)
* Bootloader same as Arduino Pro Mini (ATmega328p-3.3v-8MHz). Fuse setting - L-fuses=0xFF, H-fuses=0xDA, E-fuses=0x05 
![board_image](https://github.com/LowPowerDesignLab/LoRaWAN-Mini/blob/master/img/lorawan_mini.png)

## Hardware
## Setting up LoRaWAN-Mini for LoRaWAN Applications (LoRa-PHY with LoRaWAN protocol
-------------------------------------------------------------------------------------

#### Arduino and RFM95 connections for LoRaWAN
----------------------------------------------
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
---------------------------
| LoRaWAN Library | Gateway | Status |
|:--------------:|:--------:|:--------:|
| [Arduino-LMIC](https://github.com/matthijskooijman/arduino-lmic) | [IMST iC880A-SPI](https://shop.imst.de/wireless-modules/lora-products/8/ic880a-spi-lorawan-concentrator-868-mhz) | :ballot_box_with_check: |

#### Examples
-------------
##### Arduino-LMIC 
* Pin Mapping
```// Pin mapping - LoRaWAN-Mini 
const lmic_pinmap lmic_pins = {
    .nss  = 10,
    .rxtx = LMIC_UNUSED_PIN,
    .rst  = 9,
    .dio  = {2, 7, 8},  // D0, D1, D2
};
```

## Setting up LoRaWAN-Mini for non-LoRaWAN Applications (LoRa-PHY without LoRaWAN protocol)
---------------------------------------------------------------------------------------------
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
| Library Name | Status |
|:--------------:|:--------:|
| [RadioHead by AirSpayce](https://github.com/hallard/RadioHead) | :black_square_button: |
| [MySensor](https://github.com/mysensors/MySensors) | :black_square_button: |

#### Power
