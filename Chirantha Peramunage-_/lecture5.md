

<a name= "top"></a>

* Lecture 05 10/04/2018

# Table of contents

1. [Basics](#Basics)
Ocean devices - contains solar panal, no batteries needed. 
Zeewave - noting works when battery runs out. 

tasks
- [ ] Lamps
- [ ] login to knx, go to universiy site, make profile, get the certificate. https://my.knx.org/ basic course 
- [ ] install kodi media player. 
- [ ] mqttt simulators - temperature sensor temp go up down. use nodered. 

### Basics  <a name= "Basics"></a>

KNX is a standardized communication protocol for intelligent buildings. KNX is the successor of three previous standards: the European Home Systems Protocol (EHS), BatiBUS, and the European Installation Bus (EIB or Instabus). 

In contrast to a standard electric installation, there is no hard wired connection between the control units and the power supply, for example a light switch is not directly connected with the respective light. Instead, devices and electric assets are connected via the BUS which runs on 29 Volts. All BUS devices can be programmed with one common tool, thus the KNX BUS allows an easy and very flexible installation, and even subsequent changes can be done easily without changing the wiring.



Basically, a KNX system requires the following components:

Power Supply for the power of the installation
Sensors (push buttons, thermostats, air speed meters etc.) that generate commands as telegrams
Actuators (switch relays for lights, blinds etc.) that receive the telegrams and perform certain actions
The BUS that connects all Sensors and Actuators


KNX is designed to be independent of any particular hardware platform.

In the easiest possible way, an 8-bit micro controller can realize desired function, for more complex functionalities a pc may be necessary, according to the needs of a particular implementation.

The most common transmission medium in KNX is twisted pair, but KNX also provides other physical communication medium:
Twisted pair wiring
Powerline networking
Radio
Infrared
Ethernet /IP

It is possible to combine - by default normally incompatible media - via KNX media couplers.

The smallest entity within the KNX topology is a line, respectively a line segment. A line can contain a maximum of 64 devices. This is enough for most small scale projects. 

For bigger projects, up to 15 lines can be combined within one area - connected via a main line. Different lines may be connected to the main line with a Line Coupler. 

Furthermore, it is also possible to connect up to 15 areas to a backbone. Single areas are connected to the backbone line via a Backbone Coupler. 

KNX end devices may be connected anywhere in this topology. Up to 255 KNX end devices may be addressed in any sub- network. KNX end devices may be numbered from 1 to 255. But KNX end devices may NOT have device number 0. 

Each KNX device (Backbone Coupler, Line Coupler, KNX end device ...) must have an Individual Address. This Individual Address is unique throughout the complete topology. 

Configuration of a Lighting Control:
A very straightforward example of a lighting control is the engaging of a single light.
The following example shows you a step-by-step introduction how to implement this task with the KNX BUS technology. 
Many KNX devices come as "DIN-Cap-Assembly"-Devices and can easily be snapped to a DIN rail.
The first device we need to install is the power supply. A KNX BUS needs to be provided with a 29 V direct current.
The actual circuit breakers are called actuators. They typically come as multi channel switch acutators, for example as a 4-fold switch actuator that is equipped with 16 ampere relays.
As BUS media a twisted pair cable is used to connect all KNX devices to the BUS.
Push buttons sensors consist of a universal flush-mounted bus coupler and a bus end device. Both devices have to be from the same manufacturer.
The push button is put onto the bus coupler. The connection is established by a 10-pin connector, the so-called "Physical External Interface".
Last but not least, we need to connect the high voltage current. The power supply as well as the switch actuator get wired to the power circuit.
Now, we connect the consumer, in our case the one light.
With the help of a PC running ETS5, all bus devices can be programmed. Afterwards, the function-check takes place – now it’s your turn to test the system.


#### Set up ETS5 

Getting started
* no need to install the license 
* no need of extra dongle driver, automatically installs 
* diff between ets4 & 5, no longer have to create db
* overview default view, bus catalog, settings tabs
* access to license - in footer

Settings
* language- to change lang
* shortcuts - ex: for topology
* online catalog- for ETS app settigns, choose to automatic updates, or manual. 
* Software updates - now in footer - ETS version. weekly
* UI preferences- sw updates
* changes are automatically saved

Import manufacturer catalog
* first - download catalog
* import catalog with device info - no limit
* Catalogs tab - Certified knx products from various manufacturers. Can be downloaded online. 
* Click import - wizard  - select catalog file (KNXPROD file). can be retireved within ets5, no need to look manuf. website.
* importing - import all or selection, select lang,no need to import all products of one catalog. 
* under manufacturer - newly imported products. sorted by manuf. can be further drilled down to the different product catagories. 


#### Working with ETS5

Creating a new project
* Switch back to overview
* all exisiting projects are listed, possibility to manage details
* click + to define properties, name, knx medium, notation, create project. (backbone: Create line 1.1, topology: IP, Group address style: free,2 level or 3 level)
* created project will be oponed automatically. 
* Workplace - complete set of tools to create and config project 
* Green ETS button - return to overview. upperleft corner, return to project. 
* below menu bar, tool bar, below tool bar, main conntent, 2 panels, displaying. Add another panel - use workplace menu button. 
* Click panel label - changes the content of the panel. 
* Properties side bar on right - provide diff. containers. provides context info for the selected elements in the content area. ontext information on selected elements. 
* can resize any panel. 
* Drag to dock- yellow color. 
* save or eload - workplace container - click the + button, provide name.

Create a building structure - 
* ETS5 defines - knx devices, their connection to each other. devies are palces in rooms, a building structure. - devices are assigned to their installation location.
* Add- to add main building  
* Add flows for the building - select main building - click right part of add btn, - add floors, add rooms -to remove. 
* sue undo func. to return to previous work. also undo history in sidebar
* add a cabinet - to place powersupply. 

Add Devices -
* Catalog- all devices import so far, sort by manufacturer. actual devices right side
* implemet a lighting control - need a switch actuator to connect light with 230v
* Search, darg and drop the actuator to the utility room, also push button to living room. power supply. 
* can also be added with the tool bar at the bottom of catalog. select buliding part and click add. also possible to add several items altogether. 
* inspect detailsof device - proporties containor on side bar. 
* provide an isntallation note - 




Establish links between KNX devices 
* workplace, open new panel, group addresses.
* add main group - add a middle group for that. 
* add a group address for that. 
* Drag the group object " upper push button" from knx push button to your group address. 
* Also drag KNX switch actuator to group address. 

Adjust Product Parameters
* Select the switch actuator in the tree view and then open the parameters view
* enable the "delay, staircase lighting, flashing” for the first output of the actuator and then select the time function "ON/OFF delay” from the "Timer” tab.

Project Download
* After having configured all devices, now download the configuration on the actual KNX devices is possible.  select the dynamic folder "initial devices" in the tree view.
* open the "Pending Operations" Tab in the sidebar.
* Select all devices and click on the "Download" menu. Use the option "Download all".
* Setting the individual addresses is not shown in this simulation. Once the download is finished, you can see that the programming status of the devices has changed.


#### note: My video has no sounds, so no notes on that. Also internet was pretty slow, so took a while to finish. Finished the course with 96% score. 


### Things to do before the practical session. 
* activate wifi - boot/config
* editor ulnoiot/etc/ 
* editor ulnoiot/etc/ulnoiot.conf
* ifconfig

Also, 
* uncomment ulnoiot AP_BRIDGE
* reboot

** Practical session ** 

Started doing the Kodi set up through HomeAssistant & nodered. But Thomas suggested toused javascript and as he said it seems much easier. 

1. download mqttfx  - http://mqttfx.jensd.de/index.php/download (mqttfx-1.7.0-macos.dmg)
2. Downloading took ages, so Thomas shared his downloaded image with me. 
3. Thomas helped with the initial configuration. (Profile Name: SmarthomeRose, broker address: 192.168.12.1) 
4. Publish : n4/blue/set (node, device name, set)
5. 

* Anasthesia Presentation: BACnet Protocol.

* used for communication of multiple devices across building automation. 
* Ethternnet or IP
* Objects - resperesnt many different ascpects of control system, reperesnt physical, virtual devices
* Properties - contians info about objects, Every BACnet has identifier name type
* Services - Performs R,W, I/O Catagories - object access, device mgmt
* Network Technology - LANs, Phone line, hardwired EIA-232
* uses -Lightning, seurity
* Adv/ disadvantages- Performance, system size, robust internetworking, many vendors, Securtiy standards in newer versions, MT-TP wire length, Unrstricted growth, limited nu of field devices. 



##### for the internet issues.
* sudo iptables -t nat -D POSTROUTING 1; iptables -t nat -A POSTROUTING -s 192.168.12.1/24 -o wlan1 -j MASQUERADE	
* sudo iptables -t nat -D POSTROUTING 1; sudo iptables -t nat -A POSTROUTING -s 192.168.12.1/24 -o wlan1 -j MASQUERADE
