[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)

# Table of contents

1. [Installation](#Install)
2. [Tasks:](#task)
3. [Lock](#lock)
4. [Protocols and buses](#proto) 
5. [Senario for Project 2](#senario)
6. [Shopping list for Project 2](#list)
7. [Challenges](#challenge)
8. [Operate Lock using card reader](#lockcard)

 
## Installation <a name="Install"></a>

- Me and Chirantha installed **Home Assistance** 
- Elvin installed **openHAB**

## Tasks: <a name="task"></a>
- [x] Lock
- [x] Operate Lock using card reader
- [ ] Operate using openhab
- [ ] Operate using homeassistant
- [x] Create senario for Project 2
- [x] Create shopping list
- [x] Create Kanbanflow
- [x] Temperature sensor 
- [x] Incoorporate display

<a href="#top">Back to top</a> 

### Lock<a name="lock"></a>
- Connected the wemos d1 mini and the lock
- Initialised and added the device to node2
- **Command:**  Special command to connect the lock to the node
 
 ``` d("out", "lock", d0, "off", "on") ``` 

``` devices["lock"].evaluate("on") ```
- Saved the commands to aurostart.py

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
    
}
else{
    msg.payload = "off";
}
return msg;


**Result:** Failed. Not working


**Issue:**
- Tried different combinations but still not working
- Cannot figure out if the procedure we are following is correct


## Protocols and buses<a name="proto"></a>

(zigbee, zwave, bacnet, X10, rs-232, rs-422/maybe, 485/dmx, knx-bus, SPI, I2C, one-wire, canbus, ebus)

**Required Parameters:** 
- Speed
- Throughput
- Latency
- Length
- Flexibility
- Importance
- Usage example
- Domain


**Group**: Me and Manuel

**Topic**: knx-bus & ebus

I collected details on **knx-bus**

> KNX is a standardised (EN 50090, ISO/IEC 14543), OSI-based network communications protocol for building automation.
> KNX is designed to be independent of any particular hardware platform. A KNX Device Network can be controlled by anything from an 8-bit microcontroller to a PC, according to the needs of a particular implementation. 
> The most common form of installation is over twisted pair medium.

**Points for Presentation**

### KNX-bus

- OSI based network communication protocol for building automation
- Succesor to the European Home Systems Protocol (EHS), BartiBUS and
- The European Installation Bus (EIB or Instabus).
- Administered by the KNX Association.
- Designed to be independent of any particular hardware platform
- Signaling Speed: 9600 bits/s
- Maximum Segment Length: 1000m
- Flexibility: different Bus Topologies (Tree, Line, Star / mix it)
- Usage: HVAC, Shutter control, Alarm monitoring, Energy management
- Domain: Home building Automation

### Ebus

- 2-wire digital serial data-bus communication interface
- used in heating and solar energy appliances
- German manufacturers
- Length: > 100m
- Flexibility: Master -> Master, Master -> Slave
- Speed: symbol rate of 2400 baud


### Points from other teams on other protocols
- Zigbee – coordinator, router, end device, 2 years of battery life, low power, low bandwidth needs. Small scale wireless projects. The Hue.
- Zwave- Less energy than wifi, provide a reliable, low latency transmission of small data packets.
- RS – 232 – defines communication between data terminal equipment, computer terminal, replaced by usb, used in industrial machines, scientific gear.
- RS-422 – applications early macintosh, no protocol definition. Only defines voltage levels.
- SPI – shared clock, master slave acritechture. Single way transmission. Used for embedded systems. Ex: semnsors, camera lenses, card readers,
- I2C – serial half duplex, master slave relationship, only 2 bus lines required. Ex: systems management bus, power mgmt. bus, display data channel. (Low active- one curve, one voltage. Devices of different voltages can be connected along.) 10 bit address- 1024 devices. Raspberry displays.
- Canbus – mostly used in vehicles, multiplex electric wiring in automotives – to save copper, 50kbits/s ,1000m, multi master serial bus architecture.
- Modbus – serial communication protocol, use its own PLC, very flexible – easy to deploy, maintain, openly published, licence free, simple to measure temperature, used in SCADA systems. 
- X10 - communication among electronic devices used for home automation. Since 1975 Speed: Slow, 0.75s to transmit a device address and a command.
- OneWire -is a device communications bus system. Speed: communicated at a speed of up to 16.3kbps, which is now called "standard speed".

 <a href="#top">Back to top</a>

## Senario for Project 2<a name="senario"></a>

- Group met and came up with a senario 
- I defined the __friend__'s basic details and shared the document 
- Final [Senario](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Lecture%20Notes/Project2_Senario.md)


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
 
 <a href="#top">Back to top</a>
 
 ## Operate Lock using card reader<a name="lockcard"></a>
 
 Anastesia completed the task using the NodeRed and gave the Knowledge transfer
 
<a href="#top">Back to top</a>

[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)
