``#Portfolio ``
=====================

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

## Introduction <a name="introduction"></a>
* Name: Elvin Alshanov 
* From: Georgia
* BSc: Computer Information Systems (North Cyprus)

### Expectation from H&B Automation <a name="Expectation"></a>
-Want to learn how installing the right wiring, smart control systems, audiovisuals and networking. Ensuring that what’s happening, what’s on the horizon and how to prepare for it to be ready for the future. 
Learn newest technologies, dedicated home theater, smart thermostat, lighting control, motorized shades etc


### Strength and weaknesses <a name="strength"></a>

#### Strength
 -Creativity, Enthusiasm, Honesty

#### Weaknesses
  -Forgetfulness, impatient

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







### *Expectations?*
-




