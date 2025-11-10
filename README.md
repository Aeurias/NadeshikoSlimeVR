<h1 align="center">
<a  name="logo"  href="Misc/logo.png"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/Previews/logo1.png"  alt="@Nadeshiko's Mini SlimeVR"></a>
@Nadeshiko's Supermini SlimeVR

</h1>

> [!IMPORTANT]
> For the WEMOS D1 Mini variant please view the [D1 branch here](https://github.com/Aeurias/NadeshikoSlimeVR/tree/WEMOS-D1-Mini)


These are one of the smallest WiFi module based SlimeVR trackers possible, similar to [Gorbit99's Tiny Slime](https://github.com/gorbit99/tiny-slime), as small as extension trackers! The idea was for these to be a replacement for wired extension trackers, whose cable can get in the way and are prone to damage, and be a more useable and comfortable size for tracking locations such as shoulders, lower arms, neck, or head.

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
- [Flashing Firmware](#flashing)
- [How to order PCB/3DPrints](#ordering)
- [Support](#support)


## PCB

  

The PCB lets every component be soldered on without any wire connections between the modules. This includes the diodes and resistors for battery sense and charge protection. The ESP32-C3 Supermini is on the back side to save on size and cost; a JST 2mm 2-pin connector can be added to make battery connections easier; an SK12D07VG 3-pin switch will be used to turn the tracker on or off.

  

PCBs can be ordered from [JLCPCB](https://cart.jlcpcb.com/quote/), [Elecrow](https://www.elecrow.com/pcb-manufacturing.html), [PCBGOGO](https://www.pcbgogo.com/pcb-fabrication-quote.html), [NextPCB](https://www.nextpcb.com/pcb-quote#/pcb-quote) or your preferred low cost PCB manufacturer.

  

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/Previews/miniR4-2.png"  alt="Supermini Front" width=290px />&nbsp;&nbsp;&nbsp;&nbsp;<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/Previews/miniR4-1.png"  alt="Supermini Back" width=290px /></div>

<p align="center">PCB Front/Back - 26mm x 38mm</p>


## Cases

The standard tracker case, can house a 3.7V LiPo in 502040 (5x20x40mm) or 602535 (6x25x35mm) size comfortably. Max LiPo cell dimensions are 6x25x40mm. There is also a double battery variant of the case which allows stacking 2x 602535 batteries in parallel for longer runtime but is 5.6mm taller.


The cases has been designed according to [JLCPCB/JLC3DP resin 3D printing guidelines](https://jlc3dp.com/help/article/212-3D-Printing-Design-Guideline). The case can be ordered from [JLC3DP](https://jlc3dp.com/3d-printing-quote) or [Elecrow](https://www.elecrow.com/3d-printing-service.html), and the resin to select on your order is up to you. I prefer the [**9000R**](https://jlc3dp.com/help/article/195-9000R---Photosensitive-Resin), [**CBY**](https://jlc3dp.com/help/article/437-CBY-Photosensitive-Resin), [**Black Resin**](https://jlc3dp.com/help/article/198-Black-Resin--Photosensitive-Resin), or equivalent low cost options..

It prints as two parts: a snap-fit closure with holes for strap, the TP4056 charger and ESP32-C3 USB ports, and the power switch.

25mm strap can be fitted to the cases; the best one to use is the non-slip elastic kind with plastic buckles and tri-buckles in the same size to make it easier to remove, more comfortable and adjustable. Hook and Loop style of strap can also be used.


The files for the standard case are:


- [ ] [NadeshikoSupermini-TOP.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/3D%20Print%20STL/NadeshikoSupermini-TOP.stl)

- [ ] [NadeshikoSupermini-BASE.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/3D%20Print%20STL/NadeshikoSupermini-BASE.stl)

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/Previews/Readme-Preview.png"  alt="MiniPreview"/></div>

<div align="center">30.2mm x 46.0mm × 19.52mm - 8.67cm³</div>


The files for the double stack battery case are:

- [ ] [NadeshikoSupermini-Double-Battery-TOP.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/3D%20Print%20STL/NadeshikoSupermini-Double-Battery-TOP.stl)

- [ ] [NadeshikoSupermini-Double-Battery-BASE.stl](https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/3D%20Print%20STL/NadeshikoSupermini-Double-Battery-BASE.stl)

<div align="center"><img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/Previews/Readme-Preview-Double.png"  alt="MiniPlusPreview"/></div>

<div align="center">30.2mm x 46mm × 25.12mm - 10.13cm³</div>





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
- [ ] Solder the IMU module to the PCB.
- [ ] Solder the ESP32-C3 Supermini module flush to the PCB.
- [ ] Connect or solder on the LiPo battery with the power switch in the OFF position in correct polarity.

Flashing:

- [ ] Power switch still in the OFF position; Flash firmware using the online firmware flasher for BMI-270.
- [ ] When flashing, you want to choose `BOARD_LOLIN_C3_MINI` as the board.
- [ ] In Advanced options, change SDA Pin to `"6"`, SCL Pin to `"7"`, and LED Pin to `"8"`.
- [ ] In Battery Sense section, select `BAT_EXTERNAL`, Shield Resistance to `0`, Battery Shield R1 & R2 to `100`, Battery Sense Pin to `1`.
- [ ] OPTIONAL: Use polyimide tape or equivalent on sharp corners and the LiPo battery to protect it from puncture.
- [ ] OPTIONAL: If using JST PH 2mm 2-pin header. Check battery plug polarity matches the +/- polarity as on the PCB.
- [ ] OPTIONAL: If using Plus variant of ESP32-C3 Supermini, connecting the optional antenna for a more reliable WiFi, requires removing the C3 chip antenna.



<br>




## Detailed-Assembly


#### Step 1 - Resistors and Diodes.
The diodes have an orientation marked by lines, which will match the line on the PCB diode footprint.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-1-ResDio/1.jpg"  alt="1"/>

Solder on the 100K resistors first, any orientation. Flux to make them easier to solder as it helps hold them and easier to clean later.
Add a smidge of solder on one of each of the diodes pads, so it can be the first pad to solder the diodes down to.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-1-ResDio/2.jpg"  alt="2"/>

Should look like this, with the diodes lines facing each other:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-1-ResDio/3.jpg"  alt="3"/>
 

#### Step 2 -  IMU Module.
I'm using the Mumo ICM45686 IMU module here from the SlimeVR store, clamp it down on the backside of the PCB where you did the resistor/diodes with your solder helper clamps. I've added tiny bit of flux on the pads before doing this too:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-2-IMU/1.jpg"  alt="1"/>

Solder the edge castellated holes of the IMU. If your module of choice does not have those and has drill holes, just use a bit more flux and do the holes instead.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-2-IMU/2.jpg"  alt="2"/>

Do both left and right side, and double check visually to make sure there aren't any missed.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-2-IMU/3.jpg"  alt="3"/>


#### Step 3 -  Power Switch
The switch goes on the other side like shown in the image. It has it's footprint there.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-3-Switch/1.jpg"  alt="1"/>

Clamp it flat to the PCB, but still have access to at least one of the legs on the backside of the PCB to solder initially.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-3-Switch/2.jpg"  alt="2"/>

Flux those legs/pins and solder.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-3-Switch/3.jpg"  alt="3"/>

Flux will help pull solder through to the other side, which will make the switch very sturdy:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-3-Switch/4.jpg"  alt="4"/>
 
That does the backside of the PCB, you can clean the excess flux so its not sticky n ewwee for the rest of steps.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-3-Switch/5.jpg"  alt="5"/>


#### Step 4 - ESP32-C3 Supermini Module
There are few Supermini C3 variants out there. The most common of these is the one on the right with the C3 antenna only which works perfectly for these slimes. For this guide, I'm using an C3 Supermini Plus which has the same footprint profile as the normal C3 Supermini, but has an flexible IPEX antenna included with it for improved range. I will also explain later on how to use the IPEX antenna properly on the Plus as it requires a small modification for it to work.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-4-ESP32-C3-Supermini/1.jpg"  alt="1"/>

Soldering the C3 is same as the IMU earlier. Just slightly larger and few more pads. Start with fluxing the pads slightly.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-4-ESP32-C3-Supermini/2.jpg"  alt="2"/>

Clamp down the C3 with your solder helping hands in the correct position, lined up with the footprint on the PCB.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-4-ESP32-C3-Supermini/3.jpg"  alt="3"/>

Solder the edge castellated holes of the C3, both left and right side, and double check visually to make sure there aren't any missed pads.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-4-ESP32-C3-Supermini/4.jpg"  alt="4"/>
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-4-ESP32-C3-Supermini/5.jpg"  alt="5"/>

 
#### Step 5 - TP4056 Unprotected Charger Module
The TP4056 3.7v Lithium battery charging module comes in many sizes and USB styles. You want the uprotected variant with 4 holes:
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-5-TP4056/1.jpg"  alt="1"/>

Flux the PCB pads and even some of the holes on the TP4056 just to make it easier to solder and then clamp it down.
It may not allign with the footprint perfectly like mine, as these come with small variance in dimension between vendors.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-5-TP4056/2.jpg"  alt="2"/>
 
There may be a small overhang on the TP4056, mostly okay, but this can be filed/sanded down if it causes issues with fitment into the case.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-5-TP4056/3.jpg"  alt="3"/>
 

#### Step 6 -  3.7v LiPo Battery
The tracker is basically complete and useable, and can be flashed right away. But we'll continue this guide with the battery. I am using a 602030 battery here that I was able to find super cheap on AliExpress, which is 6mm x 20mm x 30mm as the name states. This Supermini PCB/Case SlimeVR can house up to a 6x25x40mm battery. Thicker batteries like 7mm could fit, but we need a gap between the battery and the inside wall of the case for the strap to pass through.

We need to cut the wire down as it's arrives bit too long. Cut them short around where the arrow is indicated. For smaller batteries you might need a bit more wire, and less for larger batteries, so its fits in the case easier.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-6-Battery/1.jpg"  alt="1"/>

Strip the ends of the cable so we can solder it on the PCB.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-6-Battery/2.jpg"  alt="2"/>

Flux the cable ends and the +/- holes on the PCB and solder it up. Making sure it's correct polarity.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-6-Battery/3.jpg"  alt="0"/>
 
The wires can be shaped/bent around, so the battery sits nicely on top of the modules/USB's.
If wires too long you can redo it and cut it shorter. If too short, you can undo the yellow polymide tape on the battery and redo the wires on it.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-6-Battery/4.jpg"  alt="4"/>

#### Step Optional - ESP32 C3 Supermini Plus IPEX Antenna
For the Plus variant C3 Supermini you must solder a bridge between these two points marked with green arrow to use the IPEX antenna.
This alone is enough to get the antenna to work, however the red C3 antenna must be removed as it causes imperfect impedance matching and signal loss. 
As some power leaks into the unused antenna, this reduces the efficiency and dB of the external antenna. For that, simply de-solder the red arrow marked C3 antenna chip, still have the green point bridged with solder, and attach the IPEX antenna.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Step-4-ESP32-C3-Supermini/6.jpg"  alt="IPEX"/>


<br>

## Flashing

Flashing these Slime's is the same as flashing [Gorbit99's Tiny Slime](https://github.com/gorbit99/tiny-slime?tab=readme-ov-file#flashing). I will show you how to flash it directly from the SlimeVR server and the online firmware flash tool, and how to solve any flashing or WiFi setup issues you may run into.

> [!NOTE]  
> For the online firmware flash tool, which is what I recommened, you can [follow this link](https://slimevr-firmware.bscotch.ca/?config=eyJyZWxlYXNlIjoiU2xpbWVWUi92MC42LjIiLCJib2FyZCI6eyJ0eXBlIjoiQk9BUkRfTE9MSU5fQzNfTUlOSSIsInBpbnMiOnsiaW11U0RBIjoiNiIsImltdVNDTCI6IjciLCJsZWQiOiI4In0sImxlZEludmVydGVkIjp0cnVlLCJlbmFibGVMZWQiOnRydWV9LCJpbXVzIjpbeyJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiSU1VX0lDTTQ1Njg2Iiwicm90YXRpb24iOjI3MCwiaW11SU5UIjoiNSJ9LHsiZW5hYmxlZCI6ZmFsc2UsInR5cGUiOiJJTVVfQk5PMDg1Iiwicm90YXRpb24iOjI3MCwiaW11SU5UIjoiOCJ9XSwiYmF0dGVyeSI6eyJ0eXBlIjoiQkFUX0VYVEVSTkFMIiwicmVzaXN0YW5jZSI6IjAiLCJyMSI6MTAwLCJyMiI6IjEwMCIsInBpbiI6IjEifSwic3dhcEFkZHJlc3NlcyI6ZmFsc2UsImRlYnVnIjp7InVzZTZBeGlzIjp0cnVlLCJvcHRpbWl6ZVVwZGF0ZXMiOnRydWUsImNvbXBsaWFuY2VNb2RlIjp0cnVlLCJibWkxNjBVc2VUZW1wY2FsIjp0cnVlLCJibWkxNjBUZW1wY2FsRGVidWciOmZhbHNlLCJibWkxNjBVc2VTZW5zY2FsIjp0cnVlfX0) with everything already inputted for the flashing. You just need to change the firmware version and select your primary IMU type.
 
 
#### Flashing with the online firmware tool
- [Online Firmware Flasher](https://slimevr-firmware.bscotch.ca/)
- [Online Firmware Flasher Alternative](https://slimevr.shinebright.dev/)

1. You want to be on the latest firmware in the drop down selection.
2. For the board type, you want to choose `BOARD_LOLIN_C3_MINI`.
3. Open **Advanced Options**, change **SDA Pin** to `6`, **SCL Pin** to `7`, and **LED Pin** to `8`.
4. For **Primary IMU**, select the one you have.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Flashing/1.png"  alt="1"/>

Next we do the Battery Sense settings.

5. Click open **Battery Sense (optional)** section, select **Battery Type** as `BAT_EXTERNAL`.
6. Change **Battery Shield Resistance (kOhm)** put `0` .
7. Set **Battery Shield (kOhm)** to `100` for both Battery Shield **R1** and **R2**.
8. For **Battery Sense Pin** set to pin `1`.
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Flashing/2.png"  alt="2"/>

For Wi-Fi settings section and input your 2.4GHz Wi-Fi credentials.

Now on the Supermini. Set it to flashable mode, first double check that it's turned off at the switch, Hold down the left button on it labeled **"BOOT"**, and while holding it down, plug it into your PC. 

After flashing you need to manually reset the Supermini. This can be done by either hitting the reset button labeled **"RST"** or by just unplugging it and powering it on.

If everything went well and your SlimeVR server is turned on, it should be able to connect and appear in there.

<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Misc/Assembly-Supermini/Flashing/3.png"  alt="3"/>

> [!NOTE]  
> Another flash mode method is by holding the **"BOOT"** button, click the **"RST"** and then release **"BOOT"** button

If however it doesn't appear in the SlimeVR server and nothing is showing in the server's serial console, you can use this [Online Serial Terminal](https://terminal.spacehuhn.com/) with the SlimeVR server closed.

Use the serial console if it doesn't appear to connect to WiFi, or set WiFi credentials when flashing, or flashes and working correctly in server when on the USB but not on WiFi.

Use the serial command `SET WIFI XXXX YYYY` where XXXX is your 2.4GHz name, and YYYY is the password, both are case sensitive.

For everything else, use the SlimeVR Documentation, as it contains information for proper SlimeVR server setup, calibration, and wearing.


## Resources


Useful Links:


- [SlimeVR Documentation](https://docs.slimevr.dev/)
- [SlimeVR Github](https://github.com/SlimeVR/)
- [SlimeVR Discord](https://discord.gg/SlimeVR)
- [Online Firmware Flasher](https://slimevr-firmware.bscotch.ca/)
- [Online Firmware Flasher Alt](https://slimevr.shinebright.dev/)
- [SlimeVR-Tracker-ESP](https://github.com/SlimeVR/SlimeVR-Tracker-ESP)
- [SlimeVR-Server](https://github.com/SlimeVR/SlimeVR-Server)


 
<br>


## Ordering

### PCB
Ordering the PCB and 3D Prints is easy. Head to the [releases](https://github.com/Aeurias/NadeshikoSlimeVR/releases) section and download the 3D print .stl files, and the PCB Gerber .zip files.

For PCB ordering, head over to  [JLCPCB](https://cart.jlcpcb.com/quote/) and upload the gerber .zip files. Use the settings below on the order page:
 
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/PCB%20Gerber/orderingPCB.png"  alt="Ordering"/>

They can also be ordered from [Elecrow](https://www.elecrow.com/pcb-manufacturing.html), [PCBGOGO](https://www.pcbgogo.com/pcb-fabrication-quote.html), [NextPCB](https://www.nextpcb.com/pcb-quote#/pcb-quote) or your preferred PCB manufacturer.
 
 
### Cases

For 3D Print case ordering, head over to [JLC3DP](https://jlc3dp.com/3d-printing-quote) and upload the .stl files for each model, including the top/body and base/end cap etc. One case comes in two parts, so make sure you upload both halves. Then use the settings below on the order page and set the quantity of each part to the number of trackers you are building. The available SLA material and prices will vary, as the model has been designed to be used with any of the SLA resins, any of the cheapest option will be good enough for the trackers, 
 
<img  src="https://github.com/Aeurias/NadeshikoSlimeVR/blob/main/Tracker%20Supermini/3D%20Print%20STL/OrderingCases.png"  alt="Ordering"/>

Cases can also be ordered from [Elecrow](https://www.elecrow.com/3d-printing-service.html) or your preferred 3D print services.

<br>

## Support
Feel free to open an issue if you have any questions or to share some pictures! :3
 
You may also DM me on Discord: [@aeurias](https://discord.com/users/240905316013703169), or add on VRChat: [Nadeshiko ~](https://vrchat.com/home/user/usr_f6e358a4-a938-46eb-bfb2-4fee10bd21e5).
