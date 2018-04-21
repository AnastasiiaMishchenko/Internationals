
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
* Problmes with nodered - http://192.168.12.1:1880/ is not loading properly. Tried 'ulnoiot upgrade' & restarting the Pi but it wasn't the solution. 
* Checked the wifi config on 'ulnoiot/etc/ulnoiot.conf' 
* tried pining and shows no packet losses. also the channel is set to random at ulnoiot/etc/ulnoiot.conf. Tired using a wifi analyser as well. It shows that the wifi has 2 channels, it just uses one though.
* seems like a problem with wifi or either the power supply for the pi.
* used a usb hub to power the pi on. 




