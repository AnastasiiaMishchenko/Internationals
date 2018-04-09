

* Lecture 4 03/04/2018

# Table of contents
1. [Home Assistant](#Home_Assistant)
2. [Practical Session: Smart lock](#Practical_Session_Smart_Lock)
3. [NodeRed](#NodeRed)
4. [Additional Commands used](#NodeRed)
5. [Debate](#Debate)
6. [Protocols](#Protocols)
7. [Afterwork/ Problems faced](#Afterwork_and_Problems_Faced)

**1. Home Assistant** <a name= "Extra_Commands"></a>

Install 'Home Assistant', login :  hass --open-ui 
Link to download: https://www.home-assistant.io/docs/installation/macos/
Installation guide: https://www.youtube.com/watch?v=hej6ipN86ls

* Issues faced - the final command to login wasn't working on the same terminal. 
* error - hass: command not found
* Workaround - open new terminal and run the same command again. (found it in a youtube video comment). 
* login :  hass --open-ui 

**2. Practical Session: Smart lock** <a name= "Practical_Session_Smart_Lock"></a>

In the meantime tried the smart lock using below code. Saved the codes on autostart.py
A group member did it mostly while I was initializing home assistant and later shared the knowledge. 

* Commands 

```
run()

devices
devices["lock"]
devices["lock"].evaluate("on")
devices["lock"].evaluate("off")
wemos d1 mini - rfid-rc522 board

```

- 3v3 - 3.3V
- d8  - sda
- d7  - MOSI
- d6  - MISO
- d5  - SCK
- d0  - RST
- G   - GND

* Add device with: r=d("mfrc522","r",d0)

* Write data to a mifare classic card: r.write("mydata to write to reader")

* import ulno_iot_relay as relay relay.right() relay.left()

* d("out", "lock", d0, "off", "on") run()

* devices 
* devices["lock"] devices["lock"].evaluate("on") 
* devices["lock"].evaluate("off")

* mqtt_all 
* mqtt_action n4/reader anychange xyz mqtt_send n1/lock/set

* d("led","blue",onboardled, "off", "on") b1= d("button", "b1", d3, "off", "on") 
* mqtt_action n2/b1 anychange xyz mqtt_send n1/blue/set on

**3. NodeRed** <a name= "NodeRed"></a>

* Tried the function in of NodeRED toggle:

```
var idArray= msg.payload.split(" ");

var id = idArray[1];

if(id === "dab93ad58c"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;
```

**4. Additional Commands used** <a name= "Extra_Commands"></a>

* Ignore the 'shell already in use' command. - esc, exit from console, retry.

* ctrl A K to kill the window. 
* ctrl A Q to quit all windows
* ssh -X pi@ulnoiotgw - to login

**5. Debate** <a name= "Debate"></a>

Participated the debate representing pro team. 

**Major points collected and presented:**

1.	Safety. 

The ability to control small appliances and lighting with your fingertips anywhere you are will add safety in your home.  You can make sure appliances are off when its needed to be off and on when its needed to be on.

2.	Security.  

The ability to lock the door through your phone is one of the greatest benefits of home automation.  This will give you peace of mind knowing that the door is close and not guessing.   The fact that you can be alerted each time someone enters your home also allows you to monitor who is entering your home at all times, especially when you are not there.

3.	Convenience.  

The ability to control everything with your fingertips is very convenient.  You never leave the house without your wallet, keys and your smart phone.  With our smart phone always with us, we can easily monitor our home and control everything with just touch of a fingertip.

4. Energy Saving

The Increased energy efficiency is one of the relevant advantage of home automation. Depending on how we use our smart-home technology, it’s possible to make our space more energy-efficient. For example, you can have more precise control over the heating and cooling of your home with a programmable smart thermostat that learns your schedule and temperature preferences, and then suggests the best energy efficient settings throughout the day. Lights and motorized shades can be programed to switch to an evening mode as the sun sets, or lights can turn on and off automatically when you enter or leave the room, so you never have to worry about wasting energy.


**6. Protocols** <a name= "Protocols"></a>

*	Zigbee – coordinator, router, end device, 2 years of battery life, low power, low bandwidth needs. Small scale wireless projects. The Hue. 
*	Zwave- Less energy than wifi, provide a reliable, low latency transmission of small data packets. 
*	RS – 232 – defines communication between data terminal equipment, computer terminal, replaced by usb, used in industrial machines, scientific gear. 
*	RS-422 – applications early macintosh, no protocol definition. Only defines voltage levels. 
*	SPI – shared clock, master slave acritechture. Single way transmission. Used for embedded systems. Ex: semnsors, camera lenses, card readers,
*	I2C – serial half duplex, master slave relationship, only 2 bus lines required. Ex: systems management bus, power mgmt. bus, display data channel. (Low active- one curve, one voltage. Devices of different voltages can be connected along.) 10 bit address- 1024 devices. Raspberry displays. 
*	KNX – bus: OSI protocol, independent of platform, usage: alarm monitoring, energy monitoring speed 9600 bits/s, address scheme(how many devices) – 65000 – on one segments* 4 segements
*	Ebus – used in heating and solar appliances, 2 wire digital serial bus communication, master slave, length >100, 2400 baud symbol rate – speed.
*	Canbus – mostly used in vehicles, multiplex electric wiring in automotives – to save copper, 50kbits/s ,1000m, multi master serial bus architecture, all nodes are connected to each other through 2 wire bus. Twisted pair wires. High config flexibility, most common bus structure for automotives. 
*	Modbus – serial communication protocol, use its own PLC, very flexible – easy to deploy, maintain, openly published, licence free, simple to measure temperature, used in SCADA systems. (ex: Smart grids). Master slave communication, versions – serial, Ethernet. Unique address. 
* X10 - communication among electronic devices used for home automation. Since 1975
Speed: Slow, 0.75s to transmit a device address and a command.
Throughput: 3000 bits per second.
Latency: 60 Hz wave with a maximum delay of 100 microseconds. (TW523). 
Length: 310MHz in U.S.  & 433.92 MHz on European systems. 
Flexibility: Option to upgrade. X10 modules only react to commands, they do not transmit back a status, which limits flexibility. 
Importance: 
Advantages: Cheap, Availability
Disadvantages: poor performance (can only transmit one command at a time), distance limitations, less reliability, power phase limitations, Lack of encryption.
Usage examples: mostly hybrid systems nowadays along with Zigbee, Z-wave protocols. 
Examples: X10 Lamp dimmer module, X10 in Wall dimmer Switch. X10 appliance module can be used to monitor doors & windows as well. 
* OneWire -is a device communications bus system. 
Speed: communicated at a speed of up to 16.3kbps, which is now called "standard speed." To reduce the time needed to read a 64Kbit memory iButton to less than 1 second, a high-speed mode called "overdrive"
Flexibility:  1-wire slave and I2C master operational modes. Supports 15 kbps and 77 kbps 1-wire protocol with packetized I2C data payloads
Advantages of 1-wire interface: Multiple slaves are accessed using only 2-wires in this interface type. Due to use of less wires, the interface is cheaper. It is easy to implement the interface. The interface supports longer distance (about 300 meters)
Disadvantages of 1-wire interface: It is implemented both in the hardware as well as software. The synchronization of data at the receiver has to be taken care in software which is a complex task. Though the interface supports longer distance, it is limited due to noise and cable capacitance. It supports slower speed of communication. 1-wire slave devices are manufactured by Dallas semiconductor only.


**7. Afterwork/ Problems faced** <a name= "Afterwork_and_Problems_Faced"></a>

* suggestions for the scenario project, family members a name, why they want home automation, cost estimation (amazon, ali express)
* get lock working in openhub or homeassitant, and card reader. Also nodered. 

* Tried log in to ELvin's Pi : password - ulnoiot
* Get's the same error that Elvin gets when adding a new device. Tried several times but no success. 
* tried the initializing from another sd card on Elvin's pi and now it's working as expected.	
* when trying simple commands like 'mc' or 'console', the bash freezes most of the time hence had to kill that window and start again. (Sometimes that even doesn't work). (Lot of rework)
* Suggestion recieved after submitting the question - do not frequently use ctrl O to shift from mc window to bash. 
* Couldn't complete setting up a link between the working card reader and the lock using shell commands. 

