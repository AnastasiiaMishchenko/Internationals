# Table of contents

1. [Tasks:](#task)


## Tasks: <a name="task"></a>

- [ ] Learn from KNX Academy-ets e campus
- [ ] Play with kodi codi ?
- [ ] Make the Lamp work
- [ ] Mqtt Simulator using NodeRed (Install) 
One sensor and one actuator

## KNX Tutorial

[Register](https://my.knx.org/account/register)
KNX ETS5 eCampus
basic concepts of the KNX bus
KNX is a standardized communication protocol for intelligent buildings. 
 devices and electric assets are connected via the BUS which runs on 29 Volts.
 All BUS devices can be programmed with one common tool
 
 
 Basically, a KNX system requires the following components:

Power Supply for the power of the installation
Sensors (push buttons, thermostats, air speed meters etc.) that generate commands as telegrams
Actuators (switch relays for lights, blinds etc.) that receive the telegrams and perform certain actions
The BUS that connects all Sensors and Actuators

P-2

KNX is designed to be independent of any particular hardware platform.
most common transmission medium in KNX is twisted pair
It is possible to combine - by default normally incompatible media - via KNX media couplers.

p-3

The smallest entity within the KNX topology is a line, respectively a line segment. A line can contain a maximum of 64 devices. This is enough for most small scale projects. 

- up to 15 lines can be combined within one area - connected via a main line.Line Coupler. 
- it is also possible to connect up to 15 areas to a backbone. Single areas are connected to the backbone line via a Backbone Coupler. 
- KNX end devices may be connected anywhere in this topology. Up to 255 KNX end devices may be addressed in any sub- network. KNX end devices may be numbered from 1 to 255. But KNX end devices may NOT have device number 0. 
-Each KNX device (Backbone Coupler, Line Coupler, KNX end device ...) must have an Individual Address. This Individual Address is unique throughout the complete topology. 
