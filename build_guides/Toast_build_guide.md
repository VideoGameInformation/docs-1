---
title: Toast kit Build Guide
description: How to put together your new Toast solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5f2ef1b52bf5e8714a60f613
subcategory: medium
draft: false
tags: 
- 40%
- ergo
- kit
banner: https://i.imgur.com/EyfkJCX.jpg
thumbnail: https://i.imgur.com/EyfkJCX.jpg
---
### This guide is for *Toast* PCBs.

# Parts
### Required 
| Item | Count |
|------|-------|
| DIODESTYLE Diodes | 34 |
| PCB | 2 |
| Promicro-style or similar microcontroller | 2 |
| TRRS Jack | 2 | 
| TRRS Cable | 1 | 
| Reset Switch | 2 | 
| Choc Hotswap Sockets | 34 | 
| Choc Switches | 34 | 
| *Choc* Keycaps | 34 |


![components](https://i.imgur.com/1vWnwcP.jpg)

# Soldering
## Microcontrollers
**Orientation**: Both microcontrollers Left face up and right face down..
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/3FM5Rqy.jpg)
2. Place microcontroller Left face up and right face down.. 
![microcontroller placed](https://i.imgur.com/7sjplaF.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/My9TOHX.jpg)

## Solder-in switches
1. Insert switch into plate and then insert into pcb 
![switch placed](https://i.imgur.com/TZoPNbo.jpg)
2. Solder from the back
![switch soldered to the pcb](https://i.imgur.com/vwtX8p9.jpg)
![oled finished](https://i.imgur.com/9jKQixW.jpg)

## Misc.
### TRRS jacks
1. Position TRRS jack on front of PCB and secure with tape.
![trrs jack placed](https://i.imgur.com/kS3DWw3.jpg)
2. Apply solder to all four pins.
![trrs jack finished](https://i.imgur.com/cX3S0QM.jpg)
### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/pXrIgaS.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/GJd4UgH.jpg)



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