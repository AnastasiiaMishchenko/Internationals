# Table of contents

1. [Card Reader](#CardReader)
    1. [RFID Connection](#Card)
2. [General Issues & solutions](#issue)
3. [Autostart](#auto)
4. [Plan for Debate](#debat)
5. [Challenges](#challenge)
6. [Extra Commands](#extra)
7. [Debate](#deb)

 
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

Everybody should use Home Automation. True or False?

- Collected points from different sources
- Did team discussion
- Shared discussed points in Matrix
- Chika created tasks in Kanbanflow for Debate plans
- Researched and prepared personal statements for 3 mins long
- Team met again 
- Did mock debate
- Did actual debate recording
- Researched and prepared personal statements for 5 mins long


> "Home automation" refers specifically to things in your home that can be programmed to function automatically. In the past years, those automations were pretty basic, like the lamp timers, programmable thermostats and so on. But that's being changing with big and small companies foreseeing the future and coming up with a variety of devices aimed at mainstream consumers.

>Shop around, and you'll find gadgets designed to help you sleep better, self-making bed, smart shower, smart home piggy bank, devices that smarten up your home entertainment system and even connected tools for more intelligent gardening. For elderly ppl north California. The possibilities are immense, and even controlling these devices have option like voice control, gesture detection, touch, smartphones, apps etc.

>If all these sounds expensive, a new roof to avoid heat or a central AC unit will cost even more, its not that outrageous. So you just have to decide if you are comfortable with a home that listens.. so you don’t waste your money.. 
And also, in the past three years, Its seen that the prices of IoT device is coming down as the competition and the demand is increasing. With big names like Apple, Amazon, Google, GE and Microsoft, there is so much competition in the market and manufacturers are getting increasingly creative in order to stand out from the crowd, which is one of the main reasons that the smart home has diversified as quickly as it has. The market experts predict that the smart home's market share will be worth tens of billions within the next few years.

>If you're a little uncertain about taking a big leap towards home automation, there are plenty of smart, affordable entry points that offer surprisingly high levels of functionality, making it easy to experiment and figure out what you want from your connected home. It's a low-risk way to dip your foot into smart home waters, and if you like it, finding compatible gadgets that make it even smarter isn't difficult at all.

>Also, Smart hubs are designed to control multiple devices, even ones from different manufacturers. This gives a centralization and integration. A good hub can integrate every smart thing in your home into a single, seamless home automation experience, and offer consolidated controls within a single app.
In general, smart home manufacturers see the value in keeping things somewhat open, and many go out of their way to embrace third-party hubs and smart home platforms as a means of providing compatibility with other gadgets. This means that you've got a lot of options. And a variety to choose from, each compatible with one another. 

>A recent study by Intel shows that we are on the brink of a smart-home boon, with growing number of consumers. And we are expecting to see at least one smart-home device in every home by 2025. I think it is the future, and I’m confident that smart homes would become as common as smartphones within the next decade and its not wise to oppose this inevitable change.
 
