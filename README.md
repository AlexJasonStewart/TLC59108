# TLC59108 Library for Arduino Core RP2040 (Raspberry Pi Pico)

Modified Arduino library to control TI TLC59108 LED drivers using the new Mbed based ArudinoCore for RP2040.

This library is a fork of Chrylis's original Arduino library. It has been changed to work with pointers to the I2C perhipheral interfaces.

Has been tested using a Raspberry Pi Pico.

This is my first fork of a library, apologies for any mistakes!

- Used pointer to pass desired I2C perhipheral interface to the library.
- I2C setup in example sketch using arduino::MbedI2C i2c0(SDA0,SCL0); allowing for multiple I2C interfaces and any compatible pins to be used.
- Used convention to add underscore infront of private variables such as _i2c and _addr
- Removed ambiguity between setAllBrightness(const uint8_t dutyCycle) and setAllBrightness(const uint8_t dutyCycles[]) by changing second function name to setAllBrightnessArray
