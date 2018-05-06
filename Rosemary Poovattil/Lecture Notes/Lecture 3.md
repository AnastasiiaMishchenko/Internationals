# Table of contents

1. [NFC Card Reader](#CardReader)
    1. [RFID Connection](#Card)
2. [General Issues & solutions](#issue)
3. [Autostart](#auto)
4. [Plan for Debate](#debat)
5. [Challenges](#challenge)
6. [Extra Commands](#extra)
7. [Debate](#deb)

 
## NFC Card Reader <a name="CardReader"></a>

### RFID Connection<a name="Card"></a>
Connected the wemos d1 mini and the rfid-rc522 board as follows:

- 3v3 - 3.3V
- d8  - sda
- d7  - MOSI
- d6  - MISO
- d5  - SCK
- d0  - RST
- G   - GND

Initialised the device to node3


**Command:**  Special command to connect the device RC522(The card reader) to the node
 ``` d("mfrc522","reader",d0, datasize=0) ```
``` r=d("mfrc522","r",d0) ```

**Note:** datasize is optional parameter but if initialized as 0 we can detect anything, otherwise it is set to the default value.


**Result:** Success. Read two sample cards.

The id value read: f9813ad597

## General Issues & solutions<a name="issue"></a>

**Issue 1**:The Pi not getting powered up 


**Solution**: upgraded and reinitialize Pi


**Mystery** : Chirantha did upgrades & it showed message saying upgraded but no trace of that upgrade was listed when the professor checked!


**Issue 2:** Was working with MobaX portable version, but it is creating trouble and is very unstable

**Solution**: Installed MobaX Home edition


**Issue:** When two devices connected in series with the Pi, cannot identify which device is being detected by the Pi

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


**Knowledge transfer:** Coveyed the tasks completed to Elvin and Chirantha and helped them to do the same by staying back after the class


## Plan for Debate<a name="debate"></a>
Planned to meet up and discuss individual points on debate. </b>
**work:** Find points for and aganist the motion for debate
 
 ## Challenges: <a name="challenge"></a>
 - The gropu mates were absent for half of the class. 
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

**Topic: Everybody should use Home Automation. True or False?

- Collected points from different sources
- Did team discussion
- Shared discussed points in Matrix
- Chika created tasks in Kanbanflow for Debate plans
- Researched and prepared personal statements for 3 mins long
- Team met again 
- Did mock debate
- Did actual debate recording
- Researched and prepared personal statements for 5 mins long

[Personal Statement](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Lecture%20Notes/Debate_PersonalStatement.md)

[Rehersal Video](https://www.youtube.com/watch?v=1JOWhVgcfnY&feature=youtu.be)

