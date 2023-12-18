
<h1 align="center">

<a  name="logo"  href="l"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/logo.png"  alt="@Nadeshiko's SlimeVR"></a>

<br>

@Nadeshiko's SlimeVR

</h1>

  

Based off the [SlimeVR Official Component Guide](https://docs.slimevr.dev/diy/components-guide.html)

These Slime's run on a Wemos D1 Mini with IMU of your choice that have module profile same as the SlimeVR BNO08Xs or the BMI160's, they use the TP4056 charger for the battery that can work with LiPo cells and 18650 cells.

  

## Index

  

-  [Components](#components)

-  [PCB](#pcb)

-  [Case](#case)

-  [Assembly](#assembly)

-  [Resources](#resources)

  

### Components

  

#### **[The components needed have been all added to a sheet here with links to each item's store page and total cost.](https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing)**

  

### PCB

  

This PCB lets every component be soldered on without any wires connections between the modules. This includes the diodes and resistor for battery sense and charge protection.

  

PCBs can be ordered from JLCPCB or Elecrow.

  

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main//Previews/R3Mini-PCB-Front.png"  alt="R3MiniPCBFront" width=250px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Main//Previews/R3Mini-PCB-Back.png"  alt="R3MiniPCBBack" width=260px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-PCB-Front.png"  alt="TrackerExtensionPCB" width=250px />

<p align="center">PCB Front/Back - Extension Tracker</p>

These PCB's have the TP4056 charger on the back side to save on size, a JST 2mm 2-Pin connector can be added to make battery connections and swaps easier, an SK12D07VG 3-pin switch in 4, 5 or 6mm will be used to turn the tracker on or off, and a ZH 1.5mm 5-pin connector is used for AUX tracker extension communication with SCL and SDA in the same cable layout as the official tracker extension method to avoid crosstalk on long extension cables.

  

### Case

  

I've created iterations of the design and uploaded all of them, at first it was similar to the 18650 cell using Frozen Slimes, which then turned to the cheaper LiPo 503450 cells to make it overall less costly trackers.

  

All of these cases use JLCPCB/JLC3DP resin 3D printing guidelines and tolerances, the cases can be ordered from JLCPCB or Elecrow, the resin to select on your order is up to you. I prefer the **8111X** or **Black Resin**.

  

The cases and the tracker extension are 2 part

  

A snap fitting top cover or main body with strap through holes exits on the side and have port holes, and a snap fitting base plate for the top cover with strap through holes on the bottom and PCB stand/aligners. For the tracker extension is case with an end cap to close it.

50mm strap can be fitted to these, best one to use is the non-slip elastic strap kind and using plastic buckles in same size to make it easier to remove as included in the google sheet BOM. The strap has few bends through the case to stop any unnessary slop or shake when moving and keep it locked against the skin.

A gentle curve has been added on the underside of the case matching that of arms, legs or hip, this is to reduce any digging into the skin with edges and increase contact area of the non-slip strap.

  

The variants of the cases are:

  

Rev 3. **503450 & 103450 LiPo's** - These cases use a smaller PCB design that makes the whole tracker lighter, cheaper to build. The LiPo batteries for these can be found for a lot less than the 18650 cells but with basically the same runtime. The wall thickness tolerances are better also for resin printing.

  

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

25mm hook and loop straps can be used with the extension case.

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-1.png"  alt="TrackerExtension" width=200px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-2.png"  alt="TrackerExtension" width=180px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-3.png"  alt="TrackerExtension" width=220px />

<br/>


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

- [ ] Flash firmware using the SlimeVR DIY Documenation as guide. 
  
   
<br>


  

### Resources

  

Links:

  

-  [The Docs (SlimeVR Documentation)](https://docs.slimevr.dev/)

  

-  [Github Repository SlimeVR](https://github.com/SlimeVR/)

  

-  [SlimeVR Discord](https://discord.gg/SlimeVR)

  

-  [Online Firmware Flasher](https://slimevr-firmware.bscotch.ca/)

  

-  [CH340 driver](https://www.wemos.cc/en/latest/ch340_driver.html)

  

-  [BMI160 Calibration](https://github.com/SlimeVR/SlimeVR-Tracker-ESP?files=1#bmi160)