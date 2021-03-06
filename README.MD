# **OpenSprinkler for Generic esp8266 relay module**

This is the unified OpenSprinkler firmware adapted to runs on Generic esp8266 relay module, without a display and expansion boards.

This current configuration is designed to run on [LinkSprite R8](https://www.amazon.com/LinkSprite-211201005-Arduino-Compatible-Wi-Fi-Controller/dp/B01N2ALK8X/ref=sr_1_1?dchild=1&keywords=linksprite+r8&qid=1586153135&sr=8-1)
# Building the firmware

## Mappings

Internals:
  - Blue LED or WiFi LED show WiFi connectivity status: ON=WiFi Connected / SlowBlink=Connecting / FastBlink=Initializing
  - Stations 1 to 8 are mapped to Relays 1 to 8.
Externals:


## Ardunino IDE

### First, configure the IDE:
  - Add this URL to the Board Manager : http://arduino.esp8266.com/stable/package_esp8266com_index.json
  - Additional info https://github.com/esp8266/Arduino
  - Install the ESP8266 version 2.4.1 with the Arduino IDE Board Manager Menu
  - Configure board options as follows:
  
![alt text](https://github.com/enosrevlah/OpenSprinkler-Sonoff4ch/blob/master/Settings.PNG)

### Second, Download source and make change.
  - Download the code in .zip format.
  - Extract zip file.
  - Edit the defines.cpp PIN_RELAY_1-8 to match your boards gpio layout.

### Third, Create .bin and upload. 
  - In Arduino IDE, open OpenSprinkler-Sonoff4ch/OpenSprinkler-Sonoff4ch.ino
  - In Arduino IDE, go to Sketch and Verify/Compile.
  - In Arduino IDE, go to Sketch and Export Compiled Binary. The newely compiled .bin should now be in the source directory.
  - Upload the .bin with your preferred program.
