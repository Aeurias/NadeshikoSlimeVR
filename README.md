
<h1 align="center">

<a  name="logo"  href="Misc/logo.png"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/logo.png"  alt="@Nadeshiko's SlimeVR"></a>

<br>

@Nadeshiko's SlimeVR

</h1>

  

Based off the [SlimeVR Official Component Guide](https://docs.slimevr.dev/diy/components-guide.html).

@Nadeshiko Slime's run on a Wemos D1 Mini with IMU IC of your choice that have module profile same as the SlimeVR BNO085's or the BMI160's, they use the TP4056 charger for 3.7V LiPo batteries.

- Easy & cheap to build.
- No wires needed to be soldered.
- Lightweight & smooth clean looks.
- 40mm or 50mm strap width supported.
- Detailed component purchase list.

#### WIP
 
- Multi port charging dock.
- Photographed assembly instructions.



  

## Index

- [PCB](#pcb)
- [Case](#case)
- [Components](#components)
- [Assembly](#assembly)
- [Alternative IMUs](#imu)
- [Resources](#resources)

<br/>

## PCB

  

The main PCB lets every component be soldered on without any wires connections between the modules. This includes the diodes and resistor for battery sense and charge protection. The TP4056 charger is on the back side to save on size and cost, a JST 2mm 2-Pin connector can be added to make battery connections easier, an SK12D07VG 3-pin switch will be used to turn the tracker on or off, and a ZH 1.5mm 5-pin connector is used for extension tracker communication with SCL and SDA in the same cable layout as the official tracker extension method to avoid crosstalk on long extension cables.

The PCB's can also be used without a case, as there are built in slots cutouts for straps to pass through.

  

PCBs can be ordered from [Elecrow](https://www.elecrow.com/pcb-manufacturing.html), [JLCPCB](https://cart.jlcpcb.com/quote/), [PCBGOGO](https://www.pcbgogo.com/pcb-fabrication-quote.html), [NextPCB](https://www.nextpcb.com/pcb-quote#/pcb-quote) or your preferred low cost PCB manufacturer.

  

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PCBFront.png"  alt="R3MiniPCBFront" width=290px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PCBBack.png"  alt="R3MiniPCBBack" width=290px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Extension-PCB-Front.png"  alt="TrackerExtensionPCB" width=190px />

<p align="center">PCB Front/Back - Extension Tracker</p>

<br/>



## Case

  

The trackers case can house a 3.7v LiPo in sizes 503450 or smaller, to 103450 or smaller which has similar runtime to 18650 Li-ion cells but are cheaper.

  

Case has been designed to JLCPCB/JLC3DP resin 3D printing guidelines and tolerances, the cases can be ordered from JLC3DP or Elecrow, the resin to select on your order is up to you. I prefer the **8111X** or **Black Resin** or equivalent.

  

The cases and the tracker extension are 2 part with snap fitting closure, with added extra added secureness once a strap is used.

  

It prints as two parts, a snap fitting main body with strap holes on the side, ports for the D1 Mini, extension tracker connector and the power switch. The other is the base plate with strap holes on the bottom and PCB stand/aligners, and a port for the TP4056 charger.

Up to 50mm strap can be fitted to the main cases, best one to use is the non-slip elastic kind with plastic buckles in same size to make it easier to remove as listed in the Google sheet BOM. The strap has few bends through the case to stop any unnecessary slop and keep it locked against the skin.

A gentle curve has been added on the underside of the case matching that of arms, legs or hip, this is to reduce any edges digging into the skin and also increases contact area of the non-slip strap.

  

The variants of the cases are:


  

- **103450 LiPo** - Allows 3.7v LiPo cells up to 10mm thick. Cell dimensions advised are 10x34x50mm or less. *It's the one I recommend as this has best runtime for it's size and the cell's are lowest cost per wh.*

- [ ] 103450-TOP.stl

- [ ] 103450-BASE.stl



<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview1.png"  alt="R3Mini1034501"/></div>

<div align="center">7.03x2.74x5.23cm</div>

<br/>

  

-  **503450 LiPo** - This one allows a 5mm thick 503450 or thinner LiPo cell. Cell dimensions advised are 5x34x50mm or less. *LiPo's for this size are in high demand so may be difficult to find good prices*

- [ ] 503450-TOP.stl

- [ ] 503450-BASE.stl



<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview2.png"  alt="R3Mini5034501"/></div>

<div align="center">7.03x2.11x5.23cm </div>

 <br/>

- **Tracker Extension** - It is also three part, the main case, an endcap and along with the PCB to mount the BMI/BNO module and ZH 1.5mm 5 Pin connector. 25mm hook and loop straps can be used with the extension case. The PCB is based of the [SlimeVR OSHWLab DIY Extension](https://oshwlab.com/eirenliel/slimevr-diy-tracker-extension) changes to make it easier for hand soldering and case fitment. 

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-1.png"  alt="TrackerExtension" width=200px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-2.png"  alt="TrackerExtension" width=180px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-3.png"  alt="TrackerExtension" width=220px /></div>

<div align="center">3.80×1.10×3.19 cm</div>

<br/>



## Components

The components needed have been all added to a Google sheet here with links to each item's store page and total estimated cost.
-  #### [Components BOM Sheet](https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing)

<div align="center"><a  name="logo"  href="https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/render4.png"  alt="Components"></a></div>

<br>



## Assembly

Make sure all PCB's are clean before soldering, can use PCB cleaner or isopropyl alcohol both before and after soldering. The before is to be sure the pads are clean of any oils or films if you are unsure. The after is to remove the flux, which some are acidic and will attack the solder joint over time. Whilst soldering use flux to make things easier, and always keep your solder iron's tip tinned with solder when not in use to protect from oxidation! 

When using header pins, longer end of the pins point upwards toward the component and the shorter end goes into the PCB. Clip off any excess.


Basic steps of assembly for the main trackers is:
  

- [ ] Solder a TP4056 flush to the breakout PCB.
- [ ] Solder BMI/BNO08X module to the PCB with header pins or flush.
- [ ] Solder D1 Mini with included header pins.
- [ ] 1x 180K resistor and 2x 1N5817 diodes soldered in the correct orientation on the PCB.
- - [ ] If using BMI160 modules: Bridge GND>SAO pads on the back of PCB.
- [ ] Solder on a JST PH 2mm 2-Pin header for battery in correct polarity (optional but recommended).
- [ ] Check LiPo's battery JST plug matches the +/- polarity as on the PCB's Header (Fix on the battery plug if not).
- [ ] Solder on a SK12D07VG 4/5/6mm slide switch.
- [ ] Then a ZH 1.5mm 5 Pin header for communication with extension tracker (optional or use on ankle trackers for feet extensions).
- [ ] Use Polyimide tape or equivalent to protect LiPo batteries from sharps, shorts and pins.
- [ ] Connect the battery. Whilst switch in OFF position.
- [ ] Whilst switch in OFF position. Flash firmware using the online firmware flasher or by following the SlimeVR firmware documentation.
  

Basic steps of assembly for the extension trackers:
  

- [ ] Solder on a 0603 100nf capacitor to the extension PCB.
- [ ] Then the ZH 1.5mm 5 Pin header for communication with main tracker.
- [ ] Solder a BMI/BNO08X module flush to the extension PCB.
  
   
<br>



## IMU


LGA14 footprint BMI-160 alternatives such as the BMI-270, BMI360, LSM6, ICM42688, BHI360 etc. can be done with the [LSM6DSV Module by Kounocom](https://github.com/kounocom/LSM6DSV-Module) or by solder work on cheap Aliexpress GY-BMI-160 modules with your desired IC.
This requires you to use a [mini hot plate](https://www.aliexpress.com/w/wholesale-solder-mini-hot-plate.html?g=y&SearchText=solder+mini+hot+plate&sortType=total_tranpro_desc) to prevent the IMU from being melted from other soldering method such as hot air. Begin by placing solder on the module's IMU pads using your soldering iron, clean with IPA, add some fresh flux on the pads and put your replacement IMU on using the hot plate.


<br>



## Resources


Useful Links:


- [Online Firmware Flasher](https://slimevr-firmware.bscotch.ca/)
- [SlimeVR Documentation](https://docs.slimevr.dev/)
- [IMU Rotation](https://docs.slimevr.dev/firmware/configuring-project.html#adjust-imu-board-rotation)
- [CH340 driver](https://www.wemos.cc/en/latest/ch340_driver.html)
- [BMI160 Calibration](https://github.com/SlimeVR/SlimeVR-Tracker-ESP?files=1#bmi160)
- [Github SlimeVR](https://github.com/SlimeVR/)
- [Discord SlimeVR](https://discord.gg/SlimeVR)

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PlacementExample.png"  alt="TrackerPlacement"/></div>