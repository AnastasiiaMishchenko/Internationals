[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)

# Table of contents

1. [Project 3 realization](#pro)
2. [Project Integration](#int)
3. [Kanban](#kan)
4. [Final Project Presentation](#final)
5. [Total Experience ](#expe)


## Project 3 realization<a name="pro"></a>

Worked along with Chirantha and Elvin at dorm.

**Big Mistake**: Unknowgly created an infinite loop in NodeRed which always resulted the system to stop working. 


> The input and the output Mqtt nodes were given idententical names i.e, ``status``instead of ``set``


Wasted a lot of time on it and finally started trying all sensors and wrote down the NodeRed program logic offline. 


![alt text](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Images/nodeRed.png)



**Solution**: On the last day at midnight I noticed that every time I give an input to the output Mqtt NodeRed get stuck and thus I found the Mistake ... 



#### Tried many sensors for the possibility to use in Project, namely:

- 1. Auto Flash LED

d(“output”, “flash”, d0, “off”, “on”)

Connection: VCC to Port d0    

Extreme gnd to GND

**Issue**:Connection was tricky as the LED start flashing when connected to VCC and also it has two grounds.

![alt text](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Images/gnd.jpeg)


**Solution:** Connect VCC to any port so that it can be controlled



- 2. RGB Strip
Observed the different pattens and their output. Tried to control the colours selectively using NodeRed. But always having trouble with NodeRed.

Some observations and codes tried 

> Yellow (255,255,0)
> Message type is - string[9]
> (0, 0, 0) (255, 255, 255)
> var blue = "(255, 255, 255)";


> var i = msg.payload; // for example 20

> var str = i.toString(2);

> var str = msg.payload;

> var res = str.slice(1, 2);

> msg.payload = blue;

> return msg;




- 3. IR Obstacle sensor

``d("input", "IR", d8, "safe" , "intruder")``

Connect VCC to 5V 

Changed the Potentiometer value using a screw-driver to control the distance range covered




- 4. Button

``d("button", "stop", d2, "depressed", "pressed" )``




- 5. Active Buzzer

``d(“output”, “buzzer”, d1, “off”, “on”)  ``

Connect VCC to 3V for better control




- 6. Passive Buzzer

Decided to use Active buzzer as its better to control




- 7. Sound sensor

Very Sensitive to small sounds.

Not ideal to use for project




- 8. Photo interrupter 

``d("input", "PhotoInterrupt", d7, "interrupted", "safe")``

VCC to 3V    

**Note**: It gives analog o/p 




- 9. Dual colour LED

Not very controllable(colour).

Not ideal to use for project



- 10. Humidity/ Temperature Sensor.

`` d("dht22", "ht01", d7)``



- 11. Photo diode

It gives an analog output
Connect VCC to 3V

``d("analog", "photo", threshold=50, precision=5)``



- 12. Raindrop sensor

It gives an analog output
Connect VCC to 3V

``d("analog", "waterr", threshold=300, precision=10)``


<a href="#top">Back to top</a>


Worked along with Chirantha for the weather related sensors. The issues and details is documented [here](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Chirantha%20Peramunage-_/IoT%20Lecture%20Logs/lecture7.md#humidity-temperature-sensor-). The details on the issues


**Issue:** Tried combination of motor and belts to come up with a rotating Closet system for the dressing room in the senario, but gave up the idea since:
- there were lot of issues with the NodeRed and Pi to concentrate on.
- No ideal accessories 

* But it was fun playing with multiple motors *


<a href="#top">Back to top</a>

### Decided to use IR Obstacle sensor + Active Buzzer + Button as a security system

> Node red function:

> if(msg.payload === "intruder")

> { msg.payload = "on";   }

> return msg;

**Note** : Chirantha and Anastasiia used **Active Buzzer** + **Button** as alarm system and the system to stop the alarm respectively, for their project. 

We tried to use voice command to stop the alarm but since the noise of Buzzer is high the Snowboy Hotword could not be detected.


<a href="#top">Back to top</a>

### Kodi

Worked with Elvin on Kodi.

**Issue:** Elvin came up with many solutions and things but we still struggled with the JavaScripting and checked many documents and videos but none were specific.

**Help:** Andreas gave a better example of Kodi using NodeRed, which gave me a better idea on how to work with Kodi in NodeRed, but didn't include in the final project Scenario as our Video was already recorded. 


<a href="#top">Back to top</a>


## Project Integration<a name="int"></a>

Integrating all nodes under one Pi and recording the Video took us so much time and the whole group stayed back at the university almost till midnight !

**Notes:**
- Anastasiia's database inclusion was impressive and I wanted to know the details, so checked her GitHub
- Wanted to include IFTTT and Email to my scenario but didn't as we were short of time 


## Kanban Management<a name="kan"></a>

I was in charge of Kanban Project management. Thus managed and reassigned the tasks.

![alt text](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/kanban/8.png)


For full kanban details click [here](https://github.com/AnastasiiaMishchenko/Internationals/tree/master/Rosemary%20Poovattil/kanban)


<a href="#top">Back to top</a>


### My Final Scenario 

Paul’s wife Rachel enters her room and the fancy Auto flash LED lights up as the motion sensor detects her. She gives a command to her phone and the phone place her Domino’s Easy Order. While waiting for the pizza she decides to test her newly installed security system for her Jewellery room. She walks by the room door and IR Obstacle sensor sets the alarm ON and also sends an email about the intrusion to her mobile. She deactivates the alarm by pressing a button. Then she uses her RF ID card and opens her Jewel locker and ‘Hello Rachel’ is displayed in the display.


**Issue:** Dominos does not deliver here! so gave up that plan too : (


<a href="#top">Back to top</a>


## Final Project Presentation <a name="final"></a>

### ENI team

**Comment:** Liked the use of Kodi and Kettle

### MC Guys

**Comment:** Liked their coordination and communication with each other. Liked how they played with Hue lamp


### Internationals

**Comment:** Could have included a narration while taking the video but the other team mates didn't like the idea.


## Total Experience <a name="expe"></a>

- Initially thought it was a lot of work and pressure
- Lack of resources at hand and lot of unexpected issues made it harder
- But as we found out solutions and things started getting smoother
- I wish I could work with it more
- For one week day and night we were working on only this
- My roommate was really facinated by the things working and wanted to study the same
- Recomented this course to my friend who joined MC next Summer
- Worth the effort and will definitely automate something at home 
- In the end giving away the sensor kit and Pi was SAD : (

![alt text](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Images/IMG_20180426_104533419.jpg)


<a href="#top">Back to top</a>

[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)

