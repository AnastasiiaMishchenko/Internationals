
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
