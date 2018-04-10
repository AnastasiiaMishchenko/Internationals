<a name= "top"></a>

* Lecture 01 19/03/2018

# Table of contents

1. [Introduction](#Introduction) 
2. [Things to do](#To_do_list)
3. [IoT basics](#IoT_Basics)
4. [Practical session](#Practical_session)
5. [Useful commands in addition](#Commands)

**Portfolio** <a name= "Introduction"></a>


**-Who?**
* Name: Chirantha Kanchana Peramunage
* Nationality: Sri Lankan 
* Academic qualifications: BSc (Hons) in Information Technology & MBA

**-Why?** 
* Because I want to specify my bachelors level IT knowledge into a certain technical domain.

**-Expectations?**
* Enhance my engineering related knowledge 
* Learn newest technologies, trends in domain 

**-Strengths?**
* IT knowledge 
* Team leading skills, responsible for the output of the project work. 

**-Weaknesses?**
* Lack of engineering related knowledge


**Things to do/ notes:** <a name= "To_do_list"></a>
* Tasks: make a matrix account,
* use text/ file based Kanban, not graphical. 
* Mark down cheat sheet. 
* Intelligent squared –for debate.

**IoT** <a name= "IoT_Basics"></a>
-What? System of physical things embedded with sensors, software, electronics and connectivity to allow it to better performance by exchanging info with other connected devices. 

**Domains:** 
* Healthcare 
* Smart cities
* Intelligent transport systems

**Devices:** 
* Smart door locks
* Smart Bluetooth trackers
* wireless home energy monitors
* Amazon dash buttons. 
* Adriano
* Alexa  


[Move to top](#top)

**Things completed on the practical session:** <a name= "Practical_session"></a>
* 1.Installation of raspaberry pi from a pre-installed image. Use class 10 SD card to flash. 
(Had to use specific configuration since it was MacOS to fix bugs before ssh,
.profile
display
)
(https://github.com/ulno/ulnoiot)

##### Steps:

1. Downloaded the pre-prepared Raspberry Pi image & wrote the image to a sd-card with https://etcher.io/ . (Use at least 8GB class-10 sd-card)

* Issue Faced: System not detecting the sd-card even after several trials.

* Solution: Used another card-reader and it worked fine.

* Challenge: It took a long time to do the first initialization. Was successful after several attempts. Didn't take down the notes as I was more involved with the practical work while Rosmary was recording the steps we followed. Later she helped with the notes. 

* Changed values:

* uiot_ap_name: smarthome
* uiot_ap_password: internetofthings123
* Put the sd-card into a Raspberry Pi 3 and powered it up. Also connected the LAN cable to it for internet.

* Connected the laptop and mobile to this wifi network.

* Connect to the ulnoiotgw via ssh ssh -X pi@192.168.12.1 and password ulnoiot. Upgraded it.

* Run the command ulnoiot upgrade to make sure that the latest version of ulnoiot is used.

* 2.Configure passwordless SSH access. 
(https://www.raspberrypi.org/documentation/remote-access/ssh/passwordless.md) 

* Issue Faced: Had to fix a bug in MacOS ssh

* Solution: .profile display :0

* Alternative Solution: Just Restart the Mac

3. Learning Markdown syntax for creating Git logs

[Move to top](#top)

**Useful commands in addition:** <a name= "Commands"></a>
* ctrl A Q for quit
* ctrl A K for killing
* sudo poweroff: to turn off the raspberry pi
* ctrl A N for new window
* ctrl O to switch between windows
* crtl C to inturrupt ongoing exectuitons

[Move to top](#top)
