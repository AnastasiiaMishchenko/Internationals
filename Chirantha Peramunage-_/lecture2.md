
* Lecture 2 22/03/2018

**What is home & building automation?** 

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


**Practical session:First IoT System**

* Resources: https://ulno.net/teaching/iot/iot-makers/ 

* Installed matrix for the common chatroom.

**Commands used to edit password and connection name**
* sudo editor/boot/config.txt 
* sudo reboot

**Steps followed**
* Copy the folder lib/system_templates to a project directory, you can rename system_templates to a project name (i.e. iot-test-project)
* Rename the included node_template to a name for the node you want to configure (i.e. onboard_blinker)

**Difficulties faced:**
* created my folder in the wrong place intially. 
* Didn't know the exact location to copy and move.
* created 2 nodes intially instead of one before even flashing the usb device. So couldn't indetify the exact node for the device. 
* Since the device was not flashed correctly, the command to check which devices are connected (console_serial help) didn't work failing it connect to internet.

**Commands used to reslove:**

* to Quit: ctrl+[ (alt+5)

* to access device: pwd
then cd iot-
cd iot chika/
cd node

* console_serial

* to configure pi: cat("config.py") - but since the flashing has not done yet, this was aborted. 

* Then reconfigure the device without flashing:
pwd
iot-chika
cd node1
initialize - to flash wemos d1 mini. 

**Other useful commands**
ctrl a + k - to kill window
ctrl a + q - to exit all command windows
ctrl alt 6 on the mac!


**Other notes**
* Add more to 'what is H&B'
* first node> pink
* second node> yellow





