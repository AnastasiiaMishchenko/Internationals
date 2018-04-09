# Table of contents

1. [Card Reader](#CardReader)
    1. [RFID Connection](#Card)
    2. [Strength and weaknesses](#strength)
2. [Extras](#extra)

 
## Card Reader <a name="CardReader"></a>

**Issue**:The device not getting powered up 


**Solution**: upgraded and reinitialize Pi


**Mystery** : Chirantha did upgrades & it showed message saying upgraded but no trace of that upgrade was listed when the professor checked!


### RFID Connection<a name="Card"></a>
Connected the wemos d1 mini and the rfid-rc522 board as follows:

3v3 - 3.3V
d8  - sda
d7  - MOSI
d6  - MISO
d5  - SCK
d0  - RST
G   - GND

Initialised and added the device to node3


**Command:**  Special command to connect the device RC522(The card reader) to the node
 ``` d("mfrc522","reader",d0,datasize=0) ```
``` r=d("mfrc522","r",d0) ```

**Note:** datasize is optional parameter but if initialized as 0 we can detect anything, otherwise it is set to the default value.


**Result:** Sucess. Read two sample cards.

**Issue:** Was working with MobaX portable version, but it is creating trouble and is very unstable

**Solution**: Installed MobaX Home edition


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

## autostart.py configured

Extra Commands
```ctrl A N for new window in command page 
ctrl O for new window in command page
ctrl A T to name a window/bash
ctrl A -> or ctrl A <- for moving from one window to another in command page
ctrl C for interrupt in command page
Use cd instead of mc
onboardled.init( Pin.OUT )
onboardled.on()
onboardled.off()
onboardled.on()
dmesg to check if its connected ```

 the id read: f9813ad597
 RC Card reader:
 d("mfrc522","reader",d0,datasize=0)
 
