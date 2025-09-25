<h1 align="center">
<a  name="logo"  href="Misc/logo.png"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/ESP32-C3-Supermini/Tracker%20Supermini/Previews/logo1.png"  alt="@Nadeshiko's Mini SlimeVR"></a>
@Nadeshiko's Supermini SlimeVR

</h1>

> [!CAUTION]
> This is experimental, in writeup and testing process at the moment! Expect some changes to be made to this branch before finalized.

> [!IMPORTANT]
> For the regular, WEMOS D1 Mini variant please view the [main branch here!](https://github.com/Aeurias/NadeshikoSlimeVR/)

> [!WARNING]  
> Some sections below has yet to be updated for the ESP32-C3 Supermini variant!


These are one of the smallest WiFi module based SlimeVR trackers possible, similar to [Gorbit99's Tiny Slime](https://github.com/gorbit99/tiny-slime), as small as extension trackers! The idea was for these to be a replacement for wired extension trackers, whose cable can get in the way and are prone to damage, and be a more useable and comfortable size for tracking locations such as shoulders, lower arms, neck, or head.

There is however a drawback with this small size compared to the regular [@Nadeshiko SlimeVR's](https://github.com/Aeurias/NadeshikoSlimeVR/) or any built with ESP32 D1 Mini's; the WiFi performance is much weaker on the ESP32-C3 Supermini, to be used with a router setup in the same room as the trackers without wall interference.

Due to how small these are, there is no option to connect an extension tracker, as that will only increase the overall size and cost of a whole tracker set.

@Nadeshiko's Mini Slimes run on a [ESP32-C3 Supermini](https://www.aliexpress.com/item/1005005877531694.html) with an IMU IC of your choice that has the same module profile as widely used SlimeVR IMU-module format like the [Mumo ICM-45686](https://shop.slimevr.dev/products/slimevr-mumo-breakout-module-v1-icm-45686-qmc6309)'s. They use the [TP4056 Unprotected lithium charger](https://www.aliexpress.com/item/1005005468881238.html) module for 3.7V LiPo batteries.



- 2.6cm x 3.8cm PCB design.
- Easy and very cheap to build.
- No wires needed to be soldered.
- Lightweight and smooth, clean case looks.
- 25mm strap width is supported.

  

## Index

- [PCB](#pcb)
- [Case](#case)
- [Components](#components)
- [Basic Assembly Guide](#assembly)
- [Resources](#resources)
- [Detailed Assembly Guide](#detailed-assembly)
- [How to order PCB/3DPrints](#ordering)
- [Support](#support)


## PCB

  

The PCB lets every component be soldered on without any wire connections between the modules. This includes the diodes and resistors for battery sense and charge protection. The ESP32-C3 Supermini is on the back side to save on size and cost; a JST 2mm 2-pin connector can be added to make battery connections easier; an SK12D07VG 3-pin switch will be used to turn the tracker on or off.

  

PCBs can be ordered from [JLCPCB](https://cart.jlcpcb.com/quote/), [Elecrow](https://www.elecrow.com/pcb-manufacturing.html), [PCBGOGO](https://www.pcbgogo.com/pcb-fabrication-quote.html), [NextPCB](https://www.nextpcb.com/pcb-quote#/pcb-quote) or your preferred low cost PCB manufacturer.

  

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/ESP32-C3-Supermini/Tracker%20Supermini/Previews/miniR4-2.png"  alt="Supermini Front" width=290px />&nbsp;&nbsp;&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/ESP32-C3-Supermini/Tracker%20Supermini/Previews/miniR4-1.png"  alt="Supermini Back" width=290px /></div>

<p align="center">PCB Front/Back - 26mm x 38mm</p>


## Case

The tracker case, can house a 3.7V LiPo in 502040 (5x20x40mm) or 602535 (6x25x35mm) size comfortably. Max LiPo cell dimensions are 6x25x40mm or less with capacity around 200-400mah.


The case has been designed according to [JLCPCB/JLC3DP resin 3D printing guidelines](https://jlc3dp.com/help/article/212-3D-Printing-Design-Guideline). The case can be ordered from [JLC3DP](https://jlc3dp.com/3d-printing-quote) or [Elecrow](https://www.elecrow.com/3d-printing-service.html), and the resin to select on your order is up to you. I prefer the [**9000R**](https://jlc3dp.com/help/article/195-9000R---Photosensitive-Resin), [**CBY**](https://jlc3dp.com/help/article/437-CBY-Photosensitive-Resin), [**Black Resin**](https://jlc3dp.com/help/article/198-Black-Resin--Photosensitive-Resin), or equivalent low cost options..

It prints as two parts: a snap-fit closure with holes for strap, the TP4056 charger and ESP32-C3 USB ports, and the power switch.

25mm strap can be fitted to the case; the best one to use is the non-slip elastic kind with plastic buckles and tri-buckles in the same size to make it easier to remove, more comfortable and adjustable. Hook and Loop style of strap can also be used.


The files for the case are:


- [ ] [NadeshikoSupermini-TOP.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/ESP32-C3-Supermini/Tracker%20Supermini/3D%20Print%20STL/NadeshikoSupermini-TOP.stl)

- [ ] [NadeshikoSupermini-BASE.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/ESP32-C3-Supermini/Tracker%20Supermini/3D%20Print%20STL/NadeshikoSupermini-BASE.stl)


<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/ESP32-C3-Supermini/Tracker%20Supermini/Previews/Readme-Preview.png"  alt="MiniPreview"/></div>

<div align="center">30.1mm x 43.8mm × 19.7mm - 7.02cm³</div> 



<br/>



## Components

The component cost should come out to around £6.00/$8.2/€6.95 with cases per tracker usind the LSM6DSR IMU's or £8.42/$11.4/€9,7 with the recommended ICM-45686 IMU's.
Quantity and prices listed below are per tracker expense and quantity used of each components.
Some of the smaller items are sold in pack sizes of 10/50/100 etc. which can build multiple trackers with.
Prices here are listed without any shipping costs, or pack sizes, or taxes, and may not be latest.

| Components per SlimeVR Tracker        |  QTY  |   £   | Link                                                                  |
| ------------------------------------- | ----: | ----: | --------------------------------------------------------------------- |
| @Nadeshiko Mini PCB                   |     1 |  0.39 | [JLCPCB](https://jlcpcb.com/)                                         |
| @Nadeshiko Mini Case                  |     1 |  0.55 | [JLC3DP](https://jlc3dp.com/)                                         |
| ESP32-C3 SuperMini V1/V2              |     1 |  1.59 | [AliExpress](https://www.aliexpress.com/item/1005006391993583.html)   |
| SlimeVR Mumo ICM-45686 IMU Module     |     1 |  5.00 | [SlimeVR](https://shop.slimevr.dev/products/slimevr-mumo-breakout-module-v1-icm-45686-qmc6309)                                   |
| ↳ or LSM6DSR IMU Module               |     1 |  2.59 | [Mofflab](https://moffshop.deyta.de/products/lsm6dsr)                 |
| TP4056 Unprotected Charger Type-C     |     1 |  0.11 | [AliExpress](https://www.aliexpress.com/item/32646649119.html)        |
| SK12D07VG Slide Switch in 3/4/5mm     |     1 |  0.04 | [AliExpress](https://www.aliexpress.com/item/1005005786809487.html)   |
| 1206/3216 Resistors in 100K Ohm       |     2 |  0.01 | [AliExpress](https://www.aliexpress.com/item/32982307507.html)        |
| SS34 DO214AC Diodes                   |     2 |  0.01 | [AliExpress](https://www.aliexpress.com/item/1005005707508759.html)   |
| LiPo Battery 6x25x40mm or smaller     |     1 |  0.72 | [EHAO](https://www.aliexpress.com/w/wholesale-EHAO.html) or [XINJ](https://www.aliexpress.com/store/4885018/pages/all-items.html) or [ROGRAPO](https://www.aliexpress.com/store/910326412/pages/all-items.html) @AliExpress |

| Mounting Straps for Trackers          | Link                                                                  |
| ------------------------------------- | --------------------------------------------------------------------- |
| 25mm Hook & Loop                      | [AliExpress](https://www.aliexpress.com/item/1005006326126306.html)   |
| 25mm Elastic Strap & Buckles          | [AliExpress](https://www.aliexpress.com/item/1005006096453678.html)   |
| 25mm Tri Glide Adjustable Buckles     | [AliExpress](https://www.aliexpress.com/item/1005006144047161.html)   |
| 25mm Release Buckles                  | [AliExpress](https://www.aliexpress.com/item/1005006082194146.html)   |


<br>




## Assembly

Using a solder helping hand will make putting everything on the PCB much easier! While soldering, keep your solder iron's tip tinned with solder when not in use to protect from oxidation. Make sure to clean the PCBs from excess flux after soldering. You can use PCB cleaner or isopropyl alcohol.

The basic steps of assembly for the main trackers are:

- [ ] 2x 1206 100K resistor and 2x SS34 diodes soldered in the correct orientation on the PCB.
- [ ] Solder a unprotected TP4056 charger flush to the PCB.
- [ ] Solder on a SK12D07VG slide switch.
- [ ] Solder the BMI-270 IMU module to the PCB.
- [ ] Solder the ESP32-C3 SuperMini module flush to the PCB.
- [ ] Connect or solder on the LiPo battery with the power switch in the OFF position in correct polarity.

Flashing:

- [ ] Power switch still in the OFF position; Flash firmware using the online firmware flasher for BMI-270.
- [ ] When flashing, you want to choose `BOARD_LOLIN_C3_MINI` as the board.
- [ ] In Advanced options, change SDA Pin to `"6"`, SCL Pin to `"7"`, and LED Pin to `"8"`.

- [ ] OPTIONAL: Use polyimide tape or equivalent on sharp corners and the LiPo battery to protect it from puncture.
- [ ] OPTIONAL: If using JST PH 2mm 2-pin header. Check battery plug polarity matches the +/- polarity as on the PCB.
- [ ] OPTIONAL: If using V2 of ESP32-C3 SuperMini, connect an optional appropriate size antenna for a more reliable WiFi strength.

  
   
<br>    

<br>



## Resources


Useful Links:


- [SlimeVR Documentation](https://docs.slimevr.dev/)
- [SlimeVR Github](https://github.com/SlimeVR/)
- [SlimeVR Discord](https://discord.gg/SlimeVR)
- [Online Firmware Flasher](https://slimevr-firmware.bscotch.ca/)
- [Online Firmware Flasher Alt](https://slimevr.shinebright.dev/)
- [SlimeVR-Tracker-ESP](https://github.com/SlimeVR/SlimeVR-Tracker-ESP)
- [SlimeVR-Server](https://github.com/SlimeVR/SlimeVR-Server)
- [CH340 Driver](https://www.wemos.cc/en/latest/ch340_driver.html)
- [BMI Calibration](https://github.com/SlimeVR/SlimeVR-Tracker-ESP?files=1#bmi160)
- [IMU Rotation](https://docs.slimevr.dev/firmware/configuring-project.html#adjust-imu-board-rotation)


 
<br>


## Detailed-Assembly

> [!WARNING]  
> Content below has yet to be updated for the ESP32-C3 Supermini variant!

<!---
#### Step 1 - We will begin with the resistor and diodes and then the TP4056 Module.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step1-ResDio-Bend/2.jpg"  alt="1"/>
 
First bend the resistor and diodes like this to make it fit the breakout PCB:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step1-ResDio-Bend/3.jpg"  alt="2"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step1-ResDio-Bend/4.jpg"  alt="3"/>
 

#### Step 2 -  Place the resistor and diodes on the PCB.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-2-ResDio-1/1.jpg"  alt="1"/>
 
If they do not stay in place, secure them down with some polyimide tape:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-2-ResDio-1/2.jpg"  alt="2"/>
 
While they are level with the PCB, solder them down:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-2-ResDio-1/3.jpg"  alt="3"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-2-ResDio-1/4.jpg"  alt="4"/>

 
#### Step 3 -  Clip off the excess from the resistor and diodes.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-3-ResDio-2/1.jpg"  alt="1"/>
 
You can use these excess to make flush mounting the TP4056 easier if unexperienced with flush mount soldering.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-3-ResDio-2/2.jpg"  alt="2"/>
 

#### Step 4 -  Next we solder on the TP4056 flush to the PCB on the backside.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/00.jpg"  alt="00"/>

If experienced with soldering, you can skip using the excess from the previous step and flush solder; If not, then bend the excess through the TP4056 and the PCB holes so it stays in place and solder, this helps solder flow into the hole, good if you are unsure flush soldering is making good connections:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/1.jpg"  alt="1"/>
 
Here's how the topside of the breakout PCB should look when using the excess for help:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/2.jpg"  alt="2"/>
 
Then do the same thing on all the other pads of the TP4056, 6 in total:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/3.jpg"  alt="3"/>
 
Clip off the excess from all 6 points so it's nice and neat:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/5.jpg"  alt="5"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/6.jpg"  alt="6"/>

Again, if you know how to flush solder and get good connection, then you can skip on using the excess pins.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/0.jpg"  alt="0"/>

 
#### Step 5 -  We now add a JST 2-Pin for the battery connection.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/1.jpg"  alt="1"/>

First, place it in the correct position and orientation as shown on the PCB:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/2mono.jpg"  alt="2"/>
 
Then keep it in place with a helper:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/3mono.jpg"  alt="3"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/4mono.jpg"  alt="4"/>
 
And solder both of the pins on the backside of the PCB quickly, to not overheat the housing:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/5.jpg"  alt="5"/>

 
#### Step 6 -  We now do the power switch and optionally a ZH 1.5mm 5-pin header for communication with an extension tracker.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/1.jpg"  alt="1"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/2mono.jpg"  alt="2"/>
 
OPTIONAL: If a 5-pin is needed on the tracker for extension communication, then clamp it down like this so its flush with the PCB:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/3mono.jpg"  alt="3"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/4mono.jpg"  alt="4"/>
 
OPTIONAL: Solder the pins on the backside of the PCB similar to the JST 2-pin, stop soldering after the pin is wetted enough to not melt the plastic housing:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/5.jpg"  alt="5"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/6mono.jpg"  alt="6"/>
 
Next we will do the power switch, clamp it secure for soldering by the edge case grounding pin:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/7mono.jpg"  alt="7"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/8mono.jpg"  alt="8"/>
 
Solder it in place just like the previous step:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/9.jpg"  alt="9"/>


 
#### Step 7 -  The IMU module will now go on with its header pins.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/1.jpg"  alt="1"/>
 
Begin by snapping the correct length of the header pins for the side with the holes on the PCB.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/2.jpg"  alt="2"/>

The repositioning of the plastic spacer can be easily done by hand on a flat surface, best to have them even like this for good battery clearance in the cases:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/0.jpg"  alt="0"/>
 
Place it on the PCB with the excess next to it, as we will use this temporarily to keep the IMU level:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/4.jpg"  alt="4"/>

Next we place the IMU on top to have a surface to clamp the header pin down on:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/5.jpg"  alt="5"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/6.jpg"  alt="6"/>
 
Flip everything over to the backside and solder all the header pins to the breakout PCB: 
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/7.jpg"  alt="7"/>
 
Next we will solder the IMU module itself to the header pins. For the module to be level, you can continue using the excess header pins as a guide to level the module with the PCB:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/12mono.jpg"  alt="12"/>
 
Solder the IMU module to the header pins and remove the temporary excess header pins:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/13.jpg"  alt="13"/>


#### Step 8 -  Next we will do the D1 Mini and it's header pins.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-8-D1Mini/1.jpg"  alt="1"/>

Again repositioning of the plastic spacer can be easily done by hand on a flat surface, have them even both sides like this to help battery clearance:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-7-BMI-BNO/0.jpg"  alt="0"/>

Place the header pins on the PCB and then the D1 Mini. Clamp down the D1 securing the header pins:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-8-D1Mini/2.jpg"  alt="2"/>

Flip to the backside as this will be soldered first:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-8-D1Mini/3.jpg"  alt="3"/>

Solder the D1 Mini header pins on the backside of the PCB:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-8-D1Mini/4.jpg"  alt="4"/>

Finish step by soldering the D1 Mini to the header pins, making sure not to overheat the header pin's black plastic:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-8-D1Mini/5.jpg"  alt="5"/>
 



#### Step 9 -  Clean the board to remove flux, use PCB cleaner or 99% isopropyl alcohol
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-9-Cleaned/1.jpg"  alt="1"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-9-Cleaned/2.jpg"  alt="2"/>

#### Step 10 -  Tape off the pins and add a layer to the battery to protect it from puncture and wear.
> [!TIP]
> It may be best to add a sheet of plastic below the battery to protect it further. Such as plastic cut from a bottle.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-10-Tape/1.jpg"  alt="1"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-10-Tape/3.jpg"  alt="3"/>

#### Step 11 -  Flash the firmware, the light will turn from blinking to solid for a moment when complete.
For more accurate SlimeVR dashboard battery percentage/voltage readout for @Nadeshiko Slimes, set BATTERY_SHIELD_RESISTANCE to ~166K.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-11-Firmware/1.gif"  alt="1"/>

 
After firmware flashing is complete, you can tape the battery to the PCB and/or place into the 3D printed cases.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/cases8111X.jpg"  alt="cases"/>
 

-->

<br>
 
 

## Ordering

> [!WARNING]  
> Content below has yet to be updated for the ESP32-C3 Supermini variant!

### PCB
Ordering the PCB and 3D Prints is easy. Head to the [releases](https://github.com/Aeurias/NadeshikoSlimeVR/releases) section and download the 3D print .stl files, and the PCB Gerber .zip files.

For PCB ordering, head over to  [JLCPCB](https://cart.jlcpcb.com/quote/) and upload the gerber .zip files. Use the settings below on the order page:
 
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/ESP32-C3-Supermini/Tracker%20Supermini/PCB%20Gerber/orderingPCB.png"  alt="Ordering"/>

They can also be ordered from [Elecrow](https://www.elecrow.com/pcb-manufacturing.html), [PCBGOGO](https://www.pcbgogo.com/pcb-fabrication-quote.html), [NextPCB](https://www.nextpcb.com/pcb-quote#/pcb-quote) or your preferred PCB manufacturer.
 
 
### Cases

> [!WARNING]  
> Content below has yet to be updated for the ESP32-C3 Supermini variant!

For 3D Print case ordering, head over to [JLC3DP](https://jlc3dp.com/3d-printing-quote) and upload the .stl files for each model, including the top/body and base/end cap etc. One case comes in two parts, so make sure you upload both halves. Then use the settings below on the order page and set the quantity of each part to the number of trackers you are building. The available SLA material and prices will vary, as the model has been designed to be used with any of the SLA resins, any of the cheapest option will be good enough for the trackers, 
 
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/ESP32-C3-Supermini/Tracker%20Supermini/3D%20Print%20STL/OrderingCases.png"  alt="Ordering"/>

Cases can also be ordered from [Elecrow](https://www.elecrow.com/3d-printing-service.html) or your preferred 3D print services.

<br>

## Support
Feel free to open an issue if you have any questions or to share some pictures! :3
 
You may also DM me on Discord: [@aeurias](https://discord.com/users/240905316013703169), or add on VRChat: [Nadeshiko ~](https://vrchat.com/home/user/usr_f6e358a4-a938-46eb-bfb2-4fee10bd21e5).
