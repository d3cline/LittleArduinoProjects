# FM/TEA5767

Control the TEA5767 low-power FM stereo radio chip with an Arduino.

![Build](./assets/TEA5767_build.jpg?raw=true)

[:arrow_forward: return to the LEAP Catalog](http://leap.tardate.com)

## Notes

A couple of TEA5767 Low-power FM stereo radio chips landed in my lap.
They arrived mounted on a small module board with all the essential supporting circuitry,
so they should be ready to run without much external hardware.

This project is a simple test drive under Arduino control.



### TEA5767 Key Features

Picking the eyes form the data sheet:

* FM mixer for conversion to IF of the US/Europe (87.5 MHz to 108 MHz) and Japanese (76 MHz to 91 MHz) FM band
* I²C -bus and 3-wire bus, selectable via pin BUSMODE
* 4-bit level information output via the bus
* stereo output
* audio frequency output voltage 60-90mV
* total harmonic distortion 1% max
* supply voltage 2.5-5.0V
* max total current approx 11mA @ 3V


### TEA5767 Module

The TEA5767 chip itself is a 40-pin package. I have it mounted on a module board with most of the required supporting
components. It exposes only 10 pins:

| Pin | Name    | Description                                  |
|-----|---------|----------------------------------------------|
|  1  | SDA     | I²C data                                     |
|  2  | SCL     | I²C clock                                    |
|  3  | BUSMODE | bus mode select input                        |
|  4  | W/R     | write/read control input for the 3-wire bus  |
|  5  | VCC     | 2.5-5V                                       |
|  6  | GND     | ground                                       |
|  7  | ROUT    | right audio out                              |
|  8  | LOUT    | left audio out                               |
|  9  | MPXO    | FM demodulator MPX signal output             |
|  10 | ANT     | antenna in                                   |


## Construction

![Breadboard](./assets/TEA5767_bb.jpg?raw=true)

![Schematic](./assets/TEA5767_schematic.jpg?raw=true)

![Build](./assets/TEA5767_build.jpg?raw=true)

## Credits and References
* [TEA5767 datahseet](https://www.sparkfun.com/datasheets/Wireless/General/TEA5767.pdf)
* [FM radio receiver for your Arduino (TEA5767/TEA5768/TEA5757)](https://macduino.blogspot.sg/2014/12/FM-Radio-TEA5767.html)
* [TEA5767 FM Radio Breakout Board for Arduino](http://www.instructables.com/id/TEA5767-FM-Radio-Breakout-Board-for-Arduino/)
* [Arduino FM receiver with TEA5767](https://www.electronicsblog.net/arduino-fm-receiver-with-tea5767/) - nice example using the Wire library
* [TEA5767 FM Radio Library for Arduino](http://playground.arduino.cc/Main/TEA5767Radio)
* [Radio FM TEA5767](https://developer.mbed.org/users/edodm85/notebook/radio-fm-tea5767/) - ARM mbed example