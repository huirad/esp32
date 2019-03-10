# esp32
My ESP32 Howto's and Projects

## general info on the ESP32
The ESP32 is an IoT Controller with built-in WiFi, Bluetooth and some other promising features.
such as low power modes, 12 bit ADC, one-time programmable meory and a crypto accelerator.

Development boards with USB-serial interface are available for less than 10EUR.
This makes it interesting for hobby projects for which a similarly prized and sized Raspberry Pi Zero W
consumes too much power or is missing features such as an ADC.

Programming is possible with the Arduino IDE or the native SDK using Linux or Windows as host OS.


References 

* [espressif.com](https://www.espressif.com/en/products/hardware/esp32/overview)
* [heise developer 2016](https://www.heise.de/developer/artikel/ESP32-Neuer-IoT-Chip-von-Espressif-3506140.html)
* [c't 2018/12](https://www.heise.de/select/ct/2018/12/1527917618510644)
* [Power Consumption](https://arduino-hannover.de/2018/07/11/esp32-mit-batteriebetrieb/)
* [TamHanna](https://chemnitzer.linux-tage.de/2018/media/programm/papers/229_ESP32_Preiswert_WLAN_und_gut_folien_ESP32.pdf)

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

To use the [Arduino core for ESP32 WiFi chip](https://github.com/espressif/arduino-esp32), 
you have to install the packages to the Arduino IDE as descrribed 
[here](https://github.com/espressif/arduino-esp32/blob/master/docs/arduino-ide/boards_manager.md)

Tips
* UART 115200
* #define LED_BUILTIN 1



### 3. run some examples
* blink
* Wifi list
* Wifi-AP


## Using the native SDK
* [GetStarted](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/index.html)
* [LinuxSetUp](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/linux-setup.html)
* [API Reference](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/index.html)
* [I2C](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/i2c.html)
* [HW Reference](https://docs.espressif.com/projects/esp-idf/en/latest/hw-reference/index.html)

## Connecting the Sensirion SCD30 Carbon Dioxide Sensor
The [Sensirion SCD30](https://www.sensirion.com/en/environmental-sensors/carbon-dioxide-sensors-co2/) Carbon Dioxide Sensor
(see also
[1](https://www.soselectronic.de/articles/sensirion/der-scd30-ist-mehr-als-nur-ein-ndir-co2-sensor-2152)
[2](https://www.soselectronic.de/products/sensirion/scd30-1-290529)
) can be accessed via I2C. See 
https://github.com/paulvha/scd30 or 
https://github.com/Sensirion/embedded-scd
