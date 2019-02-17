# esp32
My ESP32 Howto's an Projects

## Howto setup Arduino for ESP32 on openSUSE Leap 15.0, 64bit, KDE

### 1. set up the Arduino IDE
Basically, follow the guideline from 
[Arduino- Linux](https://www.arduino.cc/en/guide/linux)

* Download the Linux 64-bit package from the [Arduino Download page](https://www.arduino.cc/en/Main/Software)
  * unpack the archive 
  * running the install script did not work for me. Instead I manually created a link on the desktop and associated it with some icon which downloaded from the internet
* add your current user to the `dialout` group
* install the `pyserial` package for python 2 using `yast`

### 2. install the ESP32 board files
**TODO**

https://www.az-delivery.de/blogs/azdelivery-blog-fur-arduino-und-raspberry-pi/esp32-jetzt-mit-boardverwalter-installieren?ls=de
https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-mac-and-linux-instructions/
https://oneguyoneblog.com/2018/08/06/esp32-arduino-ide-linux-windows/

### 3. run some examples
* blink
* Wifi list
* Wifi-AP


## Using the native SDK
