# PCB for the Adafruit Flora Ultimate GPS

<a href="http://www.adafruit.com/products/1059"><img src="assets/image.jpg?raw=true" width="500px"><br/>Click here to purchase one from the Adafruit shop</a>

__Format is EagleCAD schematic and board layout__

This module is the best way to add a GPS to your wearable project. It's part of the Adafruit Flora series of wearable electronics, designed specifically for use with the Flora motherboard. Installed on the PCB is the latest of our Ultimate GPS modules, a small, super-thin, low power GPS module with built in data-logging capability! This module's easy to use, but extremely powerful:

- -165 dBm sensitivity, 10 Hz updates, 66 channels
- Designed for wearable use with the Flora system
- Only 20mA current draw
- RTC battery-compatible - sew a battery on to create a atomic-precision real time clock
- Built-in datalogging
- Internal patch antenna + u.FL connector for external active antenna
- Fix status LED

...all for under $40!

The breakout is built around the MTK3339 chipset, a no-nonsense, high-quality GPS module that can track up to 22 satellites on 66 channels, has an excellent high-sensitivity receiver (-165 dB tracking!), and a built in antenna. It can do up to 10 location updates a second for high speed, high sensitivity logging or tracking. Power usage is incredibly low, only 20 mA during navigation.

The module is kept small and simple, we have a ferrite bead, filter capacitor and red fix LED on board. The LED blinks at about 1Hz while it's searching for satellites and blinks once every 15 seconds when a fix is found to conserve power. If you want to have an LED on all the time, we also provide the FIX signal out on a pin so you can put an external LED on.

Two features that really stand out about the MTK3339-based module is the external antenna functionality and the the built in data-logging capability. The module has a standard ceramic patch antenna that gives it -165 dB sensitivity, but when you want to have a bigger antenna, you can snap on any 3V active GPS antenna via the uFL connector. The module will automatically detect the active antenna and switch over! [Most GPS antennas use SMA connectors so you may want to pick up one of our uFL to SMA adapters.](http://www.adafruit.com/products/851)

The other cool feature of the new MTK3339-based module (which we have tested with great success) is the built in datalogging ability. Since there is a microcontroller inside the module, with some empty FLASH memory, the newest firmware now allows sending commands to do internal logging to that FLASH. The only thing is that you do need to have the Flora mainboard send the "Start Logging" command. However, after that message is sent, the Flora can go to sleep and does not need to wake up to talk to the GPS anymore to reduce power consumption. The time, date, longitude, latitude, and height is logged every 15 seconds and only when there is a fix. The internal FLASH can store about 16 hours of data, it will automatically append data so you don't have to worry about accidentally losing data if power is lost. It is not possible to change what is logged and how often, as its hardcoded into the module but we found that this arrangement covers many of the most common GPS datalogging requirements.

Comes with one fully assembled and tested module. If you'd like to back up the RTC for faster fix-recovery, pick up a [sewable CR2032 holder](http://adafruit.com/products/653) & [CR2032 battery](http://adafruit.com/products/654) and sew it so the + side connects to the VBAT pad and the - side connects to ground.

## License
Adafruit invests time and resources providing this open source design,
please support Adafruit and open-source hardware by purchasing
products from Adafruit!

Designed by Adafruit Industries.
Creative Commons Attribution, Share-Alike license, check license.txt for more information
All text above must be included in any redistribution
