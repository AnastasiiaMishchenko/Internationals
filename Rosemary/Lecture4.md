# Table of contents

1. [Installation](#Install)
2. [Tasks:](#task)
3. [Lock](#lock)
4. [Senario for Project 2](#senario)
5. [Shopping list for Project 2](#list)
6. [Challenges](#challenge)
7. [Operate Lock using card reader](#lockcard)

 
## Installation <a name="Install"></a>

- Chirantha installed **Home Assistance** 
- Elvin installed **openHAB**

## Tasks: <a name="task"></a>
- [x] Lock
- [x] Operate Lock using card reader
- [ ] Operate using openhab
- [ ] Operate using homeassistant
- [x] Create senario for Project 2
- [x] Create shopping list
- [ ] Create Kanbanflow
- [x] Temperature sensor 
- [ ] Incoorporate display


### Lock<a name="lock"></a>
Connected the wemos d1 mini and the lock


Initialised and added the device to node2


**Command:**  Special command to connect the lock to the node
 ``` d("out", "lock", d0, "off", "on") ``` 
``` devices["lock"].evaluate("on") ```


Saved the commands to aurostart.py


**Result:** Success. Lock is opening and closing.


Tried mqtt to combilne card reader and lock
 ```mqtt_action n4/reader anychange xyz mqtt_send n1/lock/set```


**Result:** Failed. Not working
**Note:** 
- Tried different combinations but still not working
- Tried to operate lock using button, but not working
- Asked Mona and Thomas, they said they didn't use mqtt and shared the function for NodeRed

>var idArray= msg.payload.split(" ");
var id = idArray[1];
if(id === "dab93ad58c"){
    msg.payload = "on";
}else{
    msg.payload = "off";
}
return msg;


**Result:** Failed. Not working


**Issue:**
- Tried different combinations but still not working
- Cannot figure out if the procedure we are following is correct


## Senario for Project 2<a name="senario"></a>

- Group met and came up with a senario 
- I defined the __friend__'s basic details and shared the document 


## Shopping List for Project 2<a name="list"></a>

- I created a shared excel for the shopping list and stated a sample entry so that the group members can contrubute to the same
- Chirantha and Elvin met up to fill in more details to the shopping list

[Click here for Shopping List:](https://docs.google.com/spreadsheets/d/1SVmDE6H7TyPvkSrJAKrBFFbK5skZS80MD8QROaJ6owY/edit#gid=0)
 
 ## Challenges: <a name="challenge"></a>
 - All gropu mates could not meet up to make an exhaustive list
 - Several trials to operate Lock using card reader failed
 - Issues with Elvin's Py
 - Lot of time spend but no worthwhile result to show
 - Tried NodeRed for Led and Button with an idea to replace Led with the lock, but Not working
 
 ## Operate Lock using card reader<a name="lockcard"></a>
 
 Anastesia completed the task using the NodeRed and gave the Knowledge transfer
 
 

