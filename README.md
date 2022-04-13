# modep-plugins
GuitarML Audio Plugins for MODEP on Raspberry Pi 3 

Meta repository to host plugin binaries for [MODEP](https://github.com/BlokasLabs/modep)

Binaries are located in the Releases section. 

These plugins have been tested using [Pi-Stomp](https://github.com/TreeFallSound/pi-stomp) hardware (Raspberry Pi 3 based). They should work for any Raspberry Pi 3 MODEP device. For running on Raspberry Pi 4 or an official MOD device, you will need to build specifically for your target.

## Deploy
You can deploy these plugins to your MODEP device using the following secure copy method.
```
# After turning on your device, copy the lv2 package to your device from another computer. 
# Note: Default password for patchboxOS is "blokaslabs"

scp -r <plugin.lv2> patch@patchbox.local:/home/patch  
ssh patch@patchbox.local:/home/patch  

# Once on the MODEP device..
sudo cp -r <plugin.lv2> /usr/modep/lv2/

# Reboot your device and use the virtual pedalboard to add the new lv2 plugin
```

## Build
If you are interested in compiling your own, or running on a target other than the Raspberry Pi 3, here are the links to the source code for the included plugins (see Readme's for build process):

 - [TS-M1N3](https://github.com/GuitarML/TS-M1N3/tree/mod) - TS-9 Guitar Pedal Emulator using Neural Networks
