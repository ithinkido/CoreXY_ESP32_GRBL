

# Grbl (CNC Controller) Using ESP32 for CORE XY

Setup for use with the custom plotter board.
This board includes software control over the microstep pins. The microsteps are defined in EggBot_coreXY.cpp ( currently configured for 1/32 with DRV8825)
### Pin out

  - x step 17
  - x dir 4
  - 
  - y step 2
  - y dir 15
  - 
  - servo pen lift 32
  - 
  - motor enable 27
  - U step 0
  - U step 1
  - U step 2

### Changes / configuration files

Grbl_Esp32\Custom\Eggbot_coreXY.cpp

Grbl_Esp32\src\Machines\EggBot_coreXY.h


### Project Overview

Grbl_ESP32 started as a port of [Grbl](https://github.com/gnea/grbl) to the ESP32. The power of the ESP32 has allowed this firmware to grow far beyond the limitations of 8-bit AVR controllers. Here are some of the current features

- **Connectivity**
  - USB/Serial
  - Bluetooth/Serial Creates a virtual serial port on your phone or PC. Standard serial port applications can use Bluetooth.
  - WIFI
    - Creates its own access point or connects to yours.
    - Built in web server. The server has full featured CNC control app that will run on your phone or PC in a browser. No app required.
    - Telnet sending of gcode
    - Push notifications (like...job done, get a text/email)
    - OTA (over the air) firmware upgrades.
- SD card. Gcode can be loaded and run via WIFI.
- **Compatibility** 
  - Grbl_ESP32 is fully backward compatible with Grbl and can use all gcode senders.
- Fast boot
  
  - It boots in about 2 seconds (unlike Raspberry Pi, Beagle Bone). Does not need to be formally shut down. Just kill the power


### Using It

Important compiling instructions are [in the wiki](https://github.com/bdring/Grbl_Esp32/wiki/Compiling-the-firmware)

The code should be compiled using the latest PlatformIO. 

I use the ESP32 Dev Module version of the ESP32. I suggest starting with that if you don't have hardware yet.

For basic instructions on using Grbl use the [gnea/grbl wiki](https://github.com/gnea/grbl/wiki). That is the Arduino version of Grbl, so keep that in mind regarding hardware setup. If you have questions ask via the GitHub issue system for this project.
