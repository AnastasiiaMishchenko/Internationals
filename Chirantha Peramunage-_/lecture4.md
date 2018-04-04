
Install 'Home Assistant', login :  hass --open-ui 

In the meantime tried the smart lock. Using below code. Saved the codes on autostart.py


run()

devices
devices["lock"]
devices["lock"].evaluate("on")
devices["lock"].evaluate("off")
wemos d1 mini - rfid-rc522 board

3v3 - 3.3V
d8  - sda
d7  - MOSI
d6  - MISO
d5  - SCK
d0  - RST
G   - GND

Add device with:
r=d("mfrc522","r",d0)

Write data to a mifare classic card:
r.write("mydata to write to reader")

Tried the function in of NodeRED:

var idArray= msg.payload.split(" ");

var id = idArray[1];

if(id === "dab93ad58c"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;

* Ignore the 'shell already in use' command. - esc, exit from console, retry.

* ctrl A K to kill the window. 
* ssh -X pi@ulnoiotgw - to login


