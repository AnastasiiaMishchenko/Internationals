# Table of contents
1. dmesg to check if its connected
The device not getting powered up coz the code 
wemos d1 mini - rfid-rc522 board

3v3 - 3.3V
d8  - sda
d7  - MOSI
d6  - MISO
d5  - SCK
d0  - RST
G   - GND

Add device with:
r=d("mfrc522","r",d0)

upgrade
reinitialize
Chika node3
Special command to connect the device RC522(The card reader) to the node
**command:** d("mfrc522","reader",d0,datasize=0)
datasize is optional but if initialized as 0 we can detect anything, otherwise it is set to the default value.
Got the result- Read two sample cards.
