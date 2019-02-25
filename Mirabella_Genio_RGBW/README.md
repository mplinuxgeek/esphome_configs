
Mirabella Genio RGBW
==================================
Mirabella sell Genio branded devices manufactured by Tuya, Tuya are a Chinese company that design and maufacture devices to sell to vendors along with their cloud platform.

The globes use a TYWE3S microcontroller which is an ESP8266 based module with 1MB flash. The globes use simple PWM GPIO outputs to drive the LEDs making them easy to use with 3rd party firmware.

The white channel is driven by a SM2083EGL which is described as a "Single channel dimmable LED linear constant current control chip", I can only find Chinese datasheets for these chips.

At this point I am unsure what drives the RGB LEDs but I assume it is also the SM2083EGL as there are 3 other 8 pin chips on the PCB.

### GPIO Assignments
| PIN | Output |
| - |:-:|
| GPIO4 | Red |
| GPIO12 | Green |
| GPIO14 | Blue |
| GPIO5 | White |

### Flashing alternate firmware
You can open the globe and physically solder wires to the relevant pins of the TYWE3S module however there are now various OTA flashing methods, I have tested and confirmed tuya-convert from VTRUST/c't magazine working with these globes.

https://github.com/ct-Open-Source/tuya-convert
Following the instructions at the tuya-convert page results in a globe flashed with Tasmota however I find this to give strange behaviour with the globe randomly turning on and off, I have switched to ESPHome to see how it compares.
