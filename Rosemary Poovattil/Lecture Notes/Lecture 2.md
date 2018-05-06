# Table of contents
1. [What does the term home & building automation entail?](#hab)
    1. [Services](#Ser)
    2. [MQTT: M2M Communication](#m2m)
2. [Practical](#prac)
3. [Points to remember](#notes)


## What does the term home & building automation entail? <a name="hab"></a>
- Automation
- Efficiency 
- Security
- Comfort
- Privacy
- Protection
- Configurability
- Flexibility
- Stability
- Connectivity/Networking
- Integrability


### Services: <a name="Ser"></a>
Lighting, Switches, Heating, Physical
Access, Entertainment, HVAC, Traffic
Control/Guidance, Information, Backups, Monitoring,
Remote Access 

Lightning and shading: blinds, Motion detectors, daylighting, switching and dimming. Smart windows.

Security and safety: alarms

<a href="#top">Back to top</a>

### MQTT: M2M Communication <a name="m2m"></a>

- Machine to machine communication  
- Can be implemented anywhere, not necessarily in IoT only

Framework for creating network communication. predate of IoT. -Specific channels, msg passing. Subscribe hierarchy. (C# - python program communication)

<a href="#top">Back to top</a>

## Practical: <a name="prac"></a>
- [x] Switch led on one Wemos D1 Mini with sending mqtt command on pi
- [x] Use button to switch led

### Switch led 
Followed the instructions given in video. No big issues.

Did along with Chirantha. For command details click [here](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Chirantha%20Peramunage-_/IoT%20Lecture%20Logs/lecture2.md#Practical_Session)

### Light turn on/off using Button
Tried Button alone in a node and saw the status publishing when button pressed and when not pressed.
To combine the two nodes (LED and Button) we use mqtt.

Did along with Chirantha. For command details click [here](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Chirantha%20Peramunage-_/IoT%20Lecture%20Logs/lecture2.md#Practical_Session)

**Issue Faced**: Pi WiFi not connecting on Laptop, but connecting on phone.

**Solution**: Just **renamed** the wifi name

Commands used to edit name
 ``` sudo editor/boot/config.txt ``` 
``` sudo reboot``` 

<a href="#top">Back to top</a>


## Points to remember: <a name="notes"></a>

- To work with a Wemos we should first *initialize* it
- While initializing make sure the respective Wemos is connected directly to the Pi in series port
- Once initialised, use ``console`` command to enter the respective node
- If the Wemos is connected to the Pi we can use the command ``console_serial``


<a href="#top">Back to top</a>


Installed matrix for the common chatroom.


**Mistake**: Didn't 'Commit changes' in git. Thus lost the notes written during class


<a href="#top">Back to top</a>

[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)
