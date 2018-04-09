

* Lecture 3 27/03/2018

# Table of contents
1. [Practical session: RFID reader](#RFID_Reader)

**1. Practical session: RFID reader** <a name= "RFID_Reader"></a>

* dmseg_  to check devices conncted

* do the ulnoiot update : ulnoiot update
* then initialize (didn't work in the first place since iI was not inside the newly created node 3. 
* instead I was just on iot-chika folder

* Commands 

nodered toggle fuction: 

```
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

```

* dmesg: to check if its connected 
* The device not getting powered up beacause wemos was not set up correctly.
* Wemos code:  wemos d1 mini - rfid-rc522 board
* 3v3 - 3.3V d8 - sda d7 - MOSI d6 - MISO d5 - SCK d0 - RST G - GND

* Add device with: r=d("mfrc522","r",d0)
* Special command to connect the device RC522(The card reader) to the node:  d("mfrc522","reader",d0,datasize=0) r=d("mfrc522","r",d0)


* Missed most of the in class practical session due to participating for an exam. 
* Gained some knowledge to configure it later on with the help of Rosemary. 

To save the python commands:
copy, paste comands into copy/autostart.py in the respective node folder. Can deploy them later and let execute automatically. 
if the deply works, you can check it by mc, respective node-> command->
or cat("autostart.py") - It worked perfectly fine for node 3 but not the previous exercise since both node 1 and 2 were involved with the same activities. (Didn't know which to run first, does mqtt command also needs to be saved inside .py file)
