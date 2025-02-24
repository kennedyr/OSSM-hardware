# OSSM V3 Board info

## V3 Changes

1. ESP32 -> ESP32-S3
2. Current monitor is changed from an analog monitor to an in-line resistor and the INA219.

## Beta 1 testing

1. Motor motion
    1. The U8g2 library doesn't play nice with other devices on the I2C bus. There are a few different things happening here.  First, the bus maxes out the clock speed per the display.  Second the code doesn't want to play nice with the buffers
1. General Connections
    1. The Encoder wheel's A/B lines are swapped. (Or somehow the encoder works backwards)
1. RS485 works-ish.
    1. Packets are being sent and recieved, but the motor is responding with a function code that isn't listed.
    1. The RE/DE pins should be shorted in HW.  (Probably using a solder jumper)
1. Neopixel Works with the FastLED library.
1. TODO: HUSB238 I2C connection. Not critical to check, but should be moved with INA219

### Beta1 -> RC1 Changes

1. Move display to it's own I2C periphal.
1. Change HUSB28 to HUSB238A.  It is available on LCSC and will allow higher power.
    1. Double check all components to handle max voltage.  Should that be 36V (Gold motor max) or 48V (IC max)
1. Make the programmable LED smaller
1. Swap Encoder A/B pins
1. Short the DE and RE pins
1. Shrink Q1&Q2
1. Pick final connectors for Motor connection (both power/pulse/dir and RS85)
1. Pick connector for remote
1. Change PCB form factor
