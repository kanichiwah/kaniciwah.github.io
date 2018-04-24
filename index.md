## A quick guide to RCM and executing the fusee payload

### What you will need

- switch (duh)
- small piece of metal, a pin, breadboard wire etc. Any of these will do
- computer running linux (or osx?) 
- usb C to A, such as the ones that come with newer phones (e.g. the Oneplus 2 and newer)
- Fusee gelee and the fusee.bin payload. These can be found [here](http://www.memecpy.com) and [here](https://t.co/d5nCLNa7E5)

## Step 1 - RCM

### To prepare the switch for entering RCM we must power it down. Once powered down there is a pin on the right hand side of the switch that must be grounded, the last pin towards the back of the switch (pin10). This is where you use your piece of metal/pin or whatever to ground pin 10 to the rail. While the pin is grounded, hold down the volume up button and press the power button. The screen will remain blank, if it does not you have not entered RCM. Another way to check is to run 'lsusb' in the terminal and look for 'Nvidia Corp'

## Step 2 - Fusee gelee

### To launch the payload (fusee.bin) we must first setup the fusee gelee launcher. Once you have the files downloaded, CD into the directory and type 'make'. This will prepare intermezzo.bin which is nessecary to run fusee.bin. We then must sate the requirements of the script by installing pyusb. We can do this by entering 'sudo pip3 install pyusb'. Once that is finished we can proceed to run the payload

## Step 3 - The payload
### The fun part, seeing all those pretty numbers art ascii art on your switch! In the console type 'sudo python3 fusee-launcher.py fusee.bin' (side note fusee.bin should be in the same directory. If all is successful, you will see the reswitched logo on your switch!

## A (set of) Picture(s) paints a thousand words
# A switch
![Image](/switch.jpg)

# The pins on the right hand side of the switch (The right joycon rail)
![Image](/pins.jpg)

# The piece of metal I used
![Image](/metal.jpg)

# The piece of metal in the rail
![Image](/metal_in_switch.jpg)

# The final result!
![Image](/final.png)


### A massive thank you to the reswitched team, all credits go to them! <3 
