Install openhub homeassistance 
display and temperature sensor

tried 

import ulno_iot_relay as relay
relay.right()
relay.left()
but not working
asked mona and thomas
</a>

d("out", "lock", d0, "off", "on")
run()

devices
devices["lock"]
devices["lock"].evaluate("on")
devices["lock"].evaluate("off")

in the function in of NodeRED:

var idArray= msg.payload.split(" ");

var id = idArray[1];

if(id === "dab93ad58c"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;
