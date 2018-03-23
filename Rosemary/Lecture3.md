# Table of contents
1. dmesg to check if its connected
The device not getting powered up coz the code 
wemos d1 mini - rfid-rc522 board

3v3 - 3.3V
d8  - sda
d7  - MOSI
d6  - MISO
d5  - SCK
d0  - RST
G   - GND

Add device with:
r=d("mfrc522","r",d0)

upgrade
reinitialize
Chika node3
Special command to connect the device RC522(The card reader) to the node
**command:** d("mfrc522","reader",d0,datasize=0)
datasize is optional but if initialized as 0 we can detect anything, otherwise it is set to the default value.
Got the result- Read two sample cards.

MobaX portable version is creating trouble thus installed MobaX Home edition


Syntax: initialize [serial_port] [noflash] [noupdate]

initialize must be called from a node directory and reads its configuration from there.
It looks for a locally (i.e. via serial) connected board matching the node
description.

It flashes the board with ulnoiot's version of micropython (if noflash is given,
this step is skipped).
It then sets or overwrites wifi and encryption data, respective to the current
node configuration folder.
Then, it calls a local/serial update on it and installs initial system
user-space software.
Then it calls a network deploy to copy the user folder and autostart to it.
The last two steps fail, if the node router and mqtt broker are not available.
Running deploy noupdate again (when router and mqtt broker become avaialable)
fixes/finishes this.

serial_port: can be empty, usb0, usb1, or acm0, acm1, ...

But this didn't work when typed initialize usb1
