<a name="top"></a>
## Table of Contents  
[Q1: Who am I](#q1) </br>
[Q2: Movie time](#q2) </br>
[Q3: IoT definition](#q3) </br>
[Q4: Installation on Raspberry Pi from Pre-Prepared Image](#q4) </br>
[Q5: Remove the password](#q5) </br>
[Q6: First IoT Nodes](#q6) </br>
[Resources](#resources) </br>

<a name="q1"></a>
## Q1: Who am I?
**1.	Who are you**
* Anastasii Mishchenko
* Ukraine
* Energy Informatics
* Exchange year as an MC student (2016/17)
* Bachelor in Software Engineering 

**2. What do you expect**
* To get the understanding of home and build automation

**3. Strength and weaknesses**
- Strength: 
  - Goal oriented
  - Strict to the deadlines
- Weaknesses:
  - Postpone till the last minute
  
 <a name="q2"></a>
 ## Q2: Movie time
 **Film 1(Bing Bang Theory)**
 - Scenarios and application domains: 
   - Lighting
   - Privacy
  - Technologies:
    - Using the Internet
  - Feasibility: 
    - Yes (remote control)
  - Weirdness/crazyness (any concerns?):
    - Useless
    - Crazy
    - Not efficient usage of resources, more for fun
    
   **Film 2(Semens)**
   - Scenarios and application domains: 
     - Security and safety
     - Optamized usage of Energy
     - Energy cooperation with other fields except distribution
     - Dynamic statistic collecting and usage
     - Safe ecvacuation
     - Exchange information in a real time
     - Parking
   - Technologies:
     - Intelligent networks
     - Lighting and voice guidense 
     - Holographic displays
     - Smart grids
     - Sensors (on floors, security sensors)
     - Elevators
     - Electric cars
   - Feasibility: 
     - Not yet (Holographic display, elavators, sensors on a floors)
     - Possible (electric cars, smart grids, lighting and voice guidance)
   - Weirdness/crazyness (any concerns?):
     - No
     
   **Film 3(The Internet of Scrimps)**
   - Scenarios and application domains: 
     - Control lights
     - Serves drinks
     - Safety
     - Organize incoming calls and social medias
   - Technologies:
     - Voice control system
     - Social networks 
     - Internet
     - Cell phone
     - Tablet
     - Intelligent Fridge
   - Feasibility: 
     - Not yet (drinking maschine)
     - Yes
   - Weirdness/crazyness (any concerns?):
     - No
     - Yes (playing music on a kitchen supplies)
     
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q3"></a>
 ## Q3: IoT definition
 **Definition:**
 this is the concept of basically connecting any device with an on and off switch to the Internet (and/or to each other). It is the network of physical devices, vehicles, home appliances and other items embedded with electronics, software, sensors, actuators, and connectivity which enables these objects to connect and exchange data. Each thing is uniquely identifiable through its embedded computing system but is able to inter-operate within the existing Internet infrastructure.
 
 **Domains:**
 - Healthcare - Monitor hand hygiene compliance through IOT device and sensors to reduce transmission of Hospital Acquired Infections to patients.
 - Transport and logistics - Monitoring the logistics vehicles health to send alerts.
 - Retail - Remote interaction with products increase personalized shopping experience.
 - Insurance - Tracking clients' activity and offer discounts or rewards for healthy and safe behavior.
 - Banking - Smart payments.
 - Space - MARS Rover.
 - Construction and Real Estate - Smart home devices/locks/camera/security.
 - Farming - Tracking soil health and climate.
 - Industrial internet - Smart Fleet management and more sensors/data in Aircraft to avoid failures.
 - Wearables - Health monitoring and Fitness tracking.

 **Devices:**
 - Fitness trackers
 - Smart lock
 - Smart phoones
 - Smart grids
 - Bluetooth tracker
 - Wifi lighting
 - Thermostats
 - Light ballb
 - Home Energy Monitors
 
 **Useful materials:**
 <div align="center">
    <p>
      <a href="https://www.youtube.com/watch?v=QaTIt1C5R-M" target="_parent"><img src="http://img.youtube.com/vi/QaTIt1C5R-M/0.jpg" /></a></br>
      The Internet of Things: Dr. John Barrett </br>
      <a href="https://www.youtube.com/watch?v=_AlcRoqS65E" target="_parent"><img src="http://img.youtube.com/vi/_AlcRoqS65E/0.jpg" /></a></br>
      What is the Internet of Things? And why should you care?: Benson Hougland </br>
      <a href="https://www.youtube.com/watch?v=mzy84Vb_Gxk" target="_parent"><img src="http://img.youtube.com/vi/mzy84Vb_Gxk/0.jpg" /></a></br>
      The internet of things: Jordan Duffy </br>
    </p>
 </div>
 
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q4"></a>
 ## Q4: Installation on Raspberry Pi from Pre-Prepared Image
 1. Download the image.
 2. Check the sha256-cheksum of the image with a comand ```shasum -a 256 ulnoiot-pi.img.xz```.  </br>
 **Note:** I applied the command to the unpacked image which lead to the different checksum.
 3. Install the iTerm2 and XQuartz.
 4. In the file config.txt set up ```uiot_ap_name``` and ```uiot_ap_password``` to the ```International``` and ```MC509SS18```.  </br>
 **Note:** At first I changed the wrong parameters: ``uiot_wifi_name``` and ```uiot_wifi_password``` and set up the password which is shorter than 8 chracters. These leds to the result, that the WiFi was not in the list of wifis.
 5. Connect to the ulnoiotgw via ssh ```ssh -X pi@192.168.12.1``` and password ```ulnoiot```.
 6. Run the command ```ulnoiot upgrade``` to make sure that the latest version of ulnoiot is used.
 
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q5"></a>
 ## Q5: Remove the password
 1. Get to the ssh folder ```cd .ssh/```.
 2. Show the password ```cat id_rsa.pub```.
 3. Copy it to the clipboard. </br>
 **Note:** the first try failed because I did not copy the “ssh-rsa” as part of the key.
 4. Connect to the ulnoiotgw via ssh.
 5. Edit the ```authorized_key``` file with the command ```editor .ssh/authorized_keys```.
 6. Set the read and write permission ```chmod 600 .ssh/authorized_keys```. </br>
 **Note:** after the removing of the password, I still need to unter my keychan password to log in.
 
 <div align="right"><a href="#top">Back to top</a></div>
 
 <a name="q6"></a>
 ## Q6: First IoT Nodes
 1. Create a folder ```mkdir assignment_light```. 
 2. Copy the file ```cp –R /home/pi/ulnoiot/lib/system_template/ /home/pi/ulnoiot/assignment_light/```.
 3. Rename the directory “system_template” ```mv “system_template” “iot-light” ```.
 4. Rename the directory “node_template” ```mv “node_template” “onboard_blinker”```.
 5. Get into the derectory ```cd onboard_blinker```.
 6. Initialize a current node ```initialized```.
 7. Access the command prompt ```console```. </br>
 **Note:** after the performed commands the microcontroler was not detected, so it was unpluged and pluged in again, the problem was still the same. As a result, it turned out that the problem was in a cabel which is not working.
 8. ```sudo poweroff```  shut down the Raspberry Pi.
 
 <div align="right"><a href="#top">Back to top</a></div>

 <a name="resources"></a>
 ## Resources:
 1. [The Internet of Things IoT comes under which domain](https://www.quora.com/The-Internet-of-Things-IoT-comes-under-which-domain)
 2. [UlnoIoT](https://github.com/ulno/ulnoiot#installation)
 <div align="right"><a href="#top">Back to top</a></div>
