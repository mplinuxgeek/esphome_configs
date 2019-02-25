Tuya RGBW MY9291
==================================
The globe is a GU10 RGBW purchased from ebay and made by Tuya, Tuya are a Chinese company that design and maufacture devices to sell to vendors along with their cloud platform.

The globes use an ESP8266 module with 1MB flash and an MY9291 LED driver which is described as "3 or 4 channel (RGBW) constant current APDM (Adaptive Pulse Density Modulation) LED driver". It appears to be identical to the PCB's used in the AILight and uses the same pin mappings.

### GPIO Assignments
| PIN | Output |
| - |:-:|
| GPIO13 | Data (DI) |
| GPIO15 | Clock (DCK) |

### Flashing alternate firmware
You can open the globe and physically solder wires to the relevant pins of the TYWE3S module however there are now various OTA flashing methods, I have tested and confirmed tuya-convert from VTRUST/c't magazine working with these globes.

https://github.com/ct-Open-Source/tuya-convert
Following the instructions at the tuya-convert page results in a globe flashed with Tasmota however I find this to give strange behaviour with the globe randomly turning on and off, I have switched to ESPHome to see how it compares.
