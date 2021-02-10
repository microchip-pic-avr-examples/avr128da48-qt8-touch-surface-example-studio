INTRODUCTION
============
This is the documentation for the Tocuh AVR128DA48 Curiosity Nano with QT8 Xpro.

Example description
===================
This example demonstates the basic touch application where the touch sensors are measured and the touch status is indicated using LED. The touch library parameters are also displayed in the datavisualizer software when the hardware kit is connected through edbg/medbg vritual com port.

RELATED DOCUMENTS / APPLICATION NOTES
=====================================
Refer the microchip developer page link `"Generate Atmel Board User Project" <http://microchipdeveloper.com/touch:generate-atmel-board-touch-project>`_.

SUPPORTED EVALUATION KIT
========================
	* `AVR128DA48-CNANO <https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/DM164151>`_
	* `Curiosity Nano Touch Adaptor <https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/AC80T88A>`_
	* `QT8 Xplained Pro Extension Kit <https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/AC164161>`_

INTERFACE SETTINGS
==================
	* RTC clock: 32KHz
	* CPU Clock Frequency: 24MHz
	* Surface Utility port pins: PB1/PB0, 38400
	* Connection: Connect QT8 XPRO to EXT1 of Curiosity Nano Touch Adaptor board.

Note: The J2 jumper on QT8 XPRO must be selected to "SAM".
Supports only Surface utility. On board LEDs on QT8 not supported.
	
RUNNING THE DEMO
================
1. Select "EXPORT PROJECT" tab and click "Download Pack" to save the .atzip file.
2. Import .atzip file into Atmel Studio 7, File->Import->Atmel Start Project.
3. Build Solution and make sure no compiler errors occur.
4. Press "Start without debugging" or use "CTRL+ALT+F5" hotkeys to run the application.
6. Open Microchip 2D Touch Surface Utility and select UART wiht 38400 baud rate and click OK.
7. Open serial port connection and connect to the target. Verify the connection is made successfully and the touch status is displayed on the dashboard. 