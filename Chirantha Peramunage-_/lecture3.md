
dmseg_  to check devices conncted

do the ulnoiot update : ulnoiot update
then initialize (didn't work in the first place since i was not inside the newly creatwd node 3. instead i was just on iot-chika folder

nodered toggle fuction: 

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

dmesg to check if its connected The device not getting powered up coz the code wemos d1 mini - rfid-rc522 board
3v3 - 3.3V d8 - sda d7 - MOSI d6 - MISO d5 - SCK d0 - RST G - GND

Add device with: r=d("mfrc522","r",d0)


To save the python commands:
copy, paste comands into copy/autostart.py in the respective node folder. Can deploy them later and let execute automatically. 
if the deply works, you can check it by mc, respective node-> command->
or cat("autostart.py") - It worked perfectly fine for node 3 but not the previous exercise since both node 1 and 2 were involved with the same activities. (Didn't know which to run first, does mqtt command also needs to be saved inside .py file)
