## Project presentation - 1 mc guys.

1. Smart fridge 
2. central control system
3. several central control panels 
4. focus on heating and climate 
5. also lightning and shutter - smart garden poles , homematic wireless switch actuator 
6. Securtiy and surveilance - all products from Homematics, ASE encryption 
7. Entertainment - 
8. Central control unit - 

Homematic - well presented. complete solutions.

* better workload break down between team members. 


## Project presentation - 2 Richy's smart home.

1. No security  - motion detectors. 
2. Loxone - main component  
3. dimmers - lightning
4. Touch pure tree, value actuator tree. 
5. IR control air, Remote air
6.smart socket, smart meter IR interface air
7. Intercom , NFC code touch tree. 
8. weatherstation tree, tubular motor. 
9. pool - aquastar air 2, Loxone cable
10 . miniserver, relay extension 
11. Base extension, Tree extension 
12. other components - Wallbox KEBA, heat pump viessmann

* More details about the devices. 


recommendations - coffee machine, smart cooking devices. 


 #### Problems faced - 
* the top tab and the buttons below on the bash is getting freezed from time to time. 
*


## Install Snowboy
* https://snowboy.kitt.ai
* https://github.com/kitt-ai/snowboy
* https://www.youtube.com/watch?v=N-SDrN4G4lE
* https://brew.sh - install homebrew 
* http://docs.kitt.ai/snowboy/
* command - /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" on terminal
* password - Mac user pw
* Then - brew install swig portaudio sox
* Since I have a python verson above I guess I don't need to install pip. Anyways, the command 'pip install pyaudio' didn't work on my command prompt. Upgrade command 'pip install -U pip' also didn't work for me. 
* Plug the microphone and run rec t.wav on the bash. It will show some waves when it recognizes voice. 
* Trained and recorded a hotward 'Internationals' on snowboy - https://snowboy.kitt.ai/hotword/20562
* In terminal open Python - type Python
* Did a mistake by skipping the pip installation because it was confusing in the intitial tutorial. A new website helped me with installation and better understanding - https://ben.fogbutter.com/2016/02/15/installing-pip-on-os-x.html
* Running the demo was not working fine with the command - python demo.py snowboy.pmdl
* Tried creating a demo.py on my desktop and access it through terminal but no luck. 
* Forgot to download the github repository. Downloaded it and accessed the filepath. exmaples/python
* Unable to complete installation as 'pip install pyaudio' command didn't work yet. 
* Workaround - running below commands again. - 'curl https://bootstrap.pypa.io/get-pip.py > get-pip.py' & then 'python get-pip.py --user'
* Still it shows 2 errors on command prompt. Errors listed below.
* matplotlib 1.3.1 requires nose, which is not installed.
* matplotlib 1.3.1 requires tornado, which is not installed.
* Then tried installing nose & tornado components but still it shows they are not being installed even after a successfull installation message. 
* Tried the same accessing bash profile 'source ~/.bash_profile' but no success. 
* Gave up on installing snowboy as it took so much time than expected. Also Anastasia could successfully install it. So all agreed upon using her installed one for voice commands if needed. 
