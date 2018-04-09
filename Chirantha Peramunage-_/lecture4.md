

* Lecture 4 03/04/2018

# Table of contents
1. [Home Assistant](#Home_Assistant)
2. [Practical Session: Smart lock](#Practical_Session_Smart_Lock)
3. [NodeRed](#NodeRed)
4. [Additional Commands used](#NodeRed)

**1.Home Assistant** <a name= "Extra_Commands"></a>

Install 'Home Assistant', login :  hass --open-ui 
Link to download: https://www.home-assistant.io/docs/installation/macos/
Installation guide: https://www.youtube.com/watch?v=hej6ipN86ls

* Issues faced - the final command to login wasn't working on the same terminal. 
* error - hass: command not found
* Workaround - open new terminal and run the same command again. (found it in a youtube video comment). 
* login :  hass --open-ui 

**2.Practical Session: Smart lock** <a name= "Practical_Session_Smart_Lock"></a>

In the meantime tried the smart lock using below code. Saved the codes on autostart.py
A group member did it mostly while I was initializing home assistant and later and shared the knowledge. 

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

**3.NodeRed** <a name= "NodeRed"></a>

* Tried the function in of NodeRED:

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

**4.Additional Commands used** <a name= "Extra_Commands"></a>

* Ignore the 'shell already in use' command. - esc, exit from console, retry.

* ctrl A K to kill the window. 
* ssh -X pi@ulnoiotgw - to login


Tried log in to ELvin's Pi : password - ulnoiot
Get's the same error that Elvin gets when adding a new device. Tried several times but no success. 

