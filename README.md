# I2C-SD-Card
Arduino code for a custom I2C based SD Card Module. 

Note: This may only work for the ATtiny1624 and 1614 and others with RAM above 900bytes (which is about the size needed by the Arduino SD card library)

The project is based on the work of David Johnson-Davies and Spence Konde's Mega Tiny Core.

CC BY 4.0
Licensed under a Creative Commons Attribution 4.0 International license: 
http://creativecommons.org/licenses/by/4.0/

Guide 
Compile the program using Spence Konde's megaTiny Core on GitHub. You can follow this Guide ( https://www.electronics-lab.com/project/using-new-attiny-processors-arduino-ide-attiny412-attiny1614-attiny3216-attiny1616-attiny3217/ ) to figure out how to connect the attiny to Arduino and use the core for programming. 

Within the Arduino IDE:

Select the ATtiny3224/1624/1614/1604/824/814/804/424/414/404/241/204 option under the megaTinyCore heading on the Board type menu. 

Ensure the chip and clock options are set as indicated below (ignore any other options):

Chip: "ATtiny1614" (or as appropriate)
Clock: "20 MHz internal"

Usage: 
The default I2C address is 0x55 but you can change it within the code. 
After uploading the code, Connect the MCU to your I2C SD Card as shown below (just regular I2C connection with an arduino uno used as an example)

Uno - I2C SD card Board
5v - VCC (pin 1 on the ATtiny1641).
GND - GND (pin 14 on the ATtiny1641).
A4 - SDA (pin 8 on the ATtiny1641).
A5 - SCL (pin 9 on the ATtiny1641).
You can go ahead and try this with the example Arduino interface script provided.


**Regular SD-Card Baord with Attiny**
If you don't have the custom board, you can still connect a regular SPI SD card module to an ATTiny for the same purpose. 
Connect the SPI SD Card module to the Attiny as shown below; 
SD Module   -  Attiny1614
    CLK     -  PA3
    DO      -  PA2
    DI      -  PA1
    CS      -  PA4
    and of course common ground and VCC.

