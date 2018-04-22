
### RGB light 
* d("rgb_multi", "rgb1", d7, 10) port, number of leds you want to activate.
* run()
* mqtt_send rgb1/set on 
* mqtt_send rgb1/rgb/set 2 blue
* mqtt_send rgb1/rgb/set red 


### Humidity/ Temperature Sensor. 
* sensoronboardled.init( Pin.OUT) this can be used to identify which node the device belongs to
* onboardled.on()
* onboardled.off()
* dmesg to check the devices connected
* d("dht22", "ht01", d7)
* run()

### Issues faced
* Problmes with nodered - http://192.168.12.1:1880/ is not loading properly. Tried 'ulnoiot upgrade' & restarting the Pi but it wasn't the solution. 
* Checked the wifi config on 'ulnoiot/etc/ulnoiot.conf' 
* tried pining and shows no packet losses. also the channel is set to random at ulnoiot/etc/ulnoiot.conf. Tired using a wifi analyser as well. It shows that the wifi has 2 channels, it just uses one though.
* seems like a problem with wifi or either the power supply for the pi.
* used a usb hub to power the pi on. 

# Problem with the power cable gave so much trouble 

### PhotoResistor
* analog, 3V, a0
* d("analog", "photo", threshold=50, precision=5)
* run()


### More issues faced
* nodered is not working properly and the console also shows weird behaviours when 2 devices are connected to the same pi.
* When I tried connecting alone to the pi, the console is working properly but the nodered mqqt inputs keep showing connecting status after deploying a flow.
* Thought of changing mqtt configurations, Tried mqqt manual connection establishment since I had no better options.
* useful links: https://github.com/node-red/node-red/issues/1135 , https://www.youtube.com/watch?v=AsDHEDbyLfg&t=186s, https://askubuntu.com/questions/222348/what-does-sudo-apt-get-update-do
* sudo apt-get update
* sudo apt-get upgrade
* sudo apt-get install mosquitto - it showed that it already has the lastest version of mosquito, so no luck there.
* Problem was the misconfiguration of the nodered mqtt port. After updating it from 1880 to 1883 it worked. 


#### Send Email nodered.

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





