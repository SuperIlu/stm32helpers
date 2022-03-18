# stm32helpers
STM32CubeMX configs and some notes to get started with STM32 development on the boards I own.
Both IOC are configured to generate [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html) projects.

## STM32f103C8Tx aka BluePill
This directory contains a configuration for LED, USB (virtual COM port), both crystals (32kHz and 8MHz) and 72MHz HCLK

### SWD connection info
SWD connector is
```
----+
 B  |
 O  +-- 3v3
 T  +-- SWIO
 T  +-- SWCLK
 O  +-- GND
 M  |
----
```
Connection mode must be set to "under reset"

## STM32f051R8Tx aka stm32f0discovery
This directory contains a configuration for the discovery board: both LEDs, pushbutton (input) and 48MHz HCLK

## ISP
### stm32f0discovery
This is the pinout for the SWD (cn3) connector on the discovery board
```
* . TARGET_VDD
  . SWDCLK
  . GND
  . SWDIO
  . RESET
  . 
```

### Dongle pinout
This is the pinout of my cheap USB dongle
```
      +--+
RESET |..| 3v3
      |..| SWDCLK
       ..| SWDIO
  GND |..| 
      |..| 
      +--+
```
