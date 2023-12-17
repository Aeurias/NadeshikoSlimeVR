
<h1 align="center">

<a  name="logo"  href="l"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/logo.png"  alt="@Nadeshiko's SlimeVR"></a>

<br>

@Nadeshiko's SlimeVR

</h1>

  

[Official Component Guide](https://docs.slimevr.dev/diy/components-guide.html)

These Slime's run on a Wemos D1 Mini with IMU of your choice that have module profile same as the SlimeVR BNO08Xs or the BMI160's, they use the TP4056 charger for the battery that can work with LiPo cells and 18650 cells.

  

## Index

  

-  [Components](#components)

-  [PCB](#pcb)

-  [Case](#case)

-  [Assembly](#assembly)

-  [Flashing Firmware](#flashing-firmware)

  

### Components

  

**[The components needed have been all added to a sheet here with links to each item's page and total cost.](https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing)**

  

### PCB

  

This PCB lets every component be soldered on without any wires connections between the modules. This includes the diodes and resistor for battery sense and charge protection.

  

PCBs can be ordered from JLCPCB or Elecrow.

  

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R3%20Mini/Previews/R3Mini-PCB-Front.png"  alt="R3MiniPCBFront" width=250px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R3%20Mini/Previews/R3Mini-PCB-Back.png"  alt="R3MiniPCBBack" width=260px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/TrackerExtension/Previews/Extension-PCB-Front.png"  alt="TrackerExtensionPCB" width=250px />

*PCB Front/Back - Extension Tracker*

  

### Case

  

I've created iterations of the design and uploaded all of them, at first it was similar to the 18650 cell using Frozen Slimes, which then turned to the cheaper LiPo 503450 cells to make it overall less costly trackers.

  

All of these cases use JLCPCB/JLC3DP resin 3D printing guidelines and tolerances, the cases can be ordered from JLCPCB or Elecrow, the resin to select on your order is up to you. I prefer the **8111X** or **Black Resin**.

  

The cases and the tracker extension are 2 part:

  

A snap fitting top cover or main body with strap through holes exits on the side and have port holes, and a snap fitting base plate for the top cover with strap through holes on the bottom and PCB stand/aligners. For the tracker extension is case with an end cap to close it.

  

The variants of the cases are:

  

**503450 & 103450 LiPo's** - These cases use the smaller PCB design that are overall lighter, cheaper to build and print. The LiPo batteries for these can be found for a lot less than the 18650 cells but with basically the same run time for a SlimeVR tracker use:

  

-  **103450 LiPo** - Allows 3.7v LiPo cells up to 10mm thick. Cell dimensions advised are 10x34x50mm or less. *It's the one I recommend as this has best runtime for it's size and the cell's are lowest cost.*

- [ ] R3Mini-103450-TOP.stl

- [ ] R3Mini-103450-BASE.stl



<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview1.png"  alt="R3Mini1034501"/>

<div align="center"> 7.03x2.74x5.23cm </div>

<br/>

  

-  **503450 LiPo** - This one allows stacking a 5mm thick 503450 or thinner LiPo cell on top of the breakout PCB and tracker modules. Cell dimensions advised are 5x34x50mm or less.

- [ ] R3Mini-503450-TOP.stl

- [ ] R3Mini-503450-BASE.stl



<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview2.png"  alt="R3Mini5034501"/>

<div align="center">7.03x2.11x5.23cm </div>

 <br/>

**Tracker Extension** - The tracker extension is also three part, the main **CASE** and an **ENDCAP** and then the **PCB** to mount the BMI/BNO module and ZH 1.5mm 5 Pin connector, this also comes with 2 ways to mount the strap; same as the main case or right through it above the PCB.

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/TrackerExtension/Previews/Extension-1.png"  alt="TrackerExtension" width=200px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/TrackerExtension/Previews/Extension-2.png"  alt="TrackerExtension" width=180px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/TrackerExtension/Previews/Extension-3.png"  alt="TrackerExtension" width=220px />

<br/>


#### *Optional other/old variants:*

  

**103450 LiPo** - This similar to the current 103450, but was larger size and PCB was single sided for modules.

  

- [ ] R2Mini-103450-TOP.stl

- [ ] R2Mini-103450-BASE.stl

  

**503450 LiPo** - Same as above but smaller battery size.

  

- [ ] R2Mini-503450-TOP.stl

- [ ] R2Mini-503450-BASE.stl

  

**18650 Li-ion Cell** - This variant can utilize the 18650 battery cells and cell holder.

  

- [ ] R1-18650-TOP.stl

- [ ] R1-18650-BASE.stl

  

**Thin/Long/Odd LiPo's** - This cases uses the same PCB as the 18650 but without the cell holder to allow thin LiPo to be installed.

  

- [ ] R1-LiPo-TOP.stl

- [ ] R1-LiPo-BASE.stl

  




<br>

  

### Assembly

  

Steps

  

- [ ] TP4056 to Breakout PCB.

- [ ] BMI or BNO08X to the breakout PCB.

- [ ] Pins from Wemos D1 Mini packaging to the D1 Mini, then set it through the holes on the PCB and solder on backside.

- [ ] 180K resistor and 1N5817 diodes in the correct orientation on the PCB.

- [ ] Bridge pads if using BMI160 (no bridge needed for BNO08X).

- [ ] JST PH 2mm 2 Pin battery connector in correct polarity.

-  - [ ] Check LiPo battery connector matches the +/- polarity as on the PCB.

- [ ] SK12D07VG 4/5/6mm slide switch.

- [ ] ZH 1.5mm 5 Pin connector for communication with extension tracker.

- [ ] Polyimide tape to protect LiPo batteries from PCB and pins.

- [ ] Connect battery.
 
  
   
<br>

### Flashing firmware

  

Make sure to install the Slime VR server with drivers first.

If the Slime VR drivers aren't working for you:

  

- [ ] Uninstall the drivers from device manager

- [ ] Extract and install [CH340 driver](https://www.wemos.cc/en/latest/ch340_driver.html)

- [ ] Flash the trackers

  

BMI160 Specific Instructions:

  

- [ ] Use this online [firmware flasher](https://slimevr-firmware.bscotch.ca/) with the latest version of main.

- [ ] Orientation:

  

![BMI160Orientation](https://user-images.githubusercontent.com/98719680/227734508-38e85ab7-38b9-43e7-b7cb-f7d4d2efbc29.png)

  

- [ ] [BMI160 Calibration](https://github.com/SlimeVR/SlimeVR-Tracker-ESP?files=1#bmi160)

  

### Links

  

Resources:

  

-  [The Docs (SlimeVR Documentation)](https://docs.slimevr.dev/)

  

-  [Github Repository SlimeVR](https://github.com/SlimeVR/)

  

-  [SlimeVR Discord](https://discord.gg/SlimeVR)