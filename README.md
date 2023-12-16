# ![](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/logo.png)
# @Nadeshiko's SlimeVR

These Slime's are similar to Frozen Slime's and use a Wemos D1 mini's with IMU of your choice that have profiles same as the SlimeVR BNO08Xs or the BMI160's, they utilize the TP4056 charger.

[Offical Component Guide](https://docs.slimevr.dev/diy/components-guide.html)

## Index

- [Components](#Components)
- [PCB](#PCB)
- [Case](#Case)
- [Assembly](#Assembly)
- [Flashing Firmware](#Flashing-firmware)



### Components
**[The components needed have been all added to a sheet here with links to each item's page and total cost.](https://docs.google.com/spreadsheets/d/1Np8FZpWfbQaHiXM6Y5nCLdoeBbmQeeP_hg5ss5rDM44/edit?usp=sharing)**


### PCB
This PCB lets every component be soldered on without any extra wires. This includes the diodes and resistor for battery sense and charge protection.

To order the PCBs go to a website like https://cart.jlcpcb.com/quote upload the gerber file zip file and select quanity and color and order. It should autoselect all the other correct options when you upload the gerber file.

![PCB R3 Mini](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R3%20Mini/Previews/R3Mini-PCB-Front.png)

  

### Case

I've created and iterations of the file and uploaded all of them, at first it was similar to the 18650 Frozen Slimes, which then turned to the cheaper to make and overall less costly trackers with the LiPo pouch battery cells found on Ali Express.

The cases and including the tracker extension are 2 part:


**TOP** - Snap fitting top cover with strap through holes exits on the side and have port holes.
**BASE** - Snap fitting base plate for the top cover with strap through holes on the bottom and PCB stand/aligners.

Rev 3. variants of the cases are:

**503450 & 103450 LiPo's** - These cases use the R2 or R3 Mini* PCB's they are smaller, lighter and cheaper to build and print and the LiPo's can be found for a lot less than the 18650 cells but with basically the same run time:

- **103450** - This similar to the 503450, but allows LiPo cells upto 10mm thick. Cell dimensions advised are 10x34x50mm. *It's the one I recommened as this has best runtime for it's size and the cell's are lowest cost.*
- [ ] R3Mini-103450-TOP.stl
- [ ] R3Mini-103450-BASE.stl
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R3%20Mini/Previews/R3Mini103450-1.png"  alt="R3Mini1034501"/>

- **503450** - This one allows stacking a 5mm thick 503450 or thinner LiPo cell on top of the breakout PCB and tracker modules. Cell dimensions advised are 5x34x50mm.
- [ ] R3Mini-503450-TOP.stl
- [ ] R3Mini-503450-BASE.stl
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R3%20Mini/Previews/R3Mini503450-1.png"  alt="R3Mini5034501"/>


<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R1/Previews/R1-PCB-Front.png"  alt="R1PCB"/>
R3 Mini PCB to fit in the above cases.


<br/>
<br>

Rev 2. Variants:

**103450** - This variant can utilise the 18650 battery cells and cell holder, large in dimensions...
- [ ] R2Mini-103450-TOP.stl
- [ ] R2Mini-103450-BASE.stl
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R2%20Mini/Previews/R2Mini-103450-1.png"  alt="R2Mini103450"/>

**503450** - This cases uses the same PCB as the 18650 but without the cell holder to allow thin long LiPo to be installed.
- [ ] R2Mini-503450-TOP.stl
- [ ] R2Mini-503450-BASE.stl
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R2%20Mini/Previews/R2Mini-503450-1.png"  alt="R2Mini503450"/>

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R2%20Mini/Previews/R2Mini-PCB-Front.png"  alt="R2MiniPCB"/>
R2 Mini PCB to fit in the above cases.


<br/>
<br>


Rev 1. Variants:

**18650** - This variant can utilise the 18650 battery cells and cell holder, large in dimensions...
- [ ] R1-18650-TOP.stl
- [ ] R1-18650-BASE.stl
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R1/Previews/R1-18650-1.png"  alt="R118650"/>

**LiPo** - This cases uses the same PCB as the 18650 but without the cell holder to allow thin long LiPo to be installed.
- [ ] R1-LiPo-TOP.stl
- [ ] R1-LiPo-BASE.stl
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R1/Previews/R1-LiPo-1.png"  alt="R1LiPo"/>

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/R1/Previews/R1-PCB-Front.png"  alt="R1PCB"/>
R1 PCB to fit in the above cases.

**Case R# is just a revision for the iterations I did over time to adjust or improve them, the bigger the number, the newer it is.*
<br/>
**Tracker Extension** - The tracker extension is also three  part, the main **CASE** and an **ENDCAP** and then the **PCB** to mount the BMI/BNO module and ZH 1.5mm 5 Pin connector, this also comes with 2 ways to mount the strap; same as the main case or right through it above the PCB.

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/TrackerExtension/Previews/Extension-1.png"  alt="TrackerExtension"/> <img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/TrackerExtension/Previews/Extension-PCB-Front.png"  alt="TrackerExtensionPCB"/>

All of these cases use JLCPCB/JLC3DP resin 3D printing guidelines and tolereances, the cases can be ordered from JLCPCB or Elecrow, the resin to select on your order is up to you. I prefer the **8111X** in Pure White or **Black Resin**.

<br/>
<br>
  

### Assembly

Steps
- [ ] TP4056 to Breakout PCB.
- [ ] BMI or BNO08X to the breakout PCB.
- [ ] Pins from Wemos D1 Mini packaging to the D1 Mini, then set it through the holes on the PCB and solder on backside.
- [ ] 180K resitor and 1N5817 diodes in the correct orientation on the PCB.
- [ ] Bridge pads if using BMI160 (no bridge needed for BNO08X).
- [ ] JST PH 2mm 2 Pin battery connector in correct polarity.
- - [ ] Check LiPo battery connector matches the +/- polarity as on the PCB.
- [ ] SK12D07VG 4/5/6mm slide switch.
- [ ] ZH 1.5mm 5 Pin connector for communication with extension tracker.
- [ ] Polyimide tape to protect battery from anything sharp/shorts.
- [ ] Connect battery.

 
### Flashing firmware

Make sure to install the Slime VR server with drivers first.
If the Slime VR drivers arent working for you:

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
- [The Docs (SlimeVR Documentation)](https://docs.slimevr.dev/)
- [Github Repository SlimeVR](https://github.com/SlimeVR/)
- [SlimeVR Discord](https://discord.gg/SlimeVR)