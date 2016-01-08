# Arduino custom serial buffers

Implementation of separate RX and TX buffers for the serial port of the Arduino boards (tested with Arduino Uno only). This allows to choose separately the size of the RX and TX buffers. The change is obtained by doing a few modifications in the arduino core obtained through the Arduino IDE version 1.0.5.

# Installation

To install the code, copy the whole arduino_CustomBuffer folder and all its content as /hardware/arduino/cores/arduino_CustomBuffer in the tree of the code for your Arduino IDE and add the following declaration to your boards.txt file, located in hardware/arduino/boards.txt . For more information about the code Mod, see my website: ADD LINK.

 ##############################################################
 
 # an arduino uno on which the serial buffer sizes have been
 # modified

 unoCB.name=Arduino Uno (Custom Buffer)
 unoCB.upload.protocol=arduino
 unoCB.upload.maximum_size=32256
 unoCB.upload.speed=115200
 unoCB.bootloader.low_fuses=0xff
 unoCB.bootloader.high_fuses=0xde
 unoCB.bootloader.extended_fuses=0x05
 unoCB.bootloader.path=optiboot
 unoCB.bootloader.file=optiboot_atmega328.hex
 unoCB.bootloader.unlock_bits=0x3F
 unoCB.bootloader.lock_bits=0x0F
 unoCB.build.mcu=atmega328p
 unoCB.build.f_cpu=16000000L
 unoCB.build.core=arduino_CustomBuffer
 unoCB.build.variant=standard

 ##############################################################

# Using the code Mod

To use the code mod, select Arduino Uno (Custom Buffer) in the board menu of the Arduino IDE.
