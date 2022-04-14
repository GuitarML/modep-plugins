# modep-plugins
GuitarML Audio Plugins for MODEP on Raspberry Pi 3 

This is a meta repository to host plugin binaries for [MODEP](https://github.com/BlokasLabs/modep)

![app](https://github.com/GuitarML/modep-plugins/blob/main/pedalboard.jpg)

## Download

Binaries can be downloaded from the [Releases section](https://github.com/GuitarML/modep-plugins/releases).

These plugins have been tested using [Pi-Stomp](https://github.com/TreeFallSound/pi-stomp) hardware (Raspberry Pi 3 based). They should work for any Raspberry Pi 3 MODEP device running 32-bit PatchboxOS. For running on Raspberry Pi 4 or an official MOD device, you will need to build specifically for your target.

## Deploy
You can deploy these plugins to your MODEP device using the following secure copy method.
```
# After turning on your device, open a terminal and use the following commands 
#    to copy the lv2 package to your device from another computer.
# Note: Default password for patchboxOS is "blokaslabs"

scp -r <plugin.lv2> patch@patchbox.local:/home/patch  
ssh patch@patchbox.local:/home/patch  

# Once on the MODEP device..
sudo cp -r <plugin.lv2> /usr/modep/lv2/

# Reboot your device and use the virtual pedalboard to drag an drop the new plugin into your pedalboard.
```

## Build
If you are interested in compiling your own, or running on a target other than the Raspberry Pi 3, here are the links to the source code for the included plugins (see Readme's for build process):

 - [TS-M1N3](https://github.com/GuitarML/TS-M1N3/tree/mod) - TS-9 Guitar Pedal Emulator using Neural Networks
 - [DarkStar](https://github.com/GuitarML/DarkStar) - Emulation of a HT40 amp in overdrive using Neural Networks

## Info
See [TreeFallSound](https://www.treefallsound.com/) for more info on the Pi-Stomp and how to build one.

See [blokas.io](https://blokas.io/modep/) for more info about MODEP, the MOD DUO emulator.

See [Mod devices wiki](https://wiki.moddevices.com/wiki/Main_Page) for more info on MOD-Devices and how to build plugins using the [mod-plugin-builder](https://github.com/moddevices/mod-plugin-builder).
