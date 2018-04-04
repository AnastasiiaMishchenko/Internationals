
Install 'Home Assistant', 

In the meantime tried the smart lock. Using below code. Saved the codes on autostart.py

d("out", "lock", d0, "off", "on")
run()

devices
devices["lock"]
devices["lock"].evaluate("on")
devices["lock"].evaluate("off")

Tried the function in of NodeRED:

var idArray= msg.payload.split(" ");

var id = idArray[1];

if(id === "dab93ad58c"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;

* Ignore the 'shell already in use' command. 
