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

