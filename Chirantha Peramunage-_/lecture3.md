
<a name= "top"></a>
* Lecture 3 27/03/2018

# Table of contents
1. [Practical session: RFID reader](#RFID_Reader)
2. [Issues Faced](#issue)
3. [Autostart.py configuration](#Auto)
4. [Debate Preparation](#debate)

**1. Practical session: RFID reader** <a name= "RFID_Reader"></a>

* dmseg_  to check devices conncted

* do the ulnoiot update : ulnoiot update
* then initialize (didn't work in the first place since iI was not inside the newly created node 3. 
* instead I was just on iot-chika folder

#### Commands 

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

[Move to top](#top)

**2. Issues Faced** <a name= "Issues"></a>

**Issue:** When two devices connected in series with the Py, cannot identify which device is being detected by the Py

**Solution**: 

* Ulnoiot help- help()

* Syntax: initialize [serial_port] [noflash] [noupdate]

**Issue** Since I was absent for most of the practical session, it was difficult to catchup things up to speed.

**Solution**: Rosemary helped with the stuff that she has an idea about. Still there were lot more to realize by team members and it took a while to finish up the work as priority was given to the debate preparation. 

[Move to top](#top)

**3. Autostart.py configuration** <a name= "Auto"></a>

* To save the python commands: copy, paste comands into copy/autostart.py in the respective node folder. 
* Can deploy them later and let execute automatically. 
* if the deply works, you can check it by mc, respective node-> command->
* or cat("autostart.py") - It worked perfectly fine for node 3 but not the previous exercise since both node 1 and 2 were involved with the same activities. (Didn't know which to run first, does mqtt command also needs to be saved inside .py file)
* Asked about that doubt from the lecturer - Reply- mqtt does not involve with python. 

##### Resources: https://www.youtube.com/watch?v=Yzys-EiLPsk&t=2s 

[Move to top](#top)

**4. Debate Preparation** <a name= "debate"></a>

* Topic- Everybody should use Home Automation. True or False?

* Tasks done - 

##### 1. Team gathered up first and decided on the topics. 

* Specific Topics suggested. 

1. After reading this article about mobile apps which combine security and home functionality, so I would like to discuss the security (remotely monitoring) and the installation of the system.
2. Also, we would like to discuss, the market impact of home and building automation. Power consumption by energy saving devices. (Article: “Home automation market growth demand and key players to 2015-2025”).
3. In “Roseville Eskaton deploys home automation tablets for residents” article, it was stated that senior living apartments will turn into smart homes allowing each resident to manage their day-to-day activities. That’s why we want to discuss learning curve and easiness of usage for everyone.
4. Variation of the devices which provides security, flexibility, and centralized control.

* General Topics suggested. 

1. Security
2. Energy efficiency.
3. Compatibility and flexibility of the systems.
4. Costs and savings.
5. Environmental impact.
6. Reliability.
7. The complexity of the system.
8. Entertainment.
9. Monitoring/ device management.

##### 2. Sent the compiled topics for approval on Matrix. 

##### 3. Created a Kanban flow of the tasks to track the debate related tasks that we did. 

* Link to the Kanban dashboard - https://kanbanflow.com/board/1ve7FZCc

##### 4. Researched and prepared personal statements for 3 mins long.
##### 5. Did mock debate in the next team meeting. 
##### 6. Finally did an actual debate for recording. 
##### 7. Later on researched and prepared personal statements for 5 mins long. 

#### For the group debate I was the Con team. Here are some topics that I discussed during the debate: 

1. Security

* High installation & maintainance cost.
* Video survellance privacy issues.
* Vulnarability to hackers / cyber attacks. 
* Smart devices recording sensitive data.

2. H&B automation market growth/ demand.

* Impact from security and high costs. 
* Changes in lifes styles of commen people. 
* High dependability. 
* market diversification in the world. 

3. IoT for elderly people.

* High costs for specific implementations.
* Complex technology for them to understand. 
* Learning curve. 

* Additionally - Rules and regulations regarding devices. 
* Peace of mind regarding privacy. 
* Useless innovations

* Link to youtube video: https://www.youtube.com/watch?v=1JOWhVgcfnY&feature=em-share_video_user

[Move to top](#top)
