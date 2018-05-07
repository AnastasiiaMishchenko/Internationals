[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)

# Table of contents

1. [Tasks:](#task)
2. [KNX Tutorial](#knx)


## Tasks: <a name="task"></a>

- [x] Learn from KNX Academy-ets e campus
- [x] Work with kodi- Download some music. 
- [ ] Make the Media work with NodeRed & Kodi
- [x] Make the Lamp work
- [ ] Mqtt Simulator using NodeRed (Install) 
- [ ] Make a motion sensor using the distance sensor 
- [x] RGB Light
- [x] Voice input (Android) - IFTTT
- [ ] Espeak or speach response- Mqtt triggered **voice output**


## KNX Tutorial <a name="knx"></a>

[Register](https://my.knx.org/account/register)
KNX ETS5 eCampus

> basic concepts of the KNX bus
KNX is a standardized communication protocol for intelligent buildings. 
devices and electric assets are connected via the BUS which runs on 29 Volts.
All BUS devices can be programmed with one common tool
> Basically, a KNX system requires the following components:
> Power Supply for the power of the installation
Sensors (push buttons, thermostats, air speed meters etc.) that generate commands as telegrams
Actuators (switch relays for lights, blinds etc.) that receive the telegrams and perform certain actions
The BUS that connects all Sensors and Actuators

> P-2

KNX is designed to be independent of any particular hardware platform.
most common transmission medium in KNX is twisted pair
It is possible to combine - by default normally incompatible media - via KNX media couplers.

> p-3

The smallest entity within the KNX topology is a line, respectively a line segment. A line can contain a maximum of 64 devices. This is enough for most small scale projects. 

- up to 15 lines can be combined within one area - connected via a main line.Line Coupler. 
- it is also possible to connect up to 15 areas to a backbone. Single areas are connected to the backbone line via a Backbone Coupler. 
- KNX end devices may be connected anywhere in this topology. Up to 255 KNX end devices may be addressed in any sub- network. KNX end devices may be numbered from 1 to 255. But KNX end devices may NOT have device number 0. 
-Each KNX device (Backbone Coupler, Line Coupler, KNX end device ...) must have an Individual Address. This Individual Address is unique throughout the complete topology. 

> Example:

- The first device we need to install is the power supply. A KNX BUS needs to be provided with a 29 V direct current.
- The actual circuit breakers are called actuators. They typically come as multi channel switch acutators, for example as a 4-fold switch actuator that is equipped with 16 ampere relays.
- Push buttons sensors consist of a universal flush-mounted bus coupler and a bus end device. Both devices have to be from the same manufacturer.
- The push button is put onto the bus coupler. The connection is established by a 10-pin connector, the so-called "Physical External Interface".
- Last but not least, we need to connect the high voltage current. The power supply as well as the switch actuator get wired to the power circuit.
- Now, we connect the consumer, in our case the one light.
- With the help of a PC running ETS5, all bus devices can be programmed. Afterwards, the function-check takes place – now it’s your turn to test the system.

> install ets5

## Rosemary Josy Poovattil
has successfully completed the KNX eCampus
ETS Course
10th April 2018
Course-Grade: 94%
User-ID: 97838



## BACnet by Anastasiia 

BACnet is a communications protocol for Building Automation and Control (BAC) networks that leverage the ASHRAE, ANSI, and ISO 16484-5 standard protocol.

BACnet was designed to allow communication of building automation and control systems for applications such as heating, ventilating, and air-conditioning control (HVAC), lighting control, access control, and fire detection systems and their associated equipment. The BACnet protocol provides mechanisms for computerized building automation devices to exchange information, regardless of the particular building service they perform.


## Installed MQTT.FX and Kodi

<a href="#top">Back to top</a>

[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)
