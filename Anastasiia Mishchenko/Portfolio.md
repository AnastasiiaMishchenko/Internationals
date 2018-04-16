<a name="top"></a>
## Table of Contents  
[Q1: Who am I](#q1) </br>
[Q2: Movie time](#q2) </br>
[Q3: IoT definition](#q3) </br>
[Q4: Installation on Raspberry Pi from Pre-Prepared Image](#q4) </br>
[Q5: Remove the password](#q5) </br>
[Q6: First IoT Nodes](#q6) </br>
[Q7: Light turn on/off](#q7) </br>
[Q8: Home and building automation](#q8) </br>
[Q9: Home Automation Debate: Everybody should use Home Automation. True or False?](#q9) </br>
[Q10: BACnet and other protocol](#q10) </br>
[Q11: NFC reader & smart lock](#q11) </br>
[Q12: Install of the home-assistant](#q12) </br>
[Q13: KNX](#q13) </br>
[Resources](#resources) </br>

<a name="q1"></a>
## Q1: Who am I?
**1.	Who are you**
* Anastasiia Mishchenko
* Ukraine
* Energy Informatics
* Exchange year as an MC student (2016/17)
* Bachelor in Software Engineering 

**2. What do you expect**
* To get the understanding of home and build automation

**3. Strength and weaknesses**
- Strength: 
  - Goal oriented
  - Strict to the deadlines
- Weaknesses:
  - Postpone till the last minute
  
 <a name="q2"></a>
 ## Q2: Movie time
 **Film 1(Bing Bang Theory)**
 - Scenarios and application domains: 
   - Lighting
   - Privacy
  - Technologies:
    - Using the Internet
  - Feasibility: 
    - Yes (remote control)
  - Weirdness/crazyness (any concerns?):
    - Useless
    - Crazy
    - Not efficient usage of resources, more for fun
    
As for my opinion, the performed action could be implemented in a real life. It would probably won't be so fast (responce) but it is complitely useless use of resources. </br>
     
   **Film 2(Semens)**
   - Scenarios and application domains: 
     - Security and safety
     - Optamized usage of Energy
     - Energy cooperation with other fields except distribution
     - Dynamic statistic collecting and usage
     - Safe ecvacuation
     - Exchange information in a real time
     - Parking
   - Technologies:
     - Intelligent networks
     - Lighting and voice guidense 
     - Holographic displays
     - Smart grids
     - Sensors (on floors, security sensors)
     - Elevators
     - Electric cars
   - Feasibility: 
     - Not yet (Holographic display, elavators, sensors on a floors)
     - Possible (electric cars, smart grids, lighting and voice guidance)
   - Weirdness/crazyness (any concerns?):
     - No
     
In my opinion, the film loos way to "future". Some of the parts are pretty cool, like analyzing system for the rescuers  to analyze the situation during the fire, for example and react more efficient but it is still not so up to date right now.</br> 
     
   **Film 3(The Internet of Scrimps)**
   - Scenarios and application domains: 
     - Control lights
     - Serves drinks
     - Safety
     - Organize incoming calls and social medias
   - Technologies:
     - Voice control system
     - Social networks 
     - Internet
     - Cell phone
     - Tablet
     - Intelligent Fridge
   - Feasibility: 
     - Not yet (drinking maschine)
     - Yes
   - Weirdness/crazyness (any concerns?):
     - No
     - Yes (playing music on a kitchen supplies)
     
The film by itself is pretty funny but a bit stupid at the same time.  I could not come up with an idea in which life situation I will need such feature as  playing the music over the kitchen supplies. </br>
     
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q3"></a>
 ## Q3: IoT definition
 **Definition:**
 this is the concept of basically connecting any device with an on and off switch to the Internet (and/or to each other). It is the network of physical devices, vehicles, home appliances and other items embedded with electronics, software, sensors, actuators, and connectivity which enables these objects to connect and exchange data. Each thing is uniquely identifiable through its embedded computing system but is able to inter-operate within the existing Internet infrastructure.
 
 **Domains:**
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

 **Devices:**
 - Fitness trackers
 - Smart lock
 - Smart phoones
 - Smart grids
 - Bluetooth tracker
 - Wifi lighting
 - Thermostats
 - Light ballb
 - Home Energy Monitors
 
 **Useful materials:**
 <div align="center">
    <p>
      <a href="https://www.youtube.com/watch?v=QaTIt1C5R-M" target="_blank"><img src="http://img.youtube.com/vi/QaTIt1C5R-M/0.jpg" /></a></br>
      The Internet of Things: Dr. John Barrett </br>
      <a href="https://www.youtube.com/watch?v=_AlcRoqS65E" target="_blank"><img src="http://img.youtube.com/vi/_AlcRoqS65E/0.jpg" /></a></br>
      What is the Internet of Things? And why should you care?: Benson Hougland </br>
      <a href="https://www.youtube.com/watch?v=mzy84Vb_Gxk" target="_blank"><img src="http://img.youtube.com/vi/mzy84Vb_Gxk/0.jpg" /></a></br>
      The internet of things: Jordan Duffy </br>
    </p>
 </div>
 
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q4"></a>
 ## Q4: Installation on Raspberry Pi from Pre-Prepared Image
 1. Download the image.
 2. Check the sha256-cheksum of the image with a comand ```shasum -a 256 ulnoiot-pi.img.xz```.  </br>
 **Note:** I applied the command to the unpacked image which lead to the different checksum.
 3. Install the iTerm2 and XQuartz.
 4. In the file config.txt set up ```uiot_ap_name``` and ```uiot_ap_password``` to the ```MC509``` and ```MC509SS2018```.  </br>
 **Note:** At first I changed the wrong parameters: ```uiot_wifi_name``` and ```uiot_wifi_password``` and set up the password which is shorter than 8 chracters. These leds to the result, that the WiFi was not in the list of wifis.
 5. Connect to the ulnoiotgw via ssh ```ssh -X pi@192.168.12.1``` and password ```ulnoiot```.
 6. Run the command ```ulnoiot upgrade``` to make sure that the latest version of ulnoiot is used.
 
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q5"></a>
 ## Q5: Remove the password
 1. Get to the ssh folder ```cd .ssh/```.
 2. Show the password ```cat id_rsa.pub```.
 3. Copy it to the clipboard. </br>
 **Note:** the first try failed because I did not copy the “ssh-rsa” as part of the key.
 4. Connect to the ulnoiotgw via ssh.
 5. Edit the ```authorized_key``` file with the command ```editor .ssh/authorized_keys```.
 6. Set the read and write permission ```chmod 600 .ssh/authorized_keys```. </br>
 **Note:** after the removing of the password, I still need to unter my keychan password to log in.
 
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q6"></a>
 ## Q6: First IoT Nodes
 1. Create a folder ```mkdir assignment_light```. 
 2. Copy the file ```cp –R /home/pi/ulnoiot/lib/system_template/ /home/pi/ulnoiot/assignment_light/```.
 3. Rename the directory “system_template” ```mv “system_template” “iot-light” ```.
 4. Rename the directory “node_template” ```mv “node_template” “onboard_blinker”```.
 5. Get into the derectory ```cd onboard_blinker```.
 6. Initialize a current node ```initialized```.
 7. Access the command prompt ```console```. </br>
 **Note:** after the performed commands the microcontroler was not detected, so it was unpluged and pluged in again, the problem was still the same. As a result, it turned out that the problem was in a cabel which is not working.
 8. Initialize the onboardled ```onboardled.init( Pin.OUT )```.
 9. Use commands ```onboardled.off()``` and  ```onboardled.on()``` to turn on/off light on a microcontroller.
 10. ```sudo poweroff```  shut down the Raspberry Pi.
 
 <div align="right"><a href="#top">Back to top</a></div>
 
<a name="q7"></a>
## Q7: Light turn on/off
1. Connect a microcontroller which was initialized before, directly to the laptop.
2. Use a command ```console``` to enter the microcontroller.
3. ```d("led", "green", onboardled, "off", "on")``` - initialize the onboard led.
4. ```devices["green"].evaluate("off")``` and ```devices["green"].evaluate("on")``` - turn off/on the led. Activate the device with ```run()``` command.
5. Connect a second micro controller directly to the Raspberry Pi and ```initialized``` it.
6. Use a command ```console_serial``` to enter the micro controller. </br>
 **Note:** the problem was with misunderstanding of commands ```console_serial``` and ```console```. As a result, I always initialize the same micro controller.
7. Create a variable ```b1 = d("button", "b1", d3, "off", "on")``` and ```b1.updated_value()``` to see the changes while pressing the button. Activate the device with ```run()``` command.
8. ```mqtt_send onboard_blinker_2/green/set on``` and ```mqtt_send onboard_blinker_2/green/set off``` will send the request over the gateway to the led in onboard_blinker_2 directory.
9. ```mqtt_action onboard_blinker/b1 anychange abc mqtt_send onboard_blinker_2/green/set``` will send the switch on/off request over the gateway to the led in onboard_blinker_2 directory when the button from the onboard_blinker directory is pressed. 
10. ```sudo poweroff```  shut down the Raspberry Pi.

After performing the commands manually, the ``` autostart.py``` files of both microcontrollers were modified. For the microcontroller which performs on and off of the led, the following lines were added. 

```python
d("led", "green", onboardled, "off", "on")
devices["green"].evaluate("off")
devices["green"].evaluate("on")
run(10)
```

For the microcontroller which performs the button clicks, the following lines were added.

```python
b1 = d("button", "b1", d3, "off", "on")
b1.updated_value()
run(10)
```

After, we can use the command ```deploy noupdate``` from the node folder to run the ```autoupdate.py``` file.

<div align="right"><a href="#top">Back to top</a></div>

 <a name="q8"></a>
 ## Q8: Home and building automation
 
**Home and building automation** - is the automatic centralized control of a building's heating, ventilation and air conditioning, lighting and other systems through a building management system or building automation system (BAS).

**Fields:**
- Entertainment
- Lighting
- Voice control
- Heating
- Air condition
- Privacy
- Presents detection
- Convinience
- Energy optimization
- Efficiency
- Centralization    
 
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q9"></a>
 ## Q9: Home Automation Debate: Everybody should use Home Automation. True or False?
 
Our team was indicated as a pros team during the debates. After the analyzing of the information from the Internet we came up with 4 specific topics:
1. After reading this article about mobile apps which combine security and home functionality, so I would like to discuss the security (remotely monitoring) and the installation of the system.
2. Also, we would like to discuss, the market impact of home and building automation. Power consumption by energy saving devices. (Article: “Home automation market growth demand and key players to 2015-2025”).
3. In “Roseville Eskaton deploys home automation tablets for residents” article, it was stated that senior living apartments will turn into smart homes allowing each resident to manage their day-to-day activities. That’s why we want to discuss learning curve and easiness of usage for everyone. 
4. Variation of the devices which provides security, flexibility, and centralized control.

Nevertheless, we also have a more extended list of general topics which we also take a look at during the preparation for debates:
- Security
- Energy efficiency.
- Compatibility and flexibility of the systems.
- Costs and savings.
- Environmental impact.
- Reliability.
- The complexity of the system.
- Entertainment.
- Monitoring/ device management.

Despite the fact that I belong to the pros team, personally, I cannot fully agree with the statement that home automatization should be in each house. We cannot ignore the fact that according to the global analysis and forecast “Home Automation Market to 2025 " published on November 2017, global home automation system market is expected to grow from US$ 35.24 billion in 2016 to US$ 113.82 billion by 2025 at a compound annual growth rate (CAGR) of 13.93% between 2017 and 2025.  This is the strong shos that it is a dynamic industry which is financed and develop rapidly. Another driving force is: 
- increasing usage of smartphones, tablets, and other handheld devices increasing penetration of Internet 
- growing awareness of energy consumption and energy management building infrastructure 
- growing number of residential projects  
- growing need for remote home monitoring solutions  

I think, that there is still a high issue with security, in case of hacking of your system, other people could get exes to private information and your timetable which could lead to much worse problems later. Another point is the geographical inequality, according to the global analysis and forecast “Home Automation Market to 2025 ", North America dominates Global home automation market. It captures approximately 40% of the total market share closely followed by Europe. Asia-Pacific is expected to grow at the highest CAGR due to increasing building infrastructure at a significant rate and growing number of residential projects. The problem is less awareness among people. If in Europe people are more educated about the background of such systems and techno novety, it could be a challenge in Asia-Pacific where people are more "scared" about the things which are new for them. The last but not the least is the price. The price dropping is expected in following years but according to the current prices, there are some basic costs of installing home automation:
- Basic starter kit (lights or deadbolt controls): $40 to $500.
- Wireless mesh systems (Z-Wave, etc.): $300 to $600.
- Monthly service: $35 to $70 per month, plus activation fees, which normally cost around $200 to $500. Equipment is usually free.
- Cloud automation – $179 to $299.
- Hardwired – Unlike the above choices, which simply plug into your existing outlets, hardwired systems become part of your home. Hardwired systems are much more reliable and cost from $3,000 to $15,000 to install.

In general, the cost to have a professional install your system is around $85 an hour. Most homeowners can install plug-in systems, but it’s best to have a professional install hard-wired systems.
 
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q10"></a>
 ## Q10: BACnet protocol
 
 [BACnet protocol](https://docs.google.com/presentation/d/1BVP72s9Eh-SC3lFz0tEJ401lu9jmaYVq8U_FKDnpXBc/edit?usp=sharing)

**Zigbee**
- IEEE 802.15.4 specification
- Coordinator/Router/End Device
- at least 2 years battery life
- for low-power, low-bandwidth needs
- for small scale project which need wireless connection
- intended to be simpler and cheaper than other WPANs (eg Bluetooth)
- Length: 10-1500 meters
- Data Rate: 20-250 kbit/s
- Latency: 15 ms
- Flexibility: Not suitable for movable devices
- Application: wireless light switches, home energy monitors, traffic management system, smoke detector,…

**Z-Wave**
- Speed
  * ≤ 100kbit/s
- Throughput
  * ≤ 40kbit/s
- Latency
  * Low-latency
- Length
  * 800-900 MHz radio frequency (range up to 100 meters)
- Flexibility
  * Globally standardised;
  * Standardised Middleware and Z-Wave over IP specification
- Importance
  * Important in sensor communications
- Usage example
  * Home automation (thermostats, lighting control, …)
- Domain
  * Home automation
- Introduced
  * 2001 by Zensys
  * International standard
- Mesh network
  * Each node can talk to each other
- Open source
- Design
  * Provide a reliable, low latency transmission of small data packets
- Less energy than Wi-Fi
- Higher signal range than Bluetooth

**SPI**
- Synchronous serial communication (shared CLK)
- Full Duplex mode
- Master-Slave architecture (with single master)
- Slave select line to support multiple slave devices
- 4 wires: CLK, MOSI, MISO, SS
- De facto standard for short distance communication
- Primarily used in embedded systems

Speed & Throughput
- Will be limited by one of 3 factors
  * Clock speed
  * The ability of CPU to service the SPI data
  * Output driver strength (how fast a signal can the PCB/Hardware carry)
  
Latency & Length
- Latency can be as low as one clock cycle
- Data frame sizes from 1 to 16 bit
- Larger sizes by splitting into groups of 16 bit or less
- Cable length up to a few meters

Usage examples
- Talk to a variety of peripherals: sensors (Temperature, Humidity, ….), memory, LCDs, camera lenses
- RFID card reader used in class

**I2C**
- Designed by Philips
- Version 6
- Serial and Half-duplex
- Simple master/slave relationship
- Multi-master bus
  * Arbitration detection
  * Collision detection
- Only two bus lines are required

Speed & Throughput
- Clock is transmitted by the sender
  * Receiver is always able to synchronize 
- Several speed grades
  * Standard(0.1 Mbits/s)
  * Full speed (0.4  Mbits/s)
  * Fast mode (1.0  Mbits/s)
  * Highspeed (3.4 Mbits/s)
  
Length
- 1 meter at 100 Kbaud
- 10 meters at 10 Kbaud

Usage Example
- Usage in different control architectures
  * System Management Bus
  * Power Management Bus
  * Intelligent Platform Management Interface
  * Display Data Channel
  * Advanced Telecom Computing Architecture
- 7 bit Address = 128 devices
- 10 bit Address = 1024 devices

**rs232**
- is a standard for serial communication
- introduced in 1960 
- defines communication between:
- data terminal equipment (computer terminal)
- data circuit terminating equipment (modem, peripheral device)
- defines:
  * electrical characteristics 
  * timing of signals
  * meaning of signals
  * physical size of connectors
- last updated in 1999
- replaced by USB
- still used in industrial machines/scientific gear/network equipment
- maximum cable length: 15m

**rs422**
- some kind of successor of rs-232 
- last updated 2005(can be programmed the same way)
- only defines  voltage levels, no protocol definition (only refers to others)
- Multi-drop example:  you can connect one PC (the Commanding device) to 10 temperature controllers (listeners) / up to 32
- Applications
  * early Macintosh
  * extend range of rs-232

**rs485**
- some kind of successor of rs-422
- last updated 2003
- Multi-drop: multiple commanding and multiple
- listening devices
- only two wires (instead of 4)
- programming more difficult (sending/receiving on same wires) need to turn on/off transmitters
- Applications:
  * underlying physical layer of.Modbus/Profibus
  * aircraft cabins
  * theatre and performance venues
  * building automation,  e.g.control video surveillance systems
  * model railways
  
 **DMX Digital Multiplex**
- is a standard for digital communication
- often used to control stage lighting and effects
- primary method for linking controllers to dimmers/special effects
- nowadays a lot of usages:
  * from christmas lights to billboards
- uses EIA-485 (rs-485) as its physical layer + a communication protocol
- has no error handling:
  * not used in hazardous domains (pyrotechnic)
  * false triggers caused by
    * electrical fields
    * long cables
    * poor quality
- maximum recommended length: 300 m
- consists of:
  * one controller
  * one or more slaves
  * terminator
- example: lighting console and multiple lights

**X10**
- What?: communication among electronic devices used for home automation. Since 1975
- Speed: Slow, 0.75s to transmit a device address and a command.
- Throughput: 3000 bits per second.
- Latency: 60 Hz wave with a maximum delay of 100 microseconds. (TW523). 
- Length: 310MHz in U.S.  & 433.92 MHz on European systems. 
- Flexibility: Option to upgrade. X10 modules only react to commands, they do not transmit back a status, which limits flexibility. 
- Importance: 
  * Advantages: Cheap, Availability
  * Disadvantages: poor performance (can only transmit one command at a time), distance limitations, less reliability, power phase limitations, Lack of encryption.
- Usage examples: mostly hybrid systems nowadays along with Zigbee, Z-wave protocols. 
- Examples: X10 Lamp dimmer module, X10 in Wall dimmer Switch. X10 appliance module can be used to monitor doors & windows as well. 

**OneWire**
- What?: is a device communications bus system. 
- Speed: communicated at a speed of up to 16.3kbps, which is now called "standard speed." To reduce the time needed to read a 64Kbit memory iButton to less than 1 second, a high-speed mode called "overdrive"
- Flexibility:  1-wire slave and I2C master operational modes. Supports 15 kbps and 77 kbps 1-wire protocol with packetized I2C data payloads
- Advantages of 1-wire interface
  * Following are the benefits or advantages of 1-wire interface:
    * Multiple slaves are accessed using only 2-wires in this interface type. 
    * Due to use of less wires, the interface is cheaper. 
    * It is easy to implement the interface. 
    * The interface supports longer distance (about 300 meters)
  * Disadvantages of 1-wire interface:
    * It is implemented both in the hardware as well as software. The synchronization of data at the receiver has to be taken care in software which is a complex task. 
    * Though the interface supports longer distance, it is limited due to noise and cable capacitance. 
    * It supports slower speed of communication. 
    * 1-wire slave devices are manufactured by Dallas semiconductor only.
    
**KNX-bus**
- OSI based network communication protocol for building automation
- the succesor to the European Home Systems Protocol (EHS), BartiBUS and
- the European Installation Bus (EIB or Instabus).
- administered by the KNX Association.
- designed to be independent of any particular hardware platform
- Signaling Speed: 9600 bits/s
- Maximum Segment Length: 1000m
- Flexibility: different Bus Topologies (Tree, Line, Star / mix it)
- Usage: HVAC, Shutter control, Alarm monitoring, Energy management
- Domain: Home building Automation

**Ebus**
- 2-wire digital serial data-bus communication interface
- used in heating and solar energy appliances
- German manufacturers
- Length: > 100m
- Flexibility: Master -> Master, Master -> Slave
- Speed: symbol rate of 2400 baud
 
**CAN(Controller Area Network)bus**
- Invented by Bosch | Standardized since 1993
- Originally designed for multiplex electric wiring in automotives (to save copper)
- Mostly used in vehicles
- Datarates Up to 1 Mbit/s (high speed CAN) & below 40 meters of length
- 50 kbits/s by 1000 m
- Multi-master serial bus to connect several ECU (Electric Control Units)
- All nodes are connected to each other through a two wire bus (twisted pair wires)
- Message based -> Each CAN node is authorized to access the CAN bus immediately after an event occurs 
- High importance since it‘s the most commonly used bus structure in automotives. In the home automation it‘s not of high importance because there are few component available which support it and it requires wiring.
- High configuration flexibility

**MODbus**
- Serial communication protocol
- Uses it‘s own PLC
- De facto standard to connect industrial electronic devices
  * Developed with industrial application in mind
  * Openly published and license-free
  * Easy to deploy and maintain
  * Moves raw bits or words without many restrictions on vendors
- Very flexibly
  * Simple for only send temperature
  * or in big SCADA systems (e.g. Smart Grids)
- Different versions
  * Serial (modbus RTU or modbus ASCII)
  * Ethernet (modbus TCP or modbus UDP)
- Unique address
- Master/Slave communication
  * Only master is allowed to send commands
- 8-bit asynchronous lines like RS-485
  * 50 meter no signal faster than 2 Mbit/s

 <div align="right"><a href="#top">Back to top</a></div>
 
<a name="q11"></a>
 ## Q11: NFC reader & smart lock
 
**Note** The biggest mistake was to flash again the Py instead of running the ```ulnoiot upgrade```. As a result, I start all over again.

In **HIGH** if there is some input voltage – the circuit will close, if not – means the circuit is open
In **LOW** would be the opposite. 

- **GND** would be –
- **VCC** would be +
- **SIG** signal would be connected via breadboard

1. To start, I try to maintain the smart lock with a button.
2. First of all, unscrew the screw-bolts.
3. When button is pressed – the lock is open (indicated with a led on a 5 pin relay).
![Structure](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Anastasiia%20Mishchenko/Images/IMG_0224.JPG)

After I procedure to the next task, connect smart lock with nfc reader.

1. Create a reader. 
```python
r = d("mfrc522","reader",d0)
run()
```
2. Create a smart_lock
```python
d(“out”, “smart_lock”, d0, “off”, “on”)
devices[“smart_lock”].evaluate(“off”)
devices[“smart_lock”].evaluate(“on”)
run()
```
3. In REDnode:
```python
var idArray= msg.payload.split(" ");
var id = idArray[1];
if(id === "2b71112b60"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;
```
4. After receiving the id “2b71112b60” send a message to a lock to set it as on, if not - off.
![REDnode](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Anastasiia%20Mishchenko/Images/Screen%20Shot%202018-04-10%20at%2011.47.23.png)
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q12"></a>
 ## Q12: Install of the home-assistant
 
 1. Get Python 3.5.3 or later from https://www.python.org/downloads/mac-osx/
 2. In Terminal 
 ```python
  sudo pip3 install homeassistant
  hass –open-ui
  ```
  **Note**The last one did not work, as it turned out, I should restart the terminal 
  3. To open the configuration file to modify it.
  ```python
  cd .homeassistant/
  nano configuration.yaml
  ```
 <div align="right"><a href="#top">Back to top</a></div>
 
  <a name="q13"></a>
 ## Q13: KNX
 
KNX is a standardized communication protocol for intelligent buildings. KNX is the successor of three previous standards: the European Home Systems Protocol (EHS), BatiBUS, and the European Installation Bus (EIB or Instabus). 

In contrast to a standard electric installation, there is no hard wired connection between the control units and the power supply, for example a light switch is not directly connected with the respective light. Instead, devices and electric assets are connected via the BUS which runs on 29 Volts. All BUS devices can be programmed with one common tool, thus the KNX BUS allows an easy and very flexible installation, and even subsequent changes can be done easily without changing the wiring.

Basically, a KNX system requires the following components:
- Power Supply for the power of the installation
- Sensors (push buttons, thermostats, air speed meters etc.) that generate commands as telegrams
- Actuators (switch relays for lights, blinds etc.) that receive the telegrams and perform certain actions
- The BUS that connects all Sensors and Actuators

The smallest entity within the KNX topology is a line, respectively a line segment. A line can contain a maximum of 64 devices. This is enough for most small scale projects. For bigger projects, up to 15 lines can be combined within one area - connected via a main line. Different lines may be connected to the main line with a Line Coupler. 

Furthermore, it is also possible to connect up to 15 areas to a backbone. Single areas are connected to the backbone line via a Backbone Coupler. KNX end devices may be connected anywhere in this topology. Up to 255 KNX end devices may be addressed in any sub- network. KNX end devices may be numbered from 1 to 255. But KNX end devices may NOT have device number 0. 

Each KNX device (Backbone Coupler, Line Coupler, KNX end device ...) must have an Individual Address. This Individual Address is unique throughout the complete topology. 

![KNX certificate](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Anastasiia%20Mishchenko/Images/Screen%20Shot%202018-04-11%20at%2009.49.11.png)

 <div align="right"><a href="#top">Back to top</a></div>

 <a name="resources"></a>
 ## Resources:
 1. [The Internet of Things IoT comes under which domain](https://www.quora.com/The-Internet-of-Things-IoT-comes-under-which-domain)
 2. [UlnoIoT](https://github.com/ulno/ulnoiot#installation)
 3. [SmartThings ADT Home Security: Where smarts meet security](http://www.zdnet.com/article/smartthings-adt-home-security-where-smarts-meet-security/)
 4. [Home Automation Market Growth, Demand and Key Players to 2015-2025](https://www.latestmarketreports.com/2018/03/26/home-automation-market-growth-demand-and-key-players-to-2015-2025/)
 5. [Roseville Eskaton deploys home automation tablets for residents](http://www.thepresstribune.com/article/3/23/18/roseville-eskaton-deploys-home-automation-tablets-residents)
 6. [The Best Smart Home Devices of 2018](http://uk.pcmag.com/digital-home/85/feature/the-best-smart-home-devices-of-2018)
 7. [Best Smart Home Devices And How IoT Is Changing The Way We Live](https://www.forbes.com/forbes/welcome/?toURL=https://www.forbes.com/sites/forbestechcouncil/2017/06/06/best-smart-home-devices-and-how-iot-is-changing-the-way-we-live/&refURL=&referrer=#27b3bf8d43bd)
 8. [The Pros and Cons of Home Automation Systems](https://www.mythinkenergy.com/pros-cons-home-automation)
 9. [The pros and cons of smart homes](https://www.clickatell.com/articles/technology/the-pros-and-cons-of-smarthomes/)
 10. [Smart Home: What are the pros and cons going with following Home Automation provider in India?](https://www.quora.com/Smart-Home-What-are-the-pros-and-cons-going-with-following-Home-Automation-provider-in-India?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)
 11. [Is home automation right for you](https://www.somfysystems.com/ideas-insights/home-automation/is-home-automation-right-for-you)
 12. [The Pros and Cons of Having a "Smart" Home](https://www.linkedin.com/pulse/pros-cons-having-smart-home-frank-darras/)
 13. [The Pros and Cons of Smart Home Technology](https://blog.parksathome.com/the-pros-and-cons-of-smart-home-technology/)
 14. [THE ADVANTAGES & DISADVANTAGES OF A HOME LIGHTING CONTROL SYSTEM](https://www.customcontrols.co.uk/blog/what-are-the-pros-and-cons-of-a-home-lighting-control-system/)
 15. [Advantages and disadvantages of converting your home into a smart home](http://regencyhomesomaha.com/advantages-and-disadvantages-of-converting-your-home-into-a-smart-home/)
 <div align="right"><a href="#top">Back to top</a></div>
