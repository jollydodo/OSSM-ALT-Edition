# OSSM ALT Edition
---
## 🎯 Overview

OSSM ALT Edition is a community-driven alternative version of the well-known [OSSM](https://github.com/KinkyMakers/OSSM-hardware) platform. A lot of time and effort has gone into this project. This has been possible thanks to all the previous work that has been done and several community members that helped test this. Do note that we are still in 'beta testing' phase and that you may run into issues. Please provide feedback to help improve the project. This project represents a ground-up redesign focused on:

- **Modern Power Delivery**: Custom 28V 140W USB-C PCB with comprehensive protection circuits
- **Simplified Assembly**: All-in-one clean design with easily sourceable components
- **European Sourcing**: BOM optimized for availability in Europe
- **Enhanced Performance**: Support for MGN12H and MGN15H rails with support for belts up to 15mm belt.
- **Open Source**: Fully open hardware

***Links***: KM [Discord community](https://kinkymakers.com) & [Ko-Fi](https://ko-fi.com/dododesigns) (for contributions / buying boards)

![MGN15H version with new clamp](/Images/cover.jpg)

<sub>**Notice**: This version was developed without any involvement of the original OSSM / Research and Desire members. However, none of this would have been possible without their prior work which is greatly appreciated. Especially the work of [ArmpitMFG](https://github.com/armpitMFG) has been a great inspiration. </sub>

---

## ✨ Key Features

### Hardware Improvements
- **Custom 28V USB-C PCB** with extensive protection circuits
  - Over/under voltage protection
  - Reverse current protection
  - ESD protection on all exposed ports
  - Inrush current limiting
  - Hybrid polymer capacitors for stable power
  - Brake Chopper Add-On 360Watt
- **Dual Rail Options**
  - MGN15H for heavy-duty applications (up to 15mm belts)
  - MGN12H for lighter builds (up to 12mm belts)
- **Efficient Travel**: Rail length minus 150mm usable stroke
- **Compatible with Pitclamp Mini** and includes optimized alternative design with dowels

### Electronics & Firmware
- **ESP32-S3** microcontroller with integrated RS485 controller
- **WS2812 Status LED** (firmware support pending)
- **Made for [OSSM Rust](https://github.com/orange-gem/ossm-rs)** firmware
- Compatible with step/dir control for original firmware adaptation
- **Optional Brake Chopper PCB** for enhanced safety

### Design Philosophy
- Optimized for 3D printing (minimal supports required)
- Common, easily sourceable components
- Clean, simple assembly
- Comprehensive protection systems

---
  
## 📦 Bill of Materials

A comprehensive BOM with descriptions and links can be found [here](Assembly-Info/BOM-OSSM-ALT.csv). However, the parts below are a quick summary everything you need for building this complete version:

| **Part**           | **Description**                                             | **Costs** |
| -------------- | -------------------------------------------------------- | ----- |
| 57AIM30        | Motor                                                    | €110  |
| MGN15H Rail    | Rail 40cm                                                | €25   |
| Or MGN12H Rail    | Rail 40cm                                                | €21   |
| 625RS Bearing  | Belt Bearings                                            | €15   |
| M5 Bolts       | Complete kit                                             | €12   |
| M3 Bolts       | Complete kit                                             | €12   |
| Dowel Pins     | Precision pins                                           | €10    |
| GT2 Belt       | 50cm                                                     | €15   |
| GT2 20T pulley | 15mm                                                     | €10    | 
| Filament  | Max 500g | €20   |
| OSSM ALT 28V PCB   | Designs available for self-sourcing or buy through me to support this project. | €40   |
| **Total**      | Rough approximation. Check BOM for details.              | €270  |

📋 **[Complete BOM with part numbers and links](Assembly-Info/BOM-OSSM-ALT.csv)**

> **Note**: You will also need a remote control device. Compatible options include:
> - Official R&D remote
> - iOS/Android apps
> - Web control interface
> - M5 Remote (check firmware compatibility)

---

## 3D Printing Tips

500 grams of filament should be enough to complete the whole build including the main pitclamp (350 without). It is optimized as much as possible for 3D printing with only 1 part requiring a small amount of supports. The filament type should not matter for most standard build, but heavy users might want to rely on something sturdier like tough-PLA, PET-G, ASA or PC. The test builds have been printed with standard Bambulab basic PLA (Not matte/silk). 


**Filament Required**: ~500g for complete build including Pitclamp

**Recommended Materials**:
- **Standard Use**: PLA, PLA+
- **Heavy Use**: Tough-PLA, PETG, ASA, PC

**Important**: Follow the [detailed 3D printing guide](Assembly-Info/Print-Manual/README.md) carefully to ensure proper fit and function.

**Print Options**:
- Standard version (no branding)
- Multi-color branded version (AMS/toolchanger compatible)
- Single-color embossed version


![MGN12H Light version](/Images/mgn12.jpg)

---
## Assembly:

📺 **Video Assembly Guides**:
- [Part 1](https://youtu.be/EqzNXQzpHu0) 
- [Part 2](https://youtu.be/FnY4Sz64H2A) 

📖 **Written Assembly Guide**: In development

❓ **Frequently asked**: [How do I install the brake chopper?](#how-do-i-install-the-brake-chopper)

💬 **Need Help?** Join the KM [Discord community](https://kinkymakers.com) for assembly support and questions (Look for the OSSM ALT Project).

---

## 🔌 Main PCB Specifications

Most work has gone into this PCB. My vision for this Machine/PCB is that groups of people will self-source this PCB. From 10+ pieces this makes sense, so as long as you can find 10 people you should be able to buy this at an affordable price. The rest of the machine can be printed and uses off the shelf parts. I will also sell these boards for people that only need 1 PCB and want to help support this project (please not that a lot of my own money has gone into this and any support is greatly appreciated ([Ko-Fi](https://ko-fi.com/dododesigns))

![28V PCB](/Images/pcb.png)

### Technical Features

- **Power**: CH224Q for 28V USB-C PD 3.2 negotiation
- - Continuous 140Watt capable with 4 layer optimized PCB design (load tested)
- **Controller**: ESP32-S3 microcontroller with onboard antenna
- **Communication**: Integrated RS485 controller
- **Power Protection**:
  - Hybrid polymer capacitors
  - Inrush current limiting
  - Over/under voltage protection
  - Reverse current protection
- **Additional Features**:
  - Dedicated USB-C debugging port
  - ESD protection on all exposed ports
  - WS2812 status LED
  - Brake chopper expansion support

**Design Tool**: KiCAD 9  
**Manufacturing**: Optimized for major PCB fabrication houses

### Optional Brake Chopper Add-on

![Brake PCB](/Images/brakepcb.png)

Enhanced protection for heavy-duty use:
- **Dissipation**: 12W continuous, 360W short-term spikes
- **Protection Threshold**: 33V (protects 36V TVS diode)
- **Purpose**: Back-EMF spike suppression
- **Recommended For**: Heavy users and added safety margin

This was mainly a fun side project for me which also adds functionality. It is basically an improved version of a Pololu Shunt Regulator, but completely redesigned with an on-board gate driver, 12V LDO, and 12watts of power resistors (2 sides assembly up to 24watt). This PCB was designed to be very cheap and easy to produce. 

![Assembly PCB](/Images/assemblypcb.png)

> 🔧 **Installing it?** See [How do I install the brake chopper?](#how-do-i-install-the-brake-chopper) in the FAQ.

---

## ❓ FAQ

### How do I install the brake chopper?

There are **two** ways to connect the brake chopper to the main PCB. Both are electrically identical — the brake chopper simply sits in parallel with the motor supply.

#### Option 1: Screw terminal (recommended)

Simply put the brake chopper wires into the **same green screw terminal** as the motor power wires: the red (+) wire together with the motor's red wire, and the black (GND) wire together with the motor's black wire. Twist the two wires of each pair together, insert them into the terminal and tighten the screw.

This requires no soldering on the main PCB at all and is the option I recommend for everyone.

![Brake chopper in the screw terminal](/Images/brakechopper-terminal.jpg)

<video src="https://github.com/jollydodo/OSSM-ALT-Edition/raw/main/Images/brakechopper-install.mp4" controls width="640"></video>

📺 [Watch the short installation video](https://github.com/jollydodo/OSSM-ALT-Edition/raw/main/Images/brakechopper-install.mp4) *(if the player above does not load)*

#### Option 2: Solder to the dedicated pads

If you don't like doubling up wires in the screw terminal, the main PCB has **two dedicated pads on the back** for the brake chopper, marked `Brake` (`VIN` and `GND`). Solder the red wire to `VIN` and the black wire to `GND`.

![Brake chopper soldered to the dedicated pads](/Images/brakechopper-solder.jpg)

> ⚠️ **At your own risk.** This is a 4-layer PCB with large copper planes that pull a lot of heat away from the joint, so you need a decent soldering iron (and patience). Double-check that you have not accidentally bridged anything before applying power.

---
## 🔋 Compatible Power Sources

This design is focused around PD, so it only makes sense to provide some options that are tested.

> **Important**: Use a USB-C cable with E-marker chip for >3A current. Standard cables will limit performance.

### Tested & Confirmed

| Device | Type | Rating | Status | Recommended | Rating | Notes |
|--------|------|--------|--------|-------|------|-----|
| [Apple 140W USB-C Adapter](https://www.apple.com/nl/shop/product/mw2m3zm/a/usb%E2%80%91c-lichtnetadapter-van-140-w) | Wall Adapter | 28V / 5A (140W) | 🔬 Tested | ✅ Recommended| ★★★★★ (5)| Excellent reliability and quality, Only ~€60 (will likely not work with other pcb's besides the OSSM ALT since it requires inrush current protection) |
| [Ugreen 200W Powerbank](https://eu.ugreen.com/products/ugreen-nexode-power-bank-200w-25000mah) | Powerbank | 28V / 5A (140W) | 🔬 Tested| ✅ Recommended|★★★★★ (5)| Great portable option that negotiates with almost any chip. Best power bank I have tested.|
| [Ugreen Nexode 145W Powerbank 25000mAh](https://nl.ugreen.com/products/ugreen-140w-power-bank-145w-max-25000mah-externe-batterij?currency=EUR&country=NL&variant=43580105326791) | Powerbank | 28V / 5A (140W) | 🔬 Tested | ✅ Recommended| ★★★★★ (5)| Tested by community member **Frayd**. Portable option in the same Nexode line as the 200W model above. |
| [Anker 140W Wall Adapter](https://www.anker.com/products/a2697-anker-charger-140w-4-port) | Wall Adapter | 28V / 5A (140W) | 🔬 Tested| ✅ Recommended|★★★★☆ (4)| Works well, but you will definitely feel it get hot at prolonged 140W and after 20 minutes or so it will lower the power to cool down. 100Watts continuous is fine so for the gold motor there are no problems. I have yet to see a supported motor that pulls 140W continuous. 
| [Sitecom 140W Wall adapter](https://www.action.com/nl-nl/p/3221194/sitecom-usb-wandoplader/) | Wall Adapter | 28V / 5A (140W)|🔬 Tested | ✅ Recommended| ★★★★☆ (4) | Cheapest adapter of the list (~€20). Did not do any extensive testing yet, but it negotiates 28V and 20V fine. I was also able to load test it at 140W and you can feel it get warmer similar to the Anker one, but it seems to hold up fine. At it's price point it is probably a very good deal (even comes with a cable), but we don't know if it's easy to source since right now it's sold at 'action' which normally changes its inventory quite quickly. 
| [Ugreen 100W Wall Adapter](https://www.amazon.nl/dp/B091TV6LWN) | Wall Adapter | 20V / 5A (100W) | 🔬 Tested | ⚠️ Lower Power|★★★☆☆ (3) |Works okay, but do notice that this one does not support 28V. If you have the OSSM-Alt pcb at 28V and still try to power it, it will work but negotiates down to 20V. |
| [Framework 180W Adapter](https://frame.work/nl/en/products/16-power-adapter?v=FRANCR000F) | Wall Adapter | 36V / 5A (180W) | 🔬 Tested | ⚠️ Lower Power | ★★★☆☆ (3) | Quality wise I believe this is a good adapter, but it has a lot of difficulty negotiating with several common cheap PD chips. So it won't negotiate above 20V on the OSSM-ALT PCB and it also does not seem to support I2C with this chip either. Therefore, not really recommended unless you already have it and just power a motor at max 100W. 
| Apple 67W Adapter | Powerbank | 20V / 3.3A (67W) | 🔬 Tested | ⚠️ Lower Power | ★★☆☆☆ (2.5) | Negotiates well and also supports I2C negotiation. 67W is however on the lower side, so this is definitely not recommended for heavy usage. Still, this was the adapter I first tested my OSSM with and from my experience 67W is enough for most light play.  |
| Xiaomi Mi 50W | Powerbank | 20V / 2A (40W) | 🔬 Tested | ⚠️ Low Power | ★★☆☆☆ (2) | Not recommended. Negotiates well, but low power. Still for a very light weight OSSM it might. be fine.  |

**Have you tested another power source?** Please share your results!

---

## ❤️ Support the Project

If you've built an OSSM ALT and want to support continued development:

### Financial Support

- **PCB Purchase**: Buy boards from me to support the project (Discord PM, Ko-Fi (soon))
- **Buy a hardware kit**: If there is enough demand, I might start selling some hardware kits 
- **Donations**: [Ko-Fi](https://ko-fi.com/dododesigns) *(or contact me on Discord)*

### Non-Financial Support

- ⭐ **Star this repository** to increase visibility
- 📢 **Share the project** with your community
- 📸 **Share your build** with photos and feedback on Discord
- 📖 **Contribute documentation** and improvements

![teaser](/Images/teaser.jpg)

---


## 📜 License

This project is **Open Source Hardware**.

All hardware design files (including PCB schematics, layouts, and 3D mechanical design files) are licensed under the **CERN Open Hardware Licence Version 2 – Strongly Reciprocal (CERN-OHL-S-2.0)**.

You are free to:
- Use, study, modify, and manufacture this design

Under the following conditions:
- **Attribution** must be given to the original author(s)
- **All modified versions and derivatives must be released under the same license**
- **Complete corresponding source files must be made available**


---

## 🙏 Acknowledgments

Special thanks to:

### Core Contributors
- **OrangeMurker & Nakata** - OSSM Rust firmware development and invaluable feedback
- **Beta Testers** - All community members who tested and provided feedback

### Inspiration & Prior Art
- **[armpitMFG](https://github.com/armpitMFG)** - Front/end effector designs and Pitclamp Mini
- **Original OSSM / R&D Team** - Foundation and inspiration for this project

### Community
- All contributors who have improved this design
- Discord community members providing support and feedback

---


## ⚠️ Disclaimer

This project is currently in **beta testing phase**. While extensively tested, you may encounter issues. Please provide feedback to help improve the project.

**Safety**: This is a DIY project involving motors and electronics. Build and use at your own risk. Ensure all safety precautions are followed during assembly and operation.

---
