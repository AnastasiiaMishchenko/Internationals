
<a name= "top"></a>

* Lecture 2 22/03/2018

# Table of contents
1. [Introduction](#Introduction)
2. [Practical Session](#Practical_Session)
3. [Difficulties Faced](#Difficulties_Faced)
4. [Useful Commmands](#Useful_Commmands)
5. [Notes](#Notes)


**What is home & building automation?** <a name= "Introduction"></a>

Automation of household activities by providing advanced functionalities to the control systems of the building. 
Ex services: Lightning system, security and access. Voice control. Entertainment. 

**purposes:** Convinenece, multitasking, energy efficiency,flexibility, Security. 

**Heating, ventilation, Air conditioning:** Supply and remove heat, Ventilation(Free or mechanical), Humidify,/ dehumidify  (Clean/ filter)
centralised, decentralised handling. 

**Lightning and shading:** blinds, Motion detectors, daylighting, switching and dimming. Smart windows.

**Security and safety:** alarms

**MQTT: M2M Communication** 
- Framework for crating network communication. predate of IoT. 
-Specific channels, msg passing. Subscribe hierarchy. (C# - python program communication)

[Move to top](#top)

**Practical session:First IoT System** <a name= "Practical_Session"></a>

* Connect a microcontroller which was initialized before, directly to the laptop.
* Use a command console to enter the microcontroller.
* d("led", "green", onboardled, "off", "on") - initialize the onboard led.
* devices["green"].evaluate("off") and devices["green"].evaluate("on") - turn off/on the led. Activate the device with run() command.
* Connect a second micro controller directly to the Raspberry Pi and initialized it.
* Use a command console_serial to enter the micro controller. 
* Create a variable b1 = d("button", "b1", d3, "off", "on") and b1.updated_value() to see the changes while pressing the button. Activate the device with run() command.
* mqtt_send onboard_blinker_2/green/set on and mqtt_send onboard_blinker_2/green/set off will send the request over the gateway to the led in onboard_blinker_2 directory.
* mqtt_action onboard_blinker/b1 anychange abc mqtt_send onboard_blinker_2/green/set will send the switch on/off request over the gateway to the led in onboard_blinker_2 directory when the button from the onboard_blinker directory is pressed.
* sudo poweroff shut down the Raspberry Pi.
* After performing the commands manually, the autostart.py files of both microcontrollers were modified. 

##### For the microcontroller which performs on and off of the led, the following lines were added.

* d("led", "green", onboardled, "off", "on")
* devices["green"].evaluate("off")
* devices["green"].evaluate("on")
* run(10)

##### For the microcontroller which performs the button clicks, the following lines were added.

* b1 = d("button", "b1", d3, "off", "on")
* b1.updated_value()
* run(10)

* Resources: https://ulno.net/teaching/iot/iot-makers/ 
* https://www.youtube.com/watch?v=Yzys-EiLPsk&feature=youtu.be

* Installed matrix for the common chatroom.

**Commands used to edit password and connection name**
* sudo editor/boot/config.txt 
* sudo reboot

**Steps followed**
* Copy the folder lib/system_templates to a project directory, you can rename system_templates to a project name (i.e. iot-test-project)
* Rename the included node_template to a name for the node you want to configure (i.e. onboard_blinker)

[Move to top](#top)

**Difficulties faced:** <a name= "Difficulties_Faced"></a>

* created my folder in the wrong place intially. 
* Didn't know the exact location to copy and move.
* created 2 nodes intially instead of one before even flashing the usb device. So couldn't indetify the exact node for the device. 
* Since the device was not flashed correctly, the command to check which devices are connected (console_serial help) didn't work failing it connect to internet.

**Commands used to reslove:** <a name= "Useful_Commmands"></a>

* to Quit: ctrl+[ (alt+5)

* to access device: pwd
* then cd iot-
* cd iot chika/
* cd node

* console_serial

* to configure pi: cat("config.py") - but since the flashing has not done yet, this was aborted. 

* Then reconfigure the device without flashing:
* pwd
* iot-chika
* cd node1
* initialize - to flash wemos d1 mini. 

[Move to top](#top)

**Other useful commands**
* ctrl a + k - to kill window
* ctrl a + q - to exit all command windows
* ctrl alt 6 on the mac!


**Other notes** <a name= "Notes"></a>

* Add more to 'what is H&B'
* first node> pink
* second node> yellow
* add daily reflection, table of content, more difficulties faced regarding day 1



[Move to top](#top)

