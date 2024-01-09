
<h1 align="center">

<a  name="logo"  href="Misc/logo.png"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/logo.png"  alt="@Nadeshiko's SlimeVR"></a>

<br>

@Nadeshiko's SlimeVR

</h1>

  

Based off the [SlimeVR Official Component Guide](https://docs.slimevr.dev/diy/components-guide.html).

@Nadeshiko's Slimes run on a [Wemos D1 Mini](https://www.wemos.cc/en/latest/d1/d1_mini_3.1.0.html) with an IMU IC of your choice that has the same module profile as the [SlimeVR BNO085](https://shop.slimevr.dev/products/slimevr-imu-module-bno085)'s or the [GY-BMI160](https://www.aliexpress.com/w/wholesale-GY%2525252dBMI160.html)'s. They use the [TP4056 lithium charger](https://www.aliexpress.com/w/wholesale-tp4056.html) module for 3.7V LiPo batteries.

- Easy and cheap to build.
- No wires needed to be soldered.
- Lightweight and smooth, clean looks.
- 40mm or 50mm strap width is supported.
- Detailed component purchase list.
- Wall-mountable charging dock (WIP).
- Photographed assembly instructions.



  

## Index

- [PCB](#pcb)
- [Case](#case)
- [Components](#components)
- [Basic Assembly Guide](#assembly)
- [Alternative IMUs](#imu)
- [Resources](#resources)
- [Detailed Assembly Guide](#detailed-assembly)
- [How to order PCB/3DPrints](#ordering)
- [Support](#support)


<br/>

## PCB

  

The main PCB lets every component be soldered on without any wire connections between the modules. This includes the diodes and resistors for battery sense and charge protection. The TP4056 charger is on the back side to save on size and cost; a JST 2mm 2-pin connector can be added to make battery connections easier; an SK12D07VG 3-pin switch will be used to turn the tracker on or off; and a ZH 1.5mm 5-pin connector is used for extension tracker communication with SCL and SDA in the same cable layout as the official tracker extension method to avoid crosstalk on long extension cables.

The PCB's can also be used without a case, as there are built-in cutouts for straps to pass through.

  

PCBs can be ordered from [JLCPCB](https://cart.jlcpcb.com/quote/), [Elecrow](https://www.elecrow.com/pcb-manufacturing.html), [PCBGOGO](https://www.pcbgogo.com/pcb-fabrication-quote.html), [NextPCB](https://www.nextpcb.com/pcb-quote#/pcb-quote) or your preferred low cost PCB manufacturer.

  

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PCBFront.png"  alt="R3MiniPCBFront" width=290px />&nbsp;&nbsp;&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PCBBack.png"  alt="R3MiniPCBBack" width=290px />&nbsp;&nbsp;&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Extension-PCB-Front.png"  alt="TrackerExtensionPCB" width=150px />

<p align="center">PCB Front/Back - Extension Tracker</p>

<br/>



## Case

  

The tracker case, can house a 3.7V LiPo in 103450 size or any up to 10mm thick. Cell dimensions advised are 10x34x50mm or less. These cells have a similar runtime to 18650 Li-ion cells but are cheaper.

  

The case has been designed according to [JLCPCB/JLC3DP resin 3D printing guideline](https://jlc3dp.com/help/article/212-3D-Printing-Design-Guideline). The case can be ordered from [JLC3DP](https://jlc3dp.com/3d-printing-quote) or [Elecrow](https://www.elecrow.com/3d-printing-service.html), and the resin to select on your order is up to you. I prefer the [**8111X**](https://jlc3dp.com/help/article/199-8111X---Photosensitive-Resin), [**CBY**](https://jlc3dp.com/help/article/437-CBY-Photosensitive-Resin), [**Black Resin**](https://jlc3dp.com/help/article/198-Black-Resin--Photosensitive-Resin), or equivalent.

  

The case and the tracker extension case are two part with snap-fitting closures, with added extra security once a strap is used.

  

It prints as two parts: a snap-fit main body with strap holes on the side, ports for the D1 Mini, an extension tracker connector, and the power switch. The other is the base plate with strap holes on the bottom, and PCB stand/aligners, and a port for the TP4056 charger.

Up to a 50mm strap can be fitted to the main case; the best one to use is the non-slip elastic kind with plastic buckles in the same size to make it easier to remove, as listed in the Google Sheet BOM. The strap has a few bends through the case to stop any unnecessary slop and keep it locked against the skin.

A gentle curve has been added on the underside of the case, matching that of arms, legs, or hip; this is to reduce any edges digging into the skin and also increase the contact area of the non-slip strap.

  

The files for the case are:


- [ ] [TOP.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main/3D%20Print%20STL/SlimeVRNadeshiko-TOP.stl)

- [ ] [BASE.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main/3D%20Print%20STL/SlimeVRNadeshiko-BASE.stl)



<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview1.png"  alt="R3Mini1034501"/></div>

<div align="center">7.0x3.09x5.3cm</div>

<br/>



 <br/>

- **Tracker Extension:** It also has three parts: the main case, an endcap, and the PCB to mount the BMI/BNO module and ZH 1.5mm 5 Pin connector. 25mm hook and loop straps can be used with the extension case. The PCB is based on the [SlimeVR OSHWLab DIY Extension](https://oshwlab.com/eirenliel/slimevr-diy-tracker-extension) changes to make it easier for hand soldering and case fitment. 

The files for the extension are:


- [ ] [BODY.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/3D%20Print%20STL/SlimeVRNadeshikoExtension-BODY.stl)

- [ ] [ENDCAP.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/3D%20Print%20STL/SlimeVRNadeshikoExtension-ENDCAP.stl)

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-1.png"  alt="TrackerExtension" width=200px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-2.png"  alt="TrackerExtension" width=180px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-3.png"  alt="TrackerExtension" width=220px /></div>

<div align="center">3.80×1.20×3.48 cm</div>

<br/>



## Components

The components needed have all been added to a Google sheet here with links to each item's store page and total estimated cost.
-  #### [Components BOM Sheet](https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing)

If you would like to use the BMI-270, they can be purchased from [KOUNO](https://store.kouno.xyz/products/bmi270-breakout-board).

<div align="center"><a  name="logo"  href="https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/render4.png"  alt="Components"></a></div>

<br>



## Assembly

While soldering, use flux to make things easier, keep your solder iron's tip tinned with solder when not in use to protect from oxidation. Make sure to clean the PCBs after soldering. You can use PCB cleaner or isopropyl alcohol. This is to remove the flux, which some are acidic and will attack the solder joint over time. 


The basic steps of assembly for the main trackers are:


- [ ] 1x 180K resistor and 2x 1N5817 diodes soldered in the correct orientation on the PCB.
- [ ] Clip off the excess pins of the diodes and resistor and keep it aside for soldering the TP4056.
- [ ] Solder a TP4056 flush to the backside of the breakout PCB, using the clipped excess pins from previous step to make this step easier.
- [ ] Solder on a JST PH 2mm 2-Pin header for the battery.
- [ ] Solder on a SK12D07VG slide switch.
- [ ] (Optional/Ankle trackers for foot extensions) Solder on a ZH 1.5mm 5 Pin header for communication with an extension tracker.
- [ ] Solder the BMI/BNO08X module to the PCB with header pins or flush.
- [ ] Solder on a D1 Mini with included header pins, adjust them if needed.
- [ ] Use polyimide tape or equivalent on header pins and the LiPo battery to protect it from puncture, and shorts.
- [ ] Check LiPo's battery JST plug matches the +/- polarity as on the PCB's header (Fix the battery plug if not).
- [ ] Connect the LiPo battery with the power switch in the OFF position.
- [ ] Power switch still in the OFF position: flash firmware using the online firmware flasher or by following the SlimeVR firmware documentation.
  

The basic steps of assembly for the extension trackers:
  

- [ ] Solder on a 100nf capacitor to the extension PCB.
- [ ] Then the ZH 1.5mm 5 pin header for communication with the main tracker.
- [ ] Solder a BMI/BNO08X module flush to the extension PCB.
  
   
<br>



## IMU


LGA14 footprint BMI-160 alternatives such as the BMI-270, BMI360, LSM6, ICM42688, BHI360, etc. can be done with the [LSM6DSV Module by Kounocom](https://github.com/kounocom/LSM6DSV-Module) or by soldering work on cheap AliExpress GY-BMI-160 modules with your desired IC.
This requires you to use a [mini hot plate](https://www.aliexpress.com/w/wholesale-solder-mini-hot-plate.html?g=y&SearchText=solder+mini+hot+plate&sortType=total_tranpro_desc) to prevent the IMU from being melted by other soldering methods, such as hot air. Begin by placing solder on the module's IMU pads using your soldering iron, cleaning with IPA, adding some fresh flux to the pads, and putting your replacement IMU on using the hot plate.


<br>



## Resources


Useful Links:


- [Online Firmware Flasher](https://slimevr-firmware.bscotch.ca/)
- [SlimeVR Documentation](https://docs.slimevr.dev/)
- [IMU Rotation](https://docs.slimevr.dev/firmware/configuring-project.html#adjust-imu-board-rotation)
- [CH340 Driver](https://www.wemos.cc/en/latest/ch340_driver.html)
- [BMI160 Calibration](https://github.com/SlimeVR/SlimeVR-Tracker-ESP?files=1#bmi160)
- [SlimeVR Github](https://github.com/SlimeVR/)
- [SlimeVR Discord](https://discord.gg/SlimeVR)

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PlacementExample.png"  alt="TrackerPlacement"/></div>


 
<br>


## Detailed-Assembly

 
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

If you are experienced with soldering, you can skip using the excess from the previous step; if not bend the excess over the TP4056 and the PCB holes so it stays in place and solder, this helps solder flow into the hole:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/1.jpg"  alt="1"/>
 
Here's how the topside of the breakout PCB should look when using the excess for help:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/2.jpg"  alt="2"/>
 
Then do the same thing on all the other pads of the TP4056, 6 in total:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/3.jpg"  alt="3"/>
 
Clip off the excess from all 6 points so it's nice and neat:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/5.jpg"  alt="5"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/6.jpg"  alt="6"/>

If you know how to flush solder and get good connection, then you can skip on using the excess pins.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-4-TP4056/0.jpg"  alt="0"/>

 
#### Step 5 -  We now add a JST 2-Pin for the battery connection.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/1.jpg"  alt="1"/>

First place it in the correct position and orientation as shown on the PCB:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/2mono.jpg"  alt="2"/>
 
Then keep it in place with a helper:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/3mono.jpg"  alt="3"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/4mono.jpg"  alt="4"/>
 
And solder both of the pins on the backside of the PCB quickly, to not overheat the housing:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-5-2Pin/5.jpg"  alt="5"/>

 
#### Step 6 -  We now do the power switch and optionally a ZH 5 pin header for communication with an extension tracker.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/1.jpg"  alt="1"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/2mono.jpg"  alt="2"/>
 
OPTIONAL: If a 5 pin is needed on the tracker for extension communication, then clamp it down like this so its flush with the PCB:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/3mono.jpg"  alt="3"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-6-5Pin-Switch/4mono.jpg"  alt="4"/>
 
OPTIONAL: Solder the pins on the backside of the PCB similar to the JST 2 pin, stop soldering after the pin is wetted enough to not melt the plastic housing:
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
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-10-Tape/1.jpg"  alt="1"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-10-Tape/3.jpg"  alt="3"/>

#### Step 11 -  Flash the firmware, the light will turn from blinking to solid for a moment when complete.
For more accurate SlimeVR dashboard battery percentage/voltage readout set BATTERY_SHIELD_RESISTANCE to 153K.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly/Step-11-Firmware/1.gif"  alt="1"/>


 


 
After firmware flashing is complete, you can tape the battery to the PCB and/or place into the 3D printed cases.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/cases8111X.jpg"  alt="cases"/>

<br>
 
 

## Ordering

### PCB
Ordering the PCB and 3D Prints is easy. Head to the [releases](https://github.com/Aeurias/NadeshikoSlimeVR/releases) section and download the 3D print .stl files, and the PCB Gerber .zip files.

For PCB ordering, head over to  [JLCPCB](https://cart.jlcpcb.com/quote/) and upload the gerber .zip files. Use the settings below on the order page:
 
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main/PCB%20Gerber/OrderingPCB.png"  alt="Ordering"/>

They can also be ordered from [Elecrow](https://www.elecrow.com/pcb-manufacturing.html), [PCBGOGO](https://www.pcbgogo.com/pcb-fabrication-quote.html), [NextPCB](https://www.nextpcb.com/pcb-quote#/pcb-quote) or your preferred PCB manufacturer.
 
 
### Cases
For 3D Print case ordering, head over to [JLC3DP](https://jlc3dp.com/3d-printing-quote) and upload the .stl files for each model, including the top/body and base/end cap etc. One case comes in two parts, so make sure you upload both halves. Then use the settings below on the order page and set the quantity of each part to the number of trackers you are building:
 
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main/3D%20Print%20STL/OrderingCases.png"  alt="Ordering"/>

Cases can also be ordered from [Elecrow](https://www.elecrow.com/3d-printing-service.html) or your preferred 3D print services.

<br>

## Support
Feel free to open an issue if you have any questions or to share some pictures! :3
 
You may also DM me on Discord: [@aeurias](https://discord.com/users/240905316013703169), or add on VRChat: [Nadeshiko ~](https://vrchat.com/home/user/usr_f6e358a4-a938-46eb-bfb2-4fee10bd21e5).