## A quick guide to RCM and executing the fusee payload

### What you will need

- switch (duh)
- small piece of metal, a pin, breadboard wire etc. Any of these will do
- computer running linux (or osx?) 
- usb C to A, such as the ones that come with newer phones (e.g. the Oneplus 2 and newer)
- Fusee gelee and the fusee.bin payload. These can be found [here](http://www.memecpy.com) and [here](https://t.co/d5nCLNa7E5)

## Step 1 - RCM

### To prepare the switch for entering RCM we must power it down. Once powered down there are two pins on the right hand side of the switch that must be bridged, the last two pins towards the back of the switch (pins 9 & 10). This is where you use your piece of metal/pin or whatever. While those pins are bridged, hold down the volume up button and press the power button. The screen will remain blank, if it does not you have not entered RCM. Another way to check is to run 'lsusb' in the terminal and look for 'Nvidia Corp'

## Step 2 - Fusee gelee

### To launch the payload (fusee.bin) we must first setup the fusee gelee launcher. Once you have the files downloaded, CD into the directory and type 'make'. This will prepare intermezzo.bin which is nessecary to run fusee.bin. We then must sate the requirements of the script by installing pyusb. We can do this by entering 'sudo pip3 install pyusb'. Once that is finished we can proceed to run the payload

## Step 3 - The payload
### The fun part, seeing all those pretty numbers art ascii art on your switch! In the console type 'sudo python3 fusee-launcher.py fusee.bin' (side note fusee.bin should be in the same directory. If all is successful, you will see the reswitched logo on your switch!

## A (set of) Picture(s) paints a thousand words
[Image](https://imgur.com/a/lwrVnha)
# A switch

[Image](https://imgur.com/a/RATVhET)
# The pins on the right hand side of the switch (The right joycon rail)

[Image](https://imgur.com/a/bgZXGM7)
# The piece of metal I used

[Image](https://imgur.com/a/ry9tA3T)
# The piece of metal in the rail

[Image](https://imgur.com/a/auEKlQs)
# The final result!

### A massive thank you to the reswitched team, all credits go to them! <3 
