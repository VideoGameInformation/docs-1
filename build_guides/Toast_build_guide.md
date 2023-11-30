---
title: Toast Solderable Kit Build Guide
description: How to put together your new Toast solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5ec9df84c6b834480de6c3d0
subcategory: medium
draft: false
tags: 
- 30%
- ergo
- kit
banner: https://i.imgur.com/KNumKXu.jpg
thumbnail: https://i.imgur.com/KNumKXu.jpg
---
### This guide is for *Toast* PCBs.

# Parts
### Required 
| Item | Count |
|------|-------|
| PCB | 2 |
| Promicro or similar microcontroller | 2 |
| TRRS Jack | 2 | 
| TRRS Cable | 1 | 
| Reset Switch | 2 |  
| Choc Switches | 34 | 
| *Choc* Keycaps | 34 |

![components](https://i.imgur.com/Yisk1DY.jpg)

# Soldering
## Microcontrollers
**Orientation**: Microcontrollers left face down Right face up.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/8LxUkzw.jpg)
2. Place microcontroller left face down right face up . 
![microcontroller placed](https://i.imgur.com/lzF0qxl.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/2Z5txqY.jpg)

## Misc.
### TRRS jacks
1. Position TRRS jack on front of PCB and secure with tape.
![trrs jack placed](https://i.imgur.com/YqZEU3D.jpg)
2. Apply solder to all four pins.
![trrs jack finished](https://i.imgur.com/1gmfKri.jpg)
### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/oxDQQ4k.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/1XTbbSG.jpg)

## Soldering in switches 
1. Insert a couple of the corner switches into the plate and then insert those switches into the pcb.
![Hot swap socket foot print soldered](https://i.imgur.com/rSOWlPT.jpg)
2. Flip the pcb over and solder in the switches from the back.
![Hot swap socket one pin soldered](https://i.imgur.com/NofAdfk.jpg)
3. Insert the rest of the switches and solder from the back.

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