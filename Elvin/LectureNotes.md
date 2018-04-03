# Table of contents
1. [What does the term home & building automation entail?](#hab)
    1. [Services](#Ser)
    2. [MQTT: M2M Communication](#m2m)
2. [Tutorials](#prac)
3. [Tutorials (review)](#prac)


## What does the term home & building automation entail? <a name="hab"></a>
- Energy efficiency
- Efficiency 
- Security
- Streaming
- Privacy
- Protection
- Networking
- Flexibility
-


### Services: <a name="Ser"></a>
Lighting, Switches, Heating, Physical
Access, Entertainment, HVAC, Traffic
Control/Guidance, Information, Backups, Monitoring,
Remote Access 

Lightning and shading: blinds, Motion detectors, daylighting, switching and dimming. Smart windows.

Security and safety: alarms

### MQTT: M2M Communication <a name="m2m"></a>

## Tutorials: <a name="prac"></a>

19/03/2018
 - cosole serial for via serial connection by the cable connection with the device
 
 
 
22/03/2018
H&B
What does the term entail?

- 

Requirements for Building

MQTT - M2M Communication
--
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
