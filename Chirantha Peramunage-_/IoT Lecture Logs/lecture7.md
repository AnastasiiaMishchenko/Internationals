

<a name= "top"></a>

[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Chirantha%20Peramunage-_/Overview.md)

* Lecture 07 19/04/2018

### Table of contents

1. [RGB light](#rgb)
2. [Temperature/ Humidity sensor](#temp)
3. [Issues faced](#issues)
4. [Photoresistor](#photo)
5. [More Issues faced](#more)
6. [Send email NodeRed](#email)
7. [Raindrop / water sensor](#rain)
8. [Buzzer with button](#buz)
9. [Progress](#prog)
10. [Final scenario](#final)

### RGB light <a name= "rgb"></a>
* d("rgb_multi", "rgb1", d7, 10) port, number of leds you want to activate.
* run()
* mqtt_send rgb1/set on 
* mqtt_send rgb1/rgb/set 2 blue
* mqtt_send rgb1/rgb/set red 


### Humidity/ Temperature Sensor. <a name= "temp"></a>
* sensoronboardled.init( Pin.OUT) this can be used to identify which node the device belongs to
* onboardled.on()
* onboardled.off()
* dmesg to check the devices connected
* d("dht22", "ht01", d7)
* run()
* useful links - https://www.youtube.com/watch?v=ctoOsYETNZw

### Issues faced <a name= "issues"></a>
* Problmes with nodered - http://192.168.12.1:1880/ is not loading properly. Tried 'ulnoiot upgrade' & restarting the Pi but it wasn't the solution. 
* Checked the wifi config on 'ulnoiot/etc/ulnoiot.conf' 
* tried pining and shows no packet losses. also the channel is set to random at ulnoiot/etc/ulnoiot.conf. Tired using a wifi analyser as well. It shows that the wifi has 2 channels, it just uses one though.
* seems like a problem with wifi or either the power supply for the pi.
* used a usb hub to power the pi on. 

# Problem with the power cable gave so much trouble 

### PhotoResistor <a name= "photo"></a>
* analog, 3V, a0
* d("analog", "photo", threshold=50, precision=5)
* run()

[Move to top](#top)

### More issues faced <a name= "more"></a>
* nodered is not working properly and the console also shows weird behaviours when 2 devices are connected to the same pi.
* When I tried connecting alone to the pi, the console is working properly but the nodered mqqt inputs keep showing connecting status after deploying a flow.
* Thought of changing mqtt configurations, Tried mqqt manual connection establishment since I had no better options.
* useful links: https://github.com/node-red/node-red/issues/1135 , https://www.youtube.com/watch?v=AsDHEDbyLfg&t=186s, https://askubuntu.com/questions/222348/what-does-sudo-apt-get-update-do
* sudo apt-get update
* sudo apt-get upgrade
* sudo apt-get install mosquitto - it showed that it already has the lastest version of mosquito, so no luck there.
* Problem was the misconfiguration of the nodered mqtt port. After updating it from 1880 to 1883 it worked. 
* Even after that port fix, often see nodered webpage not working. Then if I poweroff the pi and again try to reconnect I see the below error msg at the first time. "connect to host ulnoiotgw port 22: Network is down". That didn't happen earlier.  
* Also if Rosmary's laptop is connected to the same wifi, the nodered prones to break. If it is just my laptop connected to the wifi, I can perfectly work on NodeRed. No idea why. 
* Every time when I try console_serial on rosy's node, I see this error, on console. 	
* Trouble to init mqtt. Exception: -2
* Trying to connect to mqtt broker. 	
* If I try the same for the second time it opens the console, and then if I check node red, it's already frozen after this. That doesn't happen when I work on my nodes. I don't see such an error. also node red works fine till rosy starts her work logging into same pi. 

[Move to top](#top)

#### Send Email nodered. <a name= "email"></a>

* useful links: 
* http://iotforum.advantech.com/discussion/92/how-to-use-nodered-to-send-the-email
* https://www.youtube.com/watch?v=qw3oKBp4rrQ
* https://nodered.org/docs/writing-functions#writing-a-function
* https://nodered.org/docs/user-guide/logging
* https://www.w3schools.com/jsref/jsref_parsefloat.asp

* var humidityValue = parseFloat(msg.payload);
node.warn("humidity float value " + humidityValue);
if(humidityValue > 1500)
{
    return msg;
}

* 

[Move to top](#top)

#### Raindrop/ water sensor <a name= "rain"></a>
* 3v, analog
* d("analog", "waterr", threshold=300, precision=10)
* run()
* useful links - https://www.youtube.com/watch?v=6RspaltqSVQ

```
var rain = parseFloat(msg.payload);
node.warn("rain float value " + rain); 

if(rain < 900)
    { 
    return msg;
    }
```
[Move to top](#top)

### Buzzer with the button  <a name= "buz"></a>
d(“output”, “buzzer”, d7, “off”, “on”)
d("button", "stop", d2, "depressed", "pressed" )
Tried to use it along with photoresistor.

* Fucntion

```
var photo = parseFloat(msg.payload);
node.warn("photo float value " + photo); 

if(photo > 700)
    { 
    msg.payload = "on";
    return msg;
    }
    
else
    { 
    msg.payload = "off";
    return msg;
    }
   
```
* Stop buzzer

```
if(msg.payload === "pressed")
{
    msg.payload = "off"
}
return msg;
```

[Move to top](#top)
    
### Progress <a name= "prog"></a>

#### (2 days before final presentation)

* Rosmery finally figured out her nodered issue. 
* Still there were rare hickups on console when we both work parallely. 
* I think ulnoiot framework should be more fine-tuned to avoid troubles when doing parallel programming. (Still it is a wonderful environment to work with) 
* I could complete all the functions that I planned to present as my part (Temp/ humidity sensor, raindrop sensor, photoresistor)
* Completed nodered flows. 
* Could integrate darksky weather api to nodered, data is showing in the dashboard although it doens't look as a good UI.
* email alert is receiving for exceeded humidity values.
* Desktop notification is showing for exceeding temperature values.
* Integrated rosmary's buzzer and the button for photoresistor for low values.
* Audio alert has been set up to notify raindrops (wetness level).
* Darksky weather api was not working after integration. 
* Completed recording the video of demonstrating scenarios. 

[Move to top](#top)

### Scenario presented. <a name= "final"></a>
"While being inside the house, Paul wants to know the weather status. He checks the dashboard to get the current weather. It shows the current temperature, humidity, amount of light having on his home and greenhouse. If there’s very less sunlight outside (>400 units), the buzzers inside the house will ring to notify the weather change. Then Paul or Rachel can go and turn off the buzzer using the button and also turn lights on inside the greenhouse. The light in the greenhouse is also automatically turned on.  If the temperature increases too much (>25 Celsius), he receives temperature status on his desktop. If the humidity value increases too much outside (>40%), Paul will receive an email notification to his personal mail mentioning the current humidity value."

[Move to top](#top)
