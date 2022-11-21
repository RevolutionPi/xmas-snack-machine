# Raspberry Pi Pico PIO NeoPixel

The following code can control a definable amount of NeoPixel LEDs based on the
WS2812 or SK6812 controller. The library is a shameless copy from 
https://github.com/blaz-r/pi_pico_neopixel.

## Setup Python on the Pi Pico

If you have a Raspberry Pi Pico without Python installed, grab the precompiled
binary from https://micropython.org/download/rp2-pico/rp2-pico-latest.uf2, press
and hold the `BOOTSEL` button and connect it to a USB port on your computer. A
storage device should show up. Drag & drop or copy the file `rp2-pico-latest.uf2`
to the mass storage device. The Pico should now have Python installed. Maybe a
power cycle of the pico is necessary.

### Verify Python installation

A new serial port device should show up when connecting the Pi Pico to a computer. Use
any console/terminal program to connect to it, e.g. picocom on Linux or putty on
Windows.

Connection details are 115200 baud, 8 data bits, no parity and one stop bit. If successful,
you should see the Python REPL console `>>>`. If not, hit enter once. If nothing shows
up, reprogram the device.

Now you can try one of the examples from https://datasheets.raspberrypi.com/pico/raspberry-pi-pico-python-sdk.pdf
like the blinky example. See chapter 2.4 and 2.5 in the dataseeht above.

## Installing a python script

To copy a python script permanent to the device, rshell is one of the tools to achieve
this. Install it with either python pip or with a package manager. After it is installed,
one can write the script onto the board with the following line:

`rshell -p /dev/ttyACM0 --buffer-size 512 cp pico_ws2812_pio.py /pyboard/main.py`

Now should the script start automatically on each power up of the board.
