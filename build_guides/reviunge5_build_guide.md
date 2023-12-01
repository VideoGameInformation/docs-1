---
title: Reviung5 Build Guide
description: How to put together your new Reviung41 solderable kit.
author: gtips
source: https://reviung.com/build-guide/391/
product_link: https://boardsource.xyz/store/5f2ef1b52bf5e8714a60f613
subcategory: medium
draft: false
tags: 
- 40%
- ergo
- kit
banner: https://reviung.com/wp-content/uploads/2021/06/reviung5-1.jpg
thumbnail: https://reviung.com/wp-content/uploads/2021/06/reviung5-1.jpg
---

# REVIUNG5 Build Guide
## Kit accessories
-----

| name                      | number | remarks                                  |
|---------------------------|--------|------------------------------------------|
| PCB                       | 1      | Main PCB                                 |
| top plate                 | 1      | acrylic                                  |
| bottom acrylic plate      | 1      | acrylic                                  |
| ProMicro protection plate | 1      | acrylic                                  |
| acrylic spacer            | 3      | acrylic spacer                           |
| spacer                    | 3      | metal spacer                             |
| M2 screw (long)           | 3      | For top/bottom plate connection          |
| M2 screw (short)          | 6      | For connecting ProMicro protection plate |
| M2 nut                    | 3      | For connecting ProMicro protection plate |
| rubber foot               | 4   | For bottom plate                         |
| Diode (1N4148)            | 5   |                                          |
| Tact switch               | 2      | SMD/TH Use either one                    |

## Required parts other than the kit
-----
MicroUSB cable 1 for keyboard and PC connection

| name           | number | remarks                                                                                                   |
|----------------|--------|-----------------------------------------------------------------------------------------------------------|
| ProMicro       | 1      | You can purchase a set with the console at  Yusha Kobo . You can purchase ProMicro alone at TALP KEYBOARD |
| Cons through   | 2      | (Spring pin header 12P) Available at Yusha Kobo and TALP KEYBOARD                                         |
| key switch     | 5 – 4  | MX compatible  You can purchase from Yusha Kobo and TALP KEYBOARD                                         |
| Keycap (1U)    | 5 – 4  | MX compatible  You can purchase from Yusha Kobo and TALP KEYBOARD                                         |
| MicroUSB cable | 1      | For keyboard and PC connection                                                                            |

## Options (sold separately)
| name                | number | remarks                                                                 |
|---------------------|--------|-------------------------------------------------------------------------|
| LED (WS2812B)       | 0-4    | You can purchase it at Yusha Kobo .                                     |
| rotary encoder      | 0 – 1  | Alps EC12 series compatible                                             |
| Diode (1N4148W SMD) | 1      | An SMD version can be used in place of the TH diode included in the kit |

## assembly
---------

TThe general flow is as follows.

1. First, prepare ProMicro.
2. Solder the reset switch.
3. Option: Solder the LEDs one by one while checking their operation.
4. Solder the diode.
5. Attach the ProMicro protective cover to the top plate.
6. Attach the switch to the top plate.
7. Optional: Solder the rotary encoder.
8. Solder the switch.
9. Attach the bottom plate to the main body.
10. Attach the keycap and you're done.


