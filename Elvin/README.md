``#Portfolio ``
=====================

![iot](https://d3uifzcxlzuvqz.cloudfront.net/images/stories/content/handbooks/iot-technologies/connectivity-diagram.jpg)
# Table of contents
1. [Introduction](#introduction)
    1. [Expectation from H&B Automation](#Expectation)
    2. [Strength and weaknesses](#strength)
2. [Movie Time](#movie)
3. [New Tools](#git)
4. [Internet of Things (IoT)](#iot)
5. [Extras](#extra)
6. [Knx-Certifcate](#knx)

7. [What does the term home & building automation entail?](#hab)
    1. [Services](#Ser)
    2. [Tutorials](#prac)
8. [Tutorials (review)](#prac)
9. [Debate](#deb)
10. [openHAB2](#hab)


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
- Internet / Industrial Internet
- Wearables
- Sensors
- Connected Cars
- Holographic displays
- Smart grids
- Camera
- Voice control
- IoT in agriculture

#### Feasibility:
Technologies exist but not economical or practical for things like Holographic display 

#### Weirdness/crazyness (any concerns?):
- Privacy and security is a concern
- Public access and vulnarability is possible
- Funny
- Some concepts does not seem worth the effort of automating


## New Tools <a name="git"></a>
- Etcher
- MobaXterm
- Git
- Kanban
- Matrix
- HomeAssistance


**Challenge**: A lot of new platforms. Many tabs open and its a mess initially. But slowly getting a hold of it. 

Team members helped each other undertand things better. 

## Internet of Things (IoT) <a name="iot"></a>

 An IOT Device can be anything connected to the internet for example a coffee maker or a fridge or even a temperature logger which uploads data to internet
It's not only about technology solution, but to sell it as an enabler for a smart way of living.
Home Automation , is automating the iot devices and lights ( majorly) , so that they make your life easier , a home automation hub can make your iot coffee maker start before your alarm rings and turn up the lights as soon as you wake up , that's Automation
 

### Domains (included areas):
- Healthcare - Monitor hand hygiene compliance through IOT device and sensors to reduce transmission of Hospital Acquired Infections to patients.
- Transport and logistics - Monitoring the logistics vehicles health to send alerts.
- Retail - Remote interaction with products increase personalized shopping experience.
- Insurance - Tracking clients' activity and offer discounts or rewards for healthy and safe behavior.
- Banking - Smart payments.
- Space - MARS Rover.
- Construction and Real Estate - Smart home devices/locks/camera/security.
- Farming - Tracking soil health and climate.
- Industrial internet - Smart Fleet management and more sensors/data in Aircraft to avoid failures.
- Wearables - Health monitoring and Fitness tracking.
- Security

### Typical devices (appliance or controller)
- Doorbell
- Intelligent lights
- Voice controled devices
- Google Home Mini: Smart speaker. Google Home Mini is the smaller version of the Google Home
- Amazon Echo Spot: Smart alarm clock. 
- Amazon Echo: 2nd generation
- Nest Thermostat
- August: Smart Lock 3rd generation
- HomePod: Smart speaker with Siri
- Amazon Echo Show: Alexa with a screen
- Amazon Echo Look: Alexa powered camera.
- Amazon Dash Button
- Amazon Echo



#### Useful commands

ctrl A T to rename

ctrl A N new bash

ctrl A H for Help page with more commands


ctrl A Q to quit session


ctrl A K to kill session


sudo editor to edit

sudo poweroff to turnoff pi

---

[Source - ulnoiot](https://github.com/ulno/ulnoiot)

[Source - analyticsvidhya.com](https://www.analyticsvidhya.com/blog/2016/08/10-youtube-videos-explaining-the-real-world-applications-of-internet-of-things-iot/)

[Source - wikipedia.org](https://en.wikipedia.org/wiki/Internet_of_things)

--
## KNX Certifcate <a name=knx> </a>

![iot](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Elvin/Images/Knx.PNG)

---










## What does the term home & building automation entail? <a name="hab"></a>
- Energy efficiency
- Efficiency 
- Security
- Streaming
- Privacy
- Protection
- Networking
- Flexibility


### Services: <a name="Ser"></a>
Lighting, Switches, Heating, Physical
Access, Entertainment, HVAC, Traffic
Control/Guidance, Information, Backups, Monitoring,
Remote Access 

Lightning and shading: blinds, Motion detectors, daylighting, switching and dimming. Smart windows.

Security and safety: alarms


## Tutorials: <a name="prac"></a>


### 1. Installation on Raspberry Pi<a name="pi"></a>

Downloaded the pre-prepared Raspberry Pi image & wrote the image to a sd-card with https://etcher.io/ .

Note: Use at least 8GB class-10 sd-card (16GB)

Challenge: Time consuming 

Changed values: 
- uiot_ap_name: eni313
- uiot_ap_password: internetofthings123

First laptop didn't find wifi and connected mobile to this wifi network.

Connect to the ulnoiotgw via ssh ssh -X pi@192.168.12.1 and password ulnoiot.

command ulnoiot upgrade to make sure that the latest version of ulnoiot is used.



19/03/2018
 - cosole serial for via serial connection by the cable connection with the device
 
 
 #UlnoIoT tutorial 2 - Switching A Light
I had troubles while connecting to laptop slot, used another power supplier solved problem.
When I had problem while connecting via console I used serial connection to connect with device.
   console_serial
Use on/off command of the onboardled command
 Test light: onboardled.init(Pin.OUT)
              onboardled.on()
              onboardled.off()
 
#UlnoIoT tutorial 3 - SLed Romote Button
       Go to node one -  cd iot-system-ulno/node1/
       Endup with the device - console
       the command which will use- d("led", "yellow", d7, "turn on", "turn off")
       checking device - devices
       using device["blue"].evaluate("off")/("on")
       then run command - run()
     It listenins commands via network by using protocol mqtt
     
     use help("button") command to see available commands
        b1 = d("button", "b1", d3, "off", "on")
     
        b1.updated_value()
            run()
        mqtt_all - to see both nodes
        mqtt_action - get help (Another uhelp led)
        mqtt_action node2/b1 anychange xyz
        mqtt_send node1/blue/set on
        mqtt_send node1/blue/set off
        mqtt_action node2/b1 anychange xyz mqtt_send node1/blue/set

## Tutorials: (review)<a name="prac"></a>
4/3/2018
Started from tutorial 2
ctr+a+t (rename)
checking correct device : dmesg
worked with: console_serial
checked to see comands by typing : dir()
switched light : onboardled.init(Pin.OUT)
light off: onboardled.on() / onboardled.off()

----------------------------
tutorial 3 - Led Remote Button
initalizes node 2 and connected node one also
node1
	d("led", "blue", onboardled, "off", "on")
   check: devices
   devices["blue"].evaluate("on") /("off)
constantly listen: run()

node2 
	help("button")
	b1 = d("button", "b1", d3, "off", "on")
	b1.
	b1. (tab to check commands)
	b1.updated_value()
	run()
new command line
	        mqtt_  (-bash: mqtt_: commant not found)
    but mqtt_all worked
	mqtt_action  (uhelp for more commands)
	mqtt_send node2/b1 anychange xyz
	mqtt_send node1/blue/set on/off (through gateway)
	mqtt_action node2/b1 anychange xyz mqtt_send node1/blue/set

-----------------------------------------------------------------------
IoT Hello World with Node-RED
	http://192.168.12.1:1880
	add: mqqt in/out and debug(msg.payload)

	javascript function block:
		if(msg.payload === "on")
{
 
  	 if(context.togglestate === "on")
   
 	{
    context.togglestate = "off";
    }
  
 	 else{
        context.togglestate ="on";
   
	 }
}
msg.payload = context.togglestate;
return msg;

------------------------------------------------------------------------
card reader
		sudo su -
		apt-cache search libnfc
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python-dev
git clone https://github.com/lthiery/SPI-Py.git
ls
cd SPI-Py/
sudo nano spi.c
ctr+w 
.cs_change <enter>
sudo python setup.py install
git clone https://github.com/mxgxw/MFRC522-python.git

cd MFRC522-python/
sudo python Read.py

------------------------------------------------------------------------
SmartLock

initialized node3
 code: d("out", "lock", d0, "off", "on")
run()

devices
devices["lock"]
devices["lock"].evaluate("on")
devices["lock"].evaluate("off")

code for Function in NodeRED:

var idArray= msg.payload.split(" ");

var id = idArray[1];

if(id === "dab93ad58c"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;

---------------------------------------------------------------------------
Card Reader


 I upgraded (ulnoiot upgrade, update wemos also)  and pi was connected to the internet, still getting same error.

  d("mfrc522","reader",d0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "uiot/_mgr.py", line 51, in d
  File "<string>", line 1, in <module>
ImportError: no module named 'uiot.mfrc522

"mfrc522" works when I test with my team mates pi.
copied and initialized another node, still could not solved

Suggestion from professor worked: Try your team mates sd-card in your pi and initialize from there. 

----------------------------------------------------------------------------

## Debate:<a name="deb"></a>

> The first and most obvious benefit to smart homes is convenience, as more connected devices can handle more operations (lighting, temperature, etc.) and frees up the resident to perform other tasks. Imagine that you're driving home on a hot summer day. But rather than turn the air conditioner on when you get home and wait for your house to cool, you simply use your smart-phone when you leave your office to tell your smart thermostat to lower the temperature.

* 1. Managing all of your home devices from one place. The convenience factor here is enormous. Being able to keep all of the technology in your home connected through one interface is a massive step forward for technology and home management. Theoretically, all you’ll have to do is learn how to use one app on your smart phone and tablet, and you’ll be able to tap into countless functions and devices throughout your home. --This cuts way back on the learning curve for new users, makes it easier to access the functionality you truly want for your home
* 2. Flexibility for new devices and appliances. Smart home systems tend to be wonderfully flexible when it comes to the accommodation of new devices and appliances and other technology. No matter how state-of-the-art your appliances seem today, there will be newer, more impressive models developed as time goes on. Beyond that, you’ll probably add to your suite of devices as you replace the older ones or discover new technology to accompany your indoor and outdoor spaces. Being able to integrate these newcomers seamlessly will make your job as a homeowner much easier, and allow you to keep upgrading to the latest lifestyle technology.
* 3. Maximizing home security. When you incorporate security and surveillance features in your smart home network, your home security can skyrocket. There are tons of options here -- only a few dozen of which are currently being explored. For example, home automation systems can connect motion detectors, surveillance cameras, automated door locks, and other tangible security measures throughout your home so you can activate them from one mobile device before heading to bed. You can also choose to receive security alerts on your various devices depending on the time of day an alert goes off, and monitor activities in real-time whether you’re in the house or halfway around the globe.

--------------------------------------------------------------------------------------------------------------------

## [openHAB2](#hab)

* Installation

- Choose between the Stable Version Download or the latest Snapshot Version Download of openHAB.

- Unzip the file in your chosen directory (e.g. C:\openHAB2)
- Start the server: Launch the runtime by executing the script C:\openHAB2\start.bat and wait a while for it to start and complete.
- Point your browser to http://localhost:8080. You should be looking at the openHAB package selection page. When you’ve selected an appropriate package, this page will contain the UI selection screen

* Backup

- Make sure that you make regular backups of the conf and userdata folders, you can zip and unzip these folders too and from openHAB installations

* Updating the openHAB Runtime
- There is currently no automatic update script for Windows. To update manually, download a later version of the openHAB distribution zip file and follow these steps:

- Stop the openHAB process if it is currently running.

- Backup openHAB as described above.

Delete the following files and folders from your existing install:

	userdata\etc\all.policy
	userdata\etc\branding.properties
	userdata\etc\branding-ssh.properties
	userdata\etc\config.properties
	userdata\etc\custom.properties
	userdata\etc\distribution.info
	userdata\etc\jre.properties
	userdata\etc\org.ops4j.pax.url.mvn.cfg
	userdata\etc\profile.cfg
	userdata\etc\startup.properties
	userdata\etc\version.properties
	userdata\etc\system.properties
	userdata\etc\custom.system.properties
	Any file in userdata\etc that starts with org.apache.karaf
	The userdata\cache folder
	The userdata\tmp folder
	The runtime folder
	
- Copy and paste the contents of the zip file over your existing install, when prompted do not overwrite existing files

* Starting openHAB as a Service

- By installing the openHAB process as a service in Windows, you can:
- Launch it automatically upon system startup
- Run it in the background

----------------------------------------------------------------------------------------------------------------------

* 4/10/2018

- Task plips lamb, program pi interntet as a output, and give it as wifi

[KNX lecture](#knx)
	
- [source knx](https://my.knx.org/)
	
- [source kodi](https://kodi.tv/)

- Mqtty simulator (build device you don't have 
	example: automation, temprature going up-down simiulator
	
## [KNX lecture](#knx) Basically, a KNX system requires the following components:

Power Supply for the power of the installation
Sensors (push buttons, thermostats, air speed meters etc.) that generate commands as telegrams
Actuators (switch relays for lights, blinds etc.) that receive the telegrams and perform certain actions
The BUS that connects all Sensors and Actuators

#### After the installation has been successfully completed, we need to import a catalog with the device informations, before we can actually start with our first project. Have a look at the video how to handle this task in ETS5.


------------------------------------------------------------------------------------------------------------------

Downloaded installed Kodi
	- Got error bad image: 
	
	msvcp140.dll is either not designed to run on windows or it contains an error kodi
Solution: 
	
	type SFC /scannow and press enter
	once its finished, copy paste this command in and press enter:
	DISM /Online /Cleanup-Image /RestoreHealth
€
------------------------------------------------------------------------------------------------------------------

1) Motion (distance)
2) RGB Light
3) Voice input (Android, if ttt, ddufrut)
4) Voice output (triggered via mqtt)

------------------------------------------------------------------------------------------------------------------

4/17/2018

#Presentation - Mc Guys

	Their scenario is about automation of a house of a Teacher, which is getting handy when teacher lady in a hurry she can check 	 her fridge during her break in school and make online grossery shopping and check heating also from application.
 	- Central Control Unit Panel (7 displays)
	- Heating & Climate - Functionalities (Automate teprature control, Hommatic Wireless Room Thermostat, window Drive Winmatric,  Temprature/Humidity Sonseor, Rain Sensor (close window automatically), Total- 10430€)
	- Lighting & Shutter Device (Philips Hue LED Struana, Beyond) 
 
#Presentation - Ricky sMMART-home

	- No Alarm
	- Motion Sensor Tree (51 pc)
	- Touch Pure Tree (45 pc)
	- no alarm
	- wiring 
	- 13h x 90 euro= 1.170euro
	- total installation 20 thousand
	- interconnections: Overview (Miniserver="Gateway" , Canban bus, 
	- Components 110,684.91
	- Configuration 20,340.00
	- SUM 131,024.91

	rocomendation - Smart cooking devices, coffee making, b	eer 

---------------------------------------------------------------------------

- no alarm
- wiring 
- 13h x 90 euro= 1.170euro
- total installation 20 thousand
- interconnections: Overview (Miniserver="Gateway" , Canban bus, 
- Components 110,684.91
- Configuration 20,340.00
- SUM 131,024.91

rocomendation - Smart cooking devices, coffee making, beer 


Midnight snack-

Paul wakes up during night and feels hungry and want to eat something so he needs
 just enough light to make your way to the refrigerator and back without disturbing family members.

Task-- KODI
connection problem (checked firewall, public/private network setting)
solution: Installed Apple bonjour services and turned on discovery from the kodi/settings
install kodi app get connection, control main kodi application from the phone. 
then install nod-red package for kodi
--
  installed kodi nod-red package and connected using IP address login and password


