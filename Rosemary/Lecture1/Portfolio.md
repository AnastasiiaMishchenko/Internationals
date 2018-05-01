# Table of contents
1. [Introduction](#introduction)
    1. [Expectation from H&B Automation](#Expectation)
    2. [Strength and weaknesses](#strength)
2. [Movie Time](#movie)
3. [New Tools](#git)
4. [Internet of Things (IoT)](#iot)
5. [Practical Sessions](practicals)
    1. [Installation on Raspberry Pi from Pre-Prepared Image](#pi)
    2. [Make pw-less ssh work on pi](#psw)
    3. [Switch led](#led)
6. [Extras](#extra)
7. [What does the term home & building automation entail?](#hab)
    1. [Services](#Ser)
    2. [MQTT: M2M Communication](#m2m)
8. [Practical](#prac)

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




