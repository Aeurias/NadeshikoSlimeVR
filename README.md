
<h1 align="center">

<a  name="logo"  href="Misc/logo.png"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/logo.png"  alt="@Nadeshiko's SlimeVR"></a>

<br>

@Nadeshiko's SlimeVR

</h1>

  

Based off the [SlimeVR Official Component Guide](https://docs.slimevr.dev/diy/components-guide.html)

These Slime's run on a Wemos D1 Mini with IMU of your choice that have module profile same as the SlimeVR BNO08Xs or the BMI160's, they use the TP4056 charger for the battery that can work with 3.7V LiPo cells.

  

## Index

  

-  [Components](#components)

-  [PCB](#pcb)

-  [Case](#case)

-  [Assembly](#assembly)

-  [Resources](#resources)

  

### Components

  

#### **[The components needed have been all added to a sheet here with links to each item's store page and total cost.](https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing)**

  

### PCB

  

This PCB lets every component be soldered on without any wires connections between the modules. This includes the diodes and resistor for battery sense and charge protection. They have a TP4056 charger on the back side to save on size, a JST 2mm 2-Pin connector can be added to make battery connections and swaps easier, an SK12D07VG 3-pin switch in 4, 5 or 6mm will be used to turn the tracker on or off, and a ZH 1.5mm 5-pin connector is used for AUX tracker extension communication with SCL and SDA in the same cable layout as the official tracker extension method to avoid crosstalk on long extension cables.

They can also be used without a case, as there is built in slots for straps.

  

PCBs can be ordered from JLCPCB or Elecrow.

  

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PCBFront.png"  alt="R3MiniPCBFront" width=290px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/PCBBack.png"  alt="R3MiniPCBBack" width=290px />&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Extension-PCB-Front.png"  alt="TrackerExtensionPCB" width=190px />

<p align="center">PCB Front/Back - Extension Tracker</p>

  

### Case

  

These tracker cases can house 3.7v LiPo in sizes 503450 or smaller, to 103450 or smaller which has similar runtime to 18650 Li-ion cells but cheaper.

  

They are designed using JLCPCB/JLC3DP resin 3D printing guidelines and tolerances, the cases can be ordered from JLC3DP or Elecrow, the resin to select on your order is up to you. I prefer the **8111X** or **Black Resin** or equivalent.

  

The cases and the tracker extension are 2 part with snap fitting closure, with added extra secureness when strap is used.

  

A snap fitting main body with strap holes on the side, they have ports for the D1 Mini, extension tracker connector and the power switch. The other is the base plate with strap holes on the bottom and PCB stand/aligners, and a port for the TP4056 charger. For the extension tracker is a case with an end cap to close it, strap holes and a port for the connector.

Up to 50mm strap can be fitted to these, best one to use is the non-slip elastic kind with plastic buckles in same size to make it easier to remove as listed in the Google sheet BOM. The strap has few bends through the case to stop any unnecessary slop and keep it locked against the skin.

A gentle curve has been added on the underside of the case matching that of arms, legs or hip, this is to reduce any edges digging into the skin with and increase contact area of the non-slip strap.

  

The variants of the cases are:


  

- **103450 LiPo** - Allows 3.7v LiPo cells up to 10mm thick. Cell dimensions advised are 10x34x50mm or less. *It's the one I recommend as this has best runtime for it's size and the cell's are lowest cost.*

- [ ] 103450-TOP.stl

- [ ] 103450-BASE.stl



<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview1.png"  alt="R3Mini1034501"/></div>

<div align="center">7.03x2.74x5.23cm</div>

<br/>

  

-  **503450 LiPo** - This one allows stacking a 5mm thick 503450 or thinner LiPo cell on top of the breakout PCB and tracker modules. Cell dimensions advised are 5x34x50mm or less.

- [ ] 503450-TOP.stl

- [ ] 503450-BASE.stl



<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/readmepreview2.png"  alt="R3Mini5034501"/></div>

<div align="center">7.03x2.11x5.23cm </div>

 <br/>

- **Tracker Extension** - The tracker extension is also three part, the main case, an endcap and along with the PCB to mount the BMI/BNO module and ZH 1.5mm 5 Pin connector. 25mm hook and loop straps can be used with the extension case. The PCB is based of the [SlimeVR OSHWLab DIY Extension](https://oshwlab.com/eirenliel/slimevr-diy-tracker-extension).

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-1.png"  alt="TrackerExtension" width=200px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-2.png"  alt="TrackerExtension" width=180px /> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Extension/Previews/Extension-3.png"  alt="TrackerExtension" width=220px /></div>

<div align="center">3.80×1.10×3.19 cm</div>

<br/>


<br>

  

### Assembly

  

Basic steps of assembly

  

1. [ ] Solder a TP4056 to breakout PCB.

2. [ ] Solder a BMI/BNO08X to the PCB.

3. [ ] Pins from D1 Mini packaging soldered to the D1 Mini, then set it through the holes on the PCB and solder on backside.

4. [ ] 1x 180K resistor and 2x 1N5817 diodes soldered in the correct orientation on the PCB.

- - [ ] If using BMI160: Bridge GND>SAO pads on the back of PCB.

6. [ ] Solder on a JST PH 2mm 2-Pin battery connector in correct polarity (optional but recommended).

7. [ ] Check LiPo's battery connector matches the +/- polarity as on the PCB! (Fix on the batteries connector if not!).

8. [ ] Solder on a SK12D07VG 4/5/6mm slide switch.

9. [ ] Then a ZH 1.5mm 5 Pin connector for communication with extension tracker (optional/use on ankle main tracker for feet extensions).

10. [ ] Polyimide tape to protect LiPo batteries from PCB and pins (or something equivalent).

11. [ ] Connect the battery. Whilst switch in OFF position.

12. [ ] Flash firmware using the SlimeVR DIY Documentation as guide. Whilst switch in OFF position.
  
   
<br>


  

### Resources

  

Useful Links:

  

-  [SlimeVR Documentation)](https://docs.slimevr.dev/)

  

-  [Github Repository SlimeVR](https://github.com/SlimeVR/)

  

-  [SlimeVR Discord](https://discord.gg/SlimeVR)

  

-  [Online Firmware Flasher](https://slimevr-firmware.bscotch.ca/)

  

-  [CH340 driver](https://www.wemos.cc/en/latest/ch340_driver.html)

  

-  [BMI160 Calibration](https://github.com/SlimeVR/SlimeVR-Tracker-ESP?files=1#bmi160)