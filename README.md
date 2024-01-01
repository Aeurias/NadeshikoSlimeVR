
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
- Wall-mountable charging dock.

#### WIP
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

  

The main PCB lets every component be soldered on without any wire connections between the modules. This includes the diodes and resistors for battery sense and charge protection. The TP4056 charger is on the back side to save on size and cost; a JST 2mm 2-pin connector can be added to make battery connections easier; an SK12D07VG 3-pin switch will be used to turn the tracker on or off; and a ZH 1.5mm 5-pin connector is used for extension tracker communication with SCL and SDA in the same cable layout as the official tracker extension method to avoid crosstalk on long extension cables.

The PCB's can also be used without a case, as there are built-in cutouts for straps to pass through.

  

PCBs can be ordered from [Elecrow](https://www.elecrow.com/pcb-manufacturing.html), [JLCPCB](https://cart.jlcpcb.com/quote/), [PCBGOGO](https://www.pcbgogo.com/pcb-fabrication-quote.html), [NextPCB](https://www.nextpcb.com/pcb-quote#/pcb-quote) or your preferred low cost PCB manufacturer.

  

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PCBFront.png"  alt="R3MiniPCBFront" width=290px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PCBBack.png"  alt="R3MiniPCBBack" width=290px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Extension-PCB-Front.png"  alt="TrackerExtensionPCB" width=190px />

<p align="center">PCB Front/Back - Extension Tracker</p>

<br/>



## Case

  

The tracker case, depending on the variant, can house a 3.7V LiPo in sizes 503450 or smaller, or 103450 or smaller, which has a similar runtime to 18650 Li-ion cells but are cheaper.

  

The cases have been designed according to JLCPCB/JLC3DP resin 3D printing guidelines and tolerances. The cases can be ordered from JLC3DP or Elecrow, and the resin to select on your order is up to you. I prefer the **8111X**, **Black Resin**, or equivalent.

  

The cases and the tracker extension are two part with snap-fitting closures, with added extra security once a strap is used.

  

It prints as two parts: a snap-fit main body with strap holes on the side, ports for the D1 Mini, an extension tracker connector, and the power switch. The other is the base plate with strap holes on the bottom, and PCB stand/aligners, and a port for the TP4056 charger.

Up to a 50mm strap can be fitted to the main cases; the best one to use is the non-slip elastic kind with plastic buckles in the same size to make it easier to remove, as listed in the Google Sheet BOM. The strap has a few bends through the case to stop any unnecessary slop and keep it locked against the skin.

A gentle curve has been added on the underside of the case, matching that of arms, legs, or hip; this is to reduce any edges digging into the skin and also increase the contact area of the non-slip strap.

  

The variants of the cases are:


  

- **103450 LiPo:**  Allows 3.7V LiPo cells up to 10mm thick. Cell dimensions advised are 10x34x50mm or less. *It's the one I recommend, as this has the best runtime for its size and the cells' lower cost per Wh compared to other LiPo sizes.*

- [ ] [103450-TOP.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main/3D%20Print%20STL/SlimeVRNadeshikoR3Mini103450-TOP.stl)

- [ ] [103450-BASE.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main/3D%20Print%20STL/SlimeVRNadeshikoR3Mini103450-BASE.stl)



<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview1.png"  alt="R3Mini1034501"/></div>

<div align="center">7.03x2.74x5.23cm</div>

<br/>

  

-  **503450 LiPo:**  This one allows a 5mm-thick 503450 or thinner LiPo cell. Cell dimensions advised are 5x34x50mm or less. *LiPo's for this size are in high demand, so it may be difficult to find good prices.*

- [ ] [503450-TOP.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main/3D%20Print%20STL/SlimeVRNadeshikoR3Mini503450-TOP.stl)

- [ ] [503450-BASE.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main/3D%20Print%20STL/SlimeVRNadeshikoR3Mini503450-BASE.stl)



<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview2.png"  alt="R3Mini5034501"/></div>

<div align="center">7.03x2.11x5.23cm </div>

 <br/>

- **Tracker Extension:** It also has three parts: the main case, an endcap, and the PCB to mount the BMI/BNO module and ZH 1.5mm 5 Pin connector. 25mm hook and loop straps can be used with the extension case. The PCB is based on the [SlimeVR OSHWLab DIY Extension](https://oshwlab.com/eirenliel/slimevr-diy-tracker-extension) changes to make it easier for hand soldering and case fitment. 

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-1.png"  alt="TrackerExtension" width=200px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-2.png"  alt="TrackerExtension" width=180px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-3.png"  alt="TrackerExtension" width=220px /></div>

<div align="center">3.80×1.10×3.19 cm</div>

<br/>



## Components

The components needed have all been added to a Google sheet here with links to each item's store page and total estimated cost.
-  #### [Components BOM Sheet](https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing)

<div align="center"><a  name="logo"  href="https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/render4.png"  alt="Components"></a></div>

<br>



## Assembly

Make sure all PCBs are clean before soldering. You can use PCB cleaner or isopropyl alcohol both before and after soldering. The before is to be sure the pads are clean of any oils or films if you are unsure. The after is to remove the flux, which some are acidic and will attack the solder joint over time. While soldering, use flux to make things easier, and always keep your solder iron's tip tinned with solder when not in use to protect from oxidation! 

When using module header pins, the longer end of the pins points upwards towards the component, and the shorter end goes into the breakout PCB. Clip off any excess.


The basic steps of assembly for the main trackers are:
  

- [ ] Solder a TP4056 flush to the breakout PCB.
- [ ] Solder the BMI/BNO08X module to the PCB with header pins or flush.
- [ ] Solder D1 Mini with included header pins.
- [ ] 1x 180K resistor and 2x 1N5817 diodes soldered in the correct orientation on the PCB.
- - [ ] If using BMI160 modules: bridge GND>SAO pads on the back of the PCB.
- [ ] (optional but recommended) Solder on a JST PH 2mm 2-Pin header for the battery in the correct polarity!
- [ ] Check LiPo's battery JST plug matches the +/- polarity as on the PCB's header (Fix the battery plug if not).
- [ ] Solder on a SK12D07VG 4/5/6mm slide switch.
- [ ] Then a ZH 1.5mm 5 Pin header for communication with an extension tracker (optional or use on ankle trackers for foot extensions).
- [ ] Use polyimide tape or equivalent to protect LiPo batteries from sharps, shorts, and pins.
- [ ] Connect the battery with the power switch in the OFF position.
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
- [CH340 driver](https://www.wemos.cc/en/latest/ch340_driver.html)
- [BMI160 Calibration](https://github.com/SlimeVR/SlimeVR-Tracker-ESP?files=1#bmi160)
- [Github SlimeVR](https://github.com/SlimeVR/)
- [Discord SlimeVR](https://discord.gg/SlimeVR)

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PlacementExample.png"  alt="TrackerPlacement"/></div>
