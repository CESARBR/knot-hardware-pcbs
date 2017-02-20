##KNoT Hardware PCBs

These are the open-source hardware PCBs of the KNoT Project.

###Overview

####KNoT Gateway Starter Board

KNoT Gateway Starter Board consists on a shield for Raspberry Pi with headers for easily coupling a nRF24L01+ module for wireless communication with the KNoT Things. It also includes push buttons and status leds. This is a support hardware that is build from the integration of existing modules for I/O, radio communication and power supply. These boards ease distribution and popularization of KNoT platform because they're cheap and easier to distribute to the community.

####KNoT Thing Development Board

KNoT Thing Development Board consistes on an Arduino based PCB with the ATMega328 microcontroler, nRF24L01+ circuit, headers for SPI and I²C communication, push button and status led. This Board is self contained and has two goals: (i) to serve as a development platform with embedded firmware for prototypes that can be validated on field and (ii) to serve as baseline for specific hardware development for final products, as schematics and layouts can be rapdily customized to attend to specific demands.

#####Characteristics

 - Suports KNoT version 01.00
 - Compatible with Arduino IDE
 - Supplied via Micro-USB conector
 - nRF24L01+ radio with external antenna
 - ATMega328-AU Microcontroller
 - Programmed through FTDI232RL USB-Serial conversor


KNoT Thing DevBoard PCBs are compatible with the Arduino IDE and may be integrated with peripherals through expantion connectors.
Before using the PCB, it's importante to burn the bootloard to the Atmega328 microcontroller. For this PCB, the Arduino Pro Mini 3.3V 8MHz bootloader is used ([ATmegaBOOT_168_atmega328_pro_8MHz.hex](https://github.com/arduino/Arduino/blob/master/hardware/arduino/avr/bootloaders/atmega/ATmegaBOOT_168_atmega328_pro_8MHz.hex)). The use of ICSP is recommended for burning the bootloader via the 3x2 header with SPI interface using an Atmel SPI Programmer and Atmel Studio. Besides burning the bootloader, the ATMega328 fuses also need to be programmed via ICSP with the values:
 - Extended: 0xFD
 - High: 0xDA
 - Low: 0xFF

###Development tools

The ECAD tool used is Altium Designer versions 14.2.3 and 14.2.4.


###PCB Files

Each PCB project includes:
 - Components Library
 - Schematics
 - Board Layout

The generated output files are:
 - Bill Of Materials
 - Gerber
 - NC Drill
 - PCADNetlist
 - Assembly Drawing
 - Composite Drawing
 - Pick and Place
 - Schematics (PDF)
