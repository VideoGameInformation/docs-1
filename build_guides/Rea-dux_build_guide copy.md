---
title: Arachnophobe Solderable Kit Build Guide
description: How to put together your new Arachnophobe solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5ec9df84c6b834480de6c3d0
subcategory: medium
draft: false
tags: 
- 30%
- ergo
- kit
banner: https://i.imgur.com/5DycGVy.jpg
thumbnail: https://i.imgur.com/5DycGVy.jpg
---
### This guide is for *KEYBOARDNAME* PCBs.

# Parts
### Required 
| Item | Count |
|------|-------|
| PCB | 2 |
| Pro micro style or similar microcontroller | 2 |
| Reset Switch | 2 | 
| Choc Hotswap Sockets | 36 | 
| Choc Switches | 36 | 
| *Choc* Keycaps | 36 |
| Batteries  | 2 |


### Optional 
| Item | Count | 
|------|-------| 
| SMD Slide switch | 2 |


![components](https://i.imgur.com/fTfESW5.jpg)

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/Z64hG3T.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](https://i.imgur.com/H2EgxMI.jpg)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/bruZc04.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers CONTROLLERPLACEMENT.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/uZgkwZ7.jpg)
2. Place microcontroller CONTROLLERPLACEMENT. 
![microcontroller placed](https://i.imgur.com/3Yud5nz.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/uTcfsN9.jpg)

## Batteries
1. Fill the B+ hole with solder
2. Reflow the solder and insert the RED wire into the whole  
3. Repeat with B- hole
4. Reflow and insert BLACK wire 
![Battery finished](https://i.imgur.com/f1c1bpa.jpg)

## Misc.
### Power switch
1. Place power with with white slider facing outside the pcb
2. Apply solder to all pins.
![trrs jack finished](https://i.imgur.com/NkrSRAs.jpg)
### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/y9mN5iQ.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/nRpZJyN.jpg)


Now just put together the case and put on you favorite switches and caps and you're all done

![finished board](https://i.imgur.com/5DycGVy.jpg)


## Firmware

### QMK
In qmk this keyboard can be found under QMKKEYBOARDNAME.
To begin, follow the [QMK setup guide](https://docs.qmk.fm/#/newbs_getting_started). (if working from an existing installation, an [update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch) may be needed.) \
For flashing instructions, see [doc](https://docs.qmk.fm/#/newbs_flashing) or [video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)

### KMK / PEG
In Peg or KMK this keyboard can be found under KMKKEYBOARDNAME

Peg can be downloaded [here](https://peg.software/), and the quick start can be seen [here](https://peg.software/docs/Peg_Client/#quick-start-and-testing).

For Kmk can be downloaded [here](https://github.com/KMKfw/kmk_firmware) and the quick start can be seen [here](http://kmkfw.io/docs/Getting_Started#tldr-quick-start-guide)



## Extra
For questions, ask in [Boardsource Discord server](https://discord.gg/5qpqbgaTYz)