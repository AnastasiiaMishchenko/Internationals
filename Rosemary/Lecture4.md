

tried 

import ulno_iot_relay as relay
relay.right()
relay.left()
but not working
asked mona and thomas
</a>

d("out", "lock", d0, "off", "on")
run()

devices
devices["lock"]
devices["lock"].evaluate("on")
devices["lock"].evaluate("off")

in the function in of NodeRED:

var idArray= msg.payload.split(" ");

var id = idArray[1];

if(id === "dab93ad58c"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;

mqtt_all
mqtt_action n4/reader anychange xyz mqtt_send n1/lock/set

d("led","blue",onboardled, "off", "on")
 b1= d("button", "b1", d3, "off", "on")
mqtt_action n2/b1 anychange xyz mqtt_send n1/blue/set on


# Table of contents

1. [Installation](#Install)
2. [Tasks:](#task)
3. [Autostart](#auto)
4. [Plan for Debate](#debat)
5. [Challenges](#challenge)
6. [Extra Commands](#extra)
7. [Debate](#deb)

 
## Installation <a name="Install"></a>

- Chirantha installed **Home Assistance** 
- Elvin installed **openHAB**

## Tasks: <a name="task"></a>
- [x] Lock
- [ ] Operate Lock using card reader
- [ ] Operate using openhab
- [ ] Operate using homeassistant
- [x] Create senario for Project 2
- [x] Create shopping list
- [ ] Create Kanbanflow
- [ ] Temperature sensor 
- [ ] Incoorporate display

display and temperature sensor

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

The id value read: f9813ad597

## General Issues & solutions<a name="issue"></a>

**Issue:** Was working with MobaX portable version, but it is creating trouble and is very unstable

**Solution**: Installed MobaX Home edition


**Issue:** When two devices connected in series with the Py, cannot identify which device is being detected by the Py

**Solution**: The help gave the following solution:


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



**Result:** Tried initialize usb1 
But this didn't work as explained in help!


## autostart.py configured<a name="auto"></a>

Watched video for autostart.py and tried it in nodes.

**Result:** working 


## Plan for Debate<a name="debate"></a>
Planned to meet up and discuss individual points on debate. </b>
**work:** Find points for and aganist the motion for debate
 
 ## Challenges: <a name="challenge"></a>
 - The gropu mates were absent for half of the class. 
 - There is a communication gap with Anastasiia and the rest of the team, thus no knowledge transfer happens from that side. 
 - A lot of time spend on solving issues
 - Staying back, working at home etc is not very helpful as getting stuck at somepoint and feel so out of resources 
 - Very time consuming task as each step involves a lot of research
 
 ## Extra Commands<a name="extra"></a>
- ```ctrl A N``` for new window in command page 
- ```ctrl O``` to navigate from one window to next
- ```ctrl A T``` to name a window/bash
- ```ctrl A -> or ctrl A <-``` for moving from one window to another in command page
- ```ctrl C``` for interrupt in command page
- Use cd instead of mc
- ```onboardled.init( Pin.OUT ```) this can be used to identify which node the device belongs to
- ```onboardled.on()```
- ```onboardled.off()```
- ```dmesg``` to check the devices connected 

## Debate<a name="deb"></a>

