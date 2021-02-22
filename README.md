<!-- Please do not change this logo with link -->
[![MCHP](images/microchip.png)](https://www.microchip.com)

# Touchpad Example using QT8 and AVR128DA48 Curiosity Nano

This example demonstrates touchpad application on AVR128DA48 Curiosity Nano with QT8 surface extension board. The example project provides user feedback to touch either using the QT8 onboard LEDS, or to a PC running Microchip 2D Surface Utility via USB.

## Related Documentation

- AVR128DA48 Curiosity Nano user guide [(DS50002971B)](https://ww1.microchip.com/downloads/en/DeviceDoc/AVR128DA48-Curiosity-Nano-UG-DS50002971B.pdf)
- Curiosity Nano Touch Adapter Kit user guide [(DS40002191A)](https://ww1.microchip.com/downloads/en/DeviceDoc/40002191A.pdf)
- 2D Surface Utility guide [(Microchipdeveloper)](https://microchipdeveloper.com/touch:guide-to-connect-to-touch-surface-utility)

## Software Used

- Microchip Studio 7 7.0.2542 or later [(microchip-studio-for-avr-and-sam-devices)](https://www.microchip.com/en-us/development-tools-tools-and-software/microchip-studio-for-avr-and-sam-devices)
- AVR-GCC 3.62 or newer toolchain [(Toolchains for AVR)](https://www.microchip.com/en-us/development-tools-tools-and-software/gcc-compilers-avr-and-arm)
- AVR-Dx_DFP (1.6.76) or later [(packs.download.microchip.com)](https://packs.download.microchip.com/)
- 2D Surface Utility [(2D Touch Surface GUI)](https://www.microchip.com/mymicrochip/filehandler.aspx?ddocname=en605897)

## Hardware Used

- AVR128DA48 Curiosity Nano [(DM164151)](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/DM164151)
- Curiosity Nano Touch Adapter Kit [(AC80T88A)](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/AC80T88A)
- QT8 Xplained Pro Extension Kit [(AC164161)](https://www.microchip.com/developmenttools/ProductDetails/AC164161)
## Setup

1. Connect QT8 to Curiosity Nano Touch Adapter Kit (EXT1).
2. Connect Curiosity Nano Touch Adapter Kit to AVR128DA48 Curiosity Nano.
3. Connect PC to the MCU board Debug USB port.

## Operation

1. Open the .atsln file in Microchip Studio.
2. Build the solution and program the device.
3. By default, UART communication is enabled to send data to Microchip Surface Utility (KRONOCOMM_UART macro in touch.h file is 1u).
4. Open Microchip 2D Touch Surface Utility and select UART with 38400 baud rate and click OK.
5. Surface status will be displayed on the utility.
6. To enable LED status:
   - Disable the UART communication by setting KRONOCOMM_UART macro to 0u in touch.h file
   - Enable LED driver by setting ENABLE_LED macro to 1u in led_driver.c file
7. Close the 2D Surface Utility.
8. Rebuild and program the target.    
    NOTE: Either LED or Kronocomm should be enabled, not both simultaneously. Running both will cause 2D utility debug data transmission to be delayed. 

## Summary

This example has illustrated a touch surface with gestures using the AVR128DA48 Curiosity Nano with QT8 extension board.  