![PCB](https://reviung.com/wp-content/uploads/2021/07/R5_01-1280x855.jpg)

PCB front

![PCB](https://reviung.com/wp-content/uploads/2021/07/R5_02-1280x855.jpg)

Back of PCB

## Prepare to connect ProMicro and PC.
-------
Solder the con-through (spring pin header) to the ProMicro. (Recommendation)

Alternatively, solder a pin header to the ProMicro.

### The con-through has a recommended mounting orientation.

The con-through has a side with holes and a side without holes , and there are also sides with holes closer to the pin and those with holes farther away.

When mounting, make sure that both small windows face the same direction , and insert the hole closer to the pin into ProMicro.

Insert a conthru into the side where the ProMicro chip is on and solder it from the other side.

Only the ProMicro and con-through sides need to be soldered.
PCB and con-throughs are not soldered.

![controller](https://reviung.com/wp-content/uploads/2020/01/Pro-Micro-1-1280x855.jpg)

![back of controller](https://reviung.com/wp-content/uploads/2020/01/Pro-Micro-2-1280x855.jpg)

### When using a pin header
------
If you are using a regular pin header instead of a 
con-through, stick the pin header into the surface where the ProMicro chip is mounted and solder it.

Also, if you use a pin header, solder the PCB side as well.

## Soldering the reset switch

Next, solder the reset switch to the PCB.

Solder the tact switch to the place where "RESET" is written on the back of the PCB.


![reset switch on pcb](https://reviung.com/wp-content/uploads/2021/07/R5_03-1280x855.jpg)


![clipping reset switch](https://reviung.com/wp-content/uploads/2021/07/R5_04-1280x855.jpg)

Attach ProMicro to the PCB, connect it to the PC with a USB cable, and prepare to write the firmware.

# Write firmware to ProMicro

## When using REMAP
----
Write the firmware using REMAP ( remap-keys.app ).

1. Start your browser (chrome) and open the REVIUNG53 firmware page in REMAP.
2. Connect ProMicro to your PC.
3. Press the RESET switch that you soldered earlier to prepare for writing.
4. Click "FLASH" in "reviung53_via.hex" on the page to write the firmware.

Once writing is complete, disconnect the USB cable from the PC.

## When using QMK Firmware
-----
Build a build environment on your PC

Download and install QMK Toolbox.

    https://github.com/qmk/qmk_toolbox/

    download
    https://github.com/qmk/qmk_toolbox/releases

Please clone and build the firmware from below.

    https://github.com/qmk/qmk_firmware


If you clone QMK firmware, the directory is "qmk_firmware/keyboards/reviung53/".
The keymap is "default" or "via".

Please refer to the QMK Firmwware documentation for details on how to build.

    QMK Firmwware documentation
     https://docs.qmk.fm/
 
Compiling the default keymap    outputs a file qmk compile -kb reviung53 -km default with  ..hex

    qmk compile -kb reviung53 -km default
 
 Once writing is complete, disconnect the USB cable from the PC.

# [Optional] Solder the LEDs one by one while checking their operation.
-------
Let's solder the optional LED (WS2812B).

If you do not want to add LEDs, please skip this step .

![LED](https://reviung.com/wp-content/uploads/2020/01/WS2812B-1280x855.jpg)

REVIUN5 uses a 5mm size chip called [WS2812B].

Use a soldering iron with a temperature control function to work at a temperature of about 320℃.
(If the temperature is too low, it will take a long time for the solder to melt, making the work difficult.)
Also, if the LED is installed outside of the installation mark, it will no longer shine, so work carefully.

First, there is an LED installation pad marked "RGB1" in the upper right corner of the back of the PCB, so start attaching the LEDs in order from here.


![LED on the PCB](https://reviung.com/wp-content/uploads/2021/07/R5_05-1280x854.jpg)

Attach the LEDs on the back of the PCB in clockwise order from "RGB1" to "RGB4".

 

1. Apply flux to the pad on the back of the PCB.

2. Next, pre-solder only one of the four pads.
If you are right-handed, it will be easier to work if you pre-solder to the bottom right pad)

It's like applying a small amount of solder to a warmed iron tip and applying it to the pad.
If you have applied too much solder, apply a dry (wipe off the solder) soldering iron to the solder on the pad to remove the excess solder.

3. Apply flux to the preliminary solder.

![LED pad saldered](https://reviung.com/wp-content/uploads/2021/07/R5_06-1280x855.jpg)

Four. Use tweezers to align and place the LED (WS2812B) so that the GND mark on the PCB matches the VSS of the LED.
(Place it so that the missing △ position on the LED matches the GND▲ mark on the PCB.)

Quoted from WS2812B datasheet ![led diogram](https://reviung.com/wp-content/uploads/2020/01/WS2812B-V5_V1.jpg)
![led placed](https://reviung.com/wp-content/uploads/2021/07/R5_07-1280x855.jpg)


 

5. While holding the LED in place with tweezers, apply the soldering iron to the preliminary solder from earlier to fix the LED.

At this time, work for 2 to 3 seconds so as not to apply too much soldering iron.
Also, be careful not to let the tip of the iron touch the LED body.

Look at the PCB from the side and check if the LED contacts are floating.
If the LED contacts fit perfectly on the PCB, it is a success.

If the LED position shifts from the four corner marks (silk/print) or is not properly fixed, wait for the LED to cool down before recovering.

![LED saldered](https://reviung.com/wp-content/uploads/2021/07/R5_08-1280x855.jpg)

6. Next, solder the other pads and LED.

Place a small amount of solder on the "stick" and solder it to the pad.
At this time, apply the tip of the iron as if you were warming a pad on the PCB, and work for 2 to 3 seconds.

 

After soldering the four pads, clean the flux with flux cleaning solution.

![LED working](https://reviung.com/wp-content/uploads/2021/07/R5_09-1280x855.jpg)

After soldering the "RGB1" LED, connect ProMicro to the PC using a USB cable and check if the LED lights up.
If it glows red, it's a success.

If it does not light up, the following may be the cause.

1. Poor soldering
2. The position has shifted
3. LED is damaged
4. Forgot to write firmware

 When recovering, be sure to disconnect the USB from the PC before proceeding.

In the case of poor soldering, it may be difficult to tell visually.
Try reheating the solder on the LED and pad.
After applying flux again to the four solder spots on the LED that do not glow, apply the soldering iron to each spot for about 2 seconds to melt the solder again.
After working on one spot, wait for the LED to cool down, then reheat the solder on the next pad in the same way.

If the LED is misaligned or floating, don't panic and try to recover the soldering.
Apply flux again and work for 1-2 seconds without applying too much soldering iron.

If the LED is damaged, suck up the solder with a solder wick, heat the LED from the sides with a soldering iron set to about 320 degrees, and carefully peel it off with tweezers.
At this time, if you forcefully pull the LED upwards, the pad may come off.
Remove the LED from the PCB by sliding it sideways with a soldering iron and tweezers or lead pliers, or by carefully breaking the LED to avoid damaging the PCB.

 

Once the "RGB1" LED is on, next work on the "RGB2" LED and check if it lights up, then work in numerical order up to "RGB10".

Be sure to disconnect the USB before soldering. There is a risk of short circuit.

 

Make sure all RGB LEDs are lit.

![All LEDS working ](https://reviung.com/wp-content/uploads/2021/07/R5_10-1280x855.jpg)

# solder the diode

There is a diode mounting position near the switch mounting position, so we will solder at 5 locations.

The direction in which the diode is installed is determined.
Install the diode so that the "|" mark on the chip component faces the "|" side of the diode mark "▹|" on the PCB.

Solder while paying attention to the direction of installation.
Work at a soldering iron temperature of about 320°.

![diode](https://reviung.com/wp-content/uploads/2021/07/R5_11-1280x855.jpg)


1. First, bend the diode legs.

2. Next, insert the diode legs into the PCB and solder them. (Place it on a suitable stand or turn it over and solder it.)
![one pad saldered](https://reviung.com/wp-content/uploads/2021/07/R5_12-1280x855.jpg)

![one pad saldered](https://reviung.com/wp-content/uploads/2021/07/R5_13-1280x855.jpg)

3. After soldering all the diodes, turn it over and cut out the legs of the diodes with nippers.

![one pad saldered](https://reviung.com/wp-content/uploads/2021/07/R5_14-1280x855.jpg)

![one pad saldered](https://reviung.com/wp-content/uploads/2021/07/R5_15-1280x855.jpg)

There may be cracks in the cut section, so lightly reheat the section with solder.

After soldering, remove the flux with flux cleaning solution.


## Check operation
------  
At this point, connect it to your PC and check its operation.

Connect the ProMicro attached to the PCB to the PC using a USB cable, and short-circuit the terminal hole of the switch with tweezers or a cut-off diode leg to see if a key can be input.
>If you use the REVIUNG41 firmware, you can check the TAB, Q, W, E, and R inputs from the right switch on the back of the PCB.

> With the REVIUNG5's default firmware, the right switch on the back of the PCB allows you to control volume (down), previous song, play/stop, next song, and volume (increase).

![](https://reviung.com/wp-content/uploads/2021/07/R5_16-1280x855.jpg)

If some keys are not input, please check the following.

・Direction of diode

・The diode is correctly soldered

 

If all keys are not input, please check the following.

・Firmware has been written

・ProMicro is correctly attached to the PCB

・ProMicor and con-through are properly soldered (there are no shorted pins)

・ProMicro and PC are connected with a USB cable (the USB cable is for data communication, not for charging only)

##Attach the ProMicro protective cover to the top plate
--------
Attach the ProMicro protective cover to the top plate 

NOTE 
+ Tightening the screws too tightly may cause cracks in the acrylic parts. Please tighten appropriately.
+ A protective sheet is attached to the acrylic parts. Please remove the protective sheet before assembling.
![Hotswaps for 1U and 1.25u](https://reviung.com/wp-content/uploads/2020/01/reviung41-PMcover-1-1280x855.jpg)


 

Insert the screw into the screw hole for the ProMicro protective cover and flip it over.

Pass the spacer through, attach the top plate, and secure with nuts.

![Hotswaps for 2.25u](https://reviung.com/wp-content/uploads/2021/07/R5_17-1280x855.jpg)


## Attach the switch to the top plate
------

Attach the switch to the top plate.

![hotswaps](https://reviung.com/wp-content/uploads/2021/07/R5_19-1280x855.jpg)

## [Optional] Solder the rotary encoder
----
Solder the rotary encoder before placing the top plate on the PCB.

## Attach all switches to the top plate and main PCB.
--------
Check that the terminals on each switch are not bent.
Attach the top plate with switches (5 pieces) to the main PCB.
Check from the side to see if each switch is inserted correctly into the main PCB.


![underglow](https://reviung.com/wp-content/uploads/2021/07/R5_20a.jpg)

## Solder the switch.
-------
Finally, solder the switch.

At this time, make sure that the switch is firmly attached to the top plate before soldering.

![Stablizers installed](https://reviung.com/wp-content/uploads/2021/07/R5_21a.jpg)

![Stablizers installed](https://reviung.com/wp-content/uploads/2021/07/R5_22a-1280x855.jpg)

This completes the soldering work.
Check the entire assembly to make sure there are no forgotten solders or incorrect installation directions of parts.

Finally, use a flux cleaning solution to thoroughly clean away any remaining flux.

## Install the bottom plate.
---------
![screen with one screw installed](https://reviung.com/wp-content/uploads/2021/07/R5_23-1280x855.jpg)
![back of screw](https://reviung.com/wp-content/uploads/2021/07/R5_24a-1280x855.jpg)

1. Attach the spacer to the bottom plate with M2 screws, paying attention to the front and back sides of the bottom plate.
2. Place the top plate + main PCB on the bottom plate.
3. Complete by fixing the screws from the top plate side.

Attach the rubber feet to the four corners of the bottom plate.

## Attach the keycap and you're done.
-------
Finally, attach the keycap and you're done.
Attach your favorite keycaps.


![switches in the top plate](https://reviung.com/wp-content/uploads/2021/07/R5_25-1280x855.jpg)
![switches in the top plate](https://reviung.com/wp-content/uploads/2021/07/reviung5-main-1280x855.jpg)
![switches in the top plate](https://reviung.com/wp-content/uploads/2021/06/reviung5-2-1280x855.jpg)
![switches in the top plate](https://reviung.com/wp-content/uploads/2021/07/reviung5-0-1280x855.jpg)
