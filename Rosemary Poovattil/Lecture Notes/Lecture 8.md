[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)

# Table of contents

1. [Project 3 realization](#pro)
2. [Kanban](#kan)

## Project 3 realization<a name="pro"></a>

Worked along with Chirantha and Elvin at dorm. 

Tried many sensors namely:

- Auto Flash LED
d(“output”, “flash”, d0, “off”, “on”)

Connection: VCC to Port d0    

Extreme gnd to GND

**Issue**:Connection was tricky as the LED start flashing when connected to VCC and also it has two grounds.

![alt text](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Images/gnd.jpeg)


**Solution:** Connect VCC to any port so that it can be controlled


- RGB Strip
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



<a href="#top">Back to top</a>

### My Final Scenario 

Paul’s wife Rachel enters her room and the fancy Auto flash LED lights up as the motion sensor detects her. She gives a command to her phone and the phone place her Domino’s Easy Order. While waiting for the pizza she decides to test her newly installed security system for her Jewellery room. She walks by the room door and IR Obstacle sensor sets the alarm ON and also sends an email about the intrusion to her mobile. She deactivates the alarm by pressing a button. Then she uses her RF ID card and opens her Jewel locker and ‘Hello Rachel’ is displayed in the display.

Party mode:
1. Auto Flash LED


2. Pizza time- IFTT
“I want pizza”

3. IR Obstacle sensor + Active Buzzer + Button
d("input", "IR", d8, "safe" , "intruder") - VCC to 5V    
d(“output”, “buzzer”, d1, “off”, “on”) - VCC to 3V   
d("button", "stop", d2, "depressed", "pressed" )
Node red function:
if(msg.payload === "intruder")
{ msg.payload = "on";   }
return msg;


6. Sound sensor
Dual colour problem

4. Photo interrupter 
d("input", "PhotoInterrupt", d7, "interrupted", "safe")
VCC to 3V    
Its an analog o/p thus act accordingly






<a href="#top">Back to top</a>


## Kanban Management<a name="kan"></a>

I was in charge of Kanban Project management. Thus assigned Tasks an managed the same.

For full kanban details click [here](https://github.com/AnastasiiaMishchenko/Internationals/tree/master/Rosemary%20Poovattil/kanban)

<a href="#top">Back to top</a>


[Home](https://github.com/AnastasiiaMishchenko/Internationals/blob/master/Rosemary%20Poovattil/Portfolio.md)

