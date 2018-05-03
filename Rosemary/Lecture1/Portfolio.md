# Table of contents
1. [Introduction](#introduction)
    1. [Expectation from H&B Automation](#Expectation)
    2. [Strength and weaknesses](#strength)
2. [Movie Time](#movie)
3. [New Tools](#git)
4. [Internet of Things (IoT)](#iot)
5. [Practical Sessions](#practicals)
    1. [Installation on Raspberry Pi from Pre-Prepared Image](#pi)
    2. [Make pw-less ssh work on pi](#psw)
    3. [Switch led](#led)
6. [Extras](#extra)
7. [What does the term home & building automation entail?](#hab)
    1. [Services](#Ser)
    2. [MQTT: M2M Communication](#m2m)
8. [Practical](#prac)
9. [Card Reader](#CardReader)
    1. [RFID Connection](#Card)
10. [General Issues & solutions](#issue)
11. [Autostart](#auto)
12. [Plan for Debate](#debat)
13. [Challenges](#challenge)
14. [Extra Commands](#extra)
15. [Debate](#deb)
16. [Installation](#Install)
17. [Tasks:](#task)
18. [Lock](#lock)
19. [Senario for Project 2](#senario)
20. [Shopping list for Project 2](#list)
21. [Challenges](#challenge)
22. [Operate Lock using card reader](#lockcard)

## Introduction <a name="introduction"></a>

Driven by my interest in interdisciplinary programs handling IT, management and technology, I'm pursuing masters in **Energy Informatics**. On completion of this masters I want to be a part of the evolving energy market, as I believe that it is a thriving research area within the IT community. 
I did my bachelor’s degree in **Electronics and Communication** Engineering and then I worked for 3 years in India. Initially I worked in business development, customer interaction and then as Software Tester with emphasis on Automation Testing for 8 months.

### Expectation from H&B Automation <a name="Expectation"></a>
During my bachelor's course, as an extension to my B.Tech mini-project ‘Light controlled digital fan regulator’ I had put forward the possibility of a Smart-room where all the electronics appliances can be controlled centrally and smartly. I hope to realize the same. 

### Strength and weaknesses <a name="strength"></a>

#### Strength
  - Good at drafting documents and communication
  
#### Weaknesses
  - Lack of prior knowledge on the topic

## Movie Time <a name="movie"></a>

#### Scenarios and application domains:
- Controlling Light
- Security and safety
- Privacy
- Energy management and efficiency
- Disaster handling
- Space division 
- Parking
- Intelligent Fridge
- Smart Kitchen
- Manage calls and social media
- Entertainment

#### Technologies:
- Internet
- Sensors
- Holographic displays
- Smart grids
- Camera
- Voice control

#### Feasibility:
Technologies exist but not economical or practical for things like Holographic display 

#### Weirdness/crazyness (any concerns?):
- Privacy and security is a concern
- Public access and vulnarability is possible
- Funny
- Some concepts does not seem worth the effort of automating


## New Tools <a name="git"></a>
- git
- Kanban
- Matrix
- Etcher
- MobaXterm

**Challenge**: A lot of new platforms. Many tabs open and its a mess initially. But slowly getting a hold of it. 

Team members helped each other undertand things better. 

## Internet of Things (IoT) <a name="iot"></a>

[The Internet of things - IoT](https://en.wikipedia.org/wiki/Internet_of_things) is the network of physical devices, vehicles, home appliances and other items embedded with electronics, software, sensors, actuators, and connectivity which enables these objects to connect and exchange data.Each thing is uniquely identifiable through its embedded computing system but is able to inter-operate within the existing Internet infrastructure. 

### Domains (included areas):
- Medical & Healthcare
- Transportation
- Manufacturing
- Energy Management
- Security

### Typical devices (appliance or controller)
- Amazon Dash Button
- Amazon Echo
- Doorbell
- Intelligent lights
- Voice controled devices

## Practical Sessions <a name="practicals"></a>

### 1. Installation on Raspberry Pi from Pre-Prepared Image <a name="pi"></a>

Did installation along with a group member.

Downloaded the pre-prepared Raspberry Pi image & wrote the image to a sd-card with https://etcher.io/ .

Note: Use at least 8GB class-10 sd-card

*Issue Faced*: System not detecting the sd-card even after several trials. 

**Solution**: Used another card-reader and it worked fine.


Challenge: Time consuming 

Changed values: 
- uiot_ap_name: smarthome
- uiot_ap_password: internetofthings123

Put the sd-card into a Raspberry Pi 3 and powered it up. Also connected the LAN cable to it for internet.

Connected my laptop and mobile to this wifi network.

Connect to the ulnoiotgw via ssh ssh -X pi@192.168.12.1 and password ulnoiot. Upgraded it.

Run the command ulnoiot upgrade to make sure that the latest version of ulnoiot is used.

### 2. Make pw-less ssh work on pi <a name="psw"></a>

Did it on a group member's laptop referring to https://www.raspberrypi.org/documentation/remote-access/ssh/passwordless.md.

**Issue Faced**: Should fix a bug in MacOS ssh 

**Solution**: .profile      display     :0

**Alternative Solution**: Just **Restart** the Mac

Tried the same on my Windows laptop but some troubles, so with the help of the lecturer implemented pw-less ssh work on pi.


### 3. Switch led <a name="led"></a>

A group member did it and shared the knowledge. Tried to do the same at home but could not!

**Issue Faced**: Pi wifi not connecting on Laptop, but connecting on phone.


Tried Restart, re-set, troubleshoot etc but it didn't work


## Extras <a name="extra"></a>


#### Some useful Commands learned 


ctrl A H for Help page with more commands


ctrl A Q to quit session


ctrl A K to kill session


sudo editor to edit


sudo poweroff to turn off the Raspberry pi

#### Learned Markdown syntax for creating Git logs


<a href="#top">Back to top</a>

## What does the term home & building automation entail? <a name="hab"></a>
- Automation
- Efficiency 
- Security
- Comfort
- Privacy
- Protection
- Configurability
- Flexibility
- Stability
- Connectivity/Networking
- Integrability


### Services: <a name="Ser"></a>
Lighting, Switches, Heating, Physical
Access, Entertainment, HVAC, Traffic
Control/Guidance, Information, Backups, Monitoring,
Remote Access 

Lightning and shading: blinds, Motion detectors, daylighting, switching and dimming. Smart windows.

Security and safety: alarms

### MQTT: M2M Communication <a name="m2m"></a>

Machine to machine communication  
Can be implemented anywhere, not necessarily in IoT only

Framework for crating network communication. predate of IoT. -Specific channels, msg passing. Subscribe hierarchy. (C# - python program communication)

## Practical: <a name="prac"></a>

Installed matrix for the common chatroom.


**Issue Faced**: Pi wifi not connecting on Laptop, but connecting on phone.

**Solution**: Just remaned the wifi name

Commands used to edit name

sudo editor/boot/config.txt
sudo reboot

**Mistake**: Didn't save commit changes in git. Thus lost the stuffs wriiten during class

### Switch led 
Followed the instructions given in video. No big issues.

### Light turn on/off using Button

Completed the task as a group but yet to figure out how

<a href="#top">Back to top</a>


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


**Result:** Success. Read two sample cards.

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
 

<a href="#top">Back to top</a>


## Installation <a name="Install"></a>

- Chirantha installed **Home Assistance** 
- Elvin installed **openHAB**

## Tasks: <a name="task"></a>
- [x] Lock
- [x] Operate Lock using card reader
- [ ] Operate using openhab
- [ ] Operate using homeassistant
- [x] Create senario for Project 2
- [x] Create shopping list
- [ ] Create Kanbanflow
- [x] Temperature sensor 
- [ ] Incoorporate display


### Lock<a name="lock"></a>
Connected the wemos d1 mini and the lock


Initialised and added the device to node2


**Command:**  Special command to connect the lock to the node
 ``` d("out", "lock", d0, "off", "on") ``` 
``` devices["lock"].evaluate("on") ```


Saved the commands to aurostart.py


**Result:** Success. Lock is opening and closing.


Tried mqtt to combilne card reader and lock
 ```mqtt_action n4/reader anychange xyz mqtt_send n1/lock/set```


**Result:** Failed. Not working
**Note:** 
- Tried different combinations but still not working
- Tried to operate lock using button, but not working
- Asked Mona and Thomas, they said they didn't use mqtt and shared the function for NodeRed

>var idArray= msg.payload.split(" ");
var id = idArray[1];
if(id === "dab93ad58c"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;


**Result:** Failed. Not working


**Issue:**
- Tried different combinations but still not working
- Cannot figure out if the procedure we are following is correct


## Senario for Project 2<a name="senario"></a>

- Group met and came up with a senario 
- I defined the __friend__'s basic details and shared the document 


## Shopping List for Project 2<a name="list"></a>

- I created a shared excel for the shopping list and stated a sample entry so that the group members can contrubute to the same
- Chirantha and Elvin met up to fill in more details to the shopping list

[Click here for Shopping List:](https://docs.google.com/spreadsheets/d/1SVmDE6H7TyPvkSrJAKrBFFbK5skZS80MD8QROaJ6owY/edit#gid=0)
 
 ## Challenges: <a name="challenge"></a>
 - All gropu mates could not meet up to make an exhaustive list
 - Several trials to operate Lock using card reader failed
 - Issues with Elvin's Py
 - Lot of time spend but no worthwhile result to show
 - Tried NodeRed for Led and Button with an idea to replace Led with the lock, but Not working
 
 ## Operate Lock using card reader<a name="lockcard"></a>
 
 Anastesia completed the task using the NodeRed and gave the Knowledge transfer
 

<a href="#top">Back to top</a>
<a href="#top">Back to top</a>




