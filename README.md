# OSSM ALT Edition

Alternative community version for the well known [OSSM](https://github.com/KinkyMakers/OSSM-hardware). Consider this experimental. 

![MGN15H version with new clamp](/assets/images/cover.jpg)

<sub>**Notice**: This version was developed without any involvement of the original OSSM / Research and Desire members. However, none of this would have been possible without their prior work which is greatly appreciated.</sub>

## Key Changes:

- Complete redesign around a custom 28V 140Watt USB-C PCB
- Made for [OSSM Rust](https://github.com/orange-gem/ossm-rs)
- Works with MGN15H rails for heavy duty versions
- MGN12H version also available for rebuilds / lighter versions
- The PCB / Motor mount is also compatible with the stock OSSM mechanics
- Supports up to 15MM belts for the MGN15H version and up to 12mm for the MGN12H version. 
- Optimized for assembly in Europe (BOM with very common parts that can easily be sourced)
- Compatible with Pitclamp Mini, but a different version optimized for this design is included. 
- Actual usable travel is rail length - 150mm
  
## BOM:

A comprehensive BOM with descriptions and links has been uploaded as a CSV in this repository. However, the parts below are everything you need for building this complete version:

| Part           | Description                                              | Costs |
| -------------- | -------------------------------------------------------- | ----- |
| 57AIM30        | Motor                                                    | €110  |
| MGN15H Rail    | Rail 40cm                                                | €22   |
| Or MGN12H Rail    | Rail 40cm                                                | €18   |
| 625RS Bearing  | Belt Bearings                                            | €10   |
| M5 Bolts       | Complete kit                                             | €12   |
| M3 Bolts       | Complete kit                                             | €12   |
| Dowel Pins     | Precision pins                                           | €6    |
| GT2 Belt       | 50cm                                                     | €10   |
| GT2 20T pulley | 15mm                                                     | €7    | 
| OSSM 28V PCB   | TBA (self sourced at 20+ quantities can be as low as €10) | €25   |
| **Total**      | Rough approximation. Check BOM for details.              | €215  |

## 3D Printing Tips

500 grams of filament should be enough to complete the whole build including the main pitclamp. It is optimized as much as possible for 3D printing, but some parts still need a small amount of support material for the lip and groove connections which make for a nice and professional fit. Unfortunately, these connections also need quite tight tolerances and nice surface finishes. This is possible with newer printers, but is also unlikely to work with older / worn printers. All tolerances / finishes have been tested to work with a Bambulab A1, Bambulab X1C and a Prusa Core One. Example sliced files with my settings have been added to the repository as well to give you an idea about the positioning of the parts and the support generation. You can directly print them with a Bambulab A1. Printing this with an Ultimaker S5 is confirmed to NOT work. The filament type should not matter for most standard build, but heavy users might want to rely on something sturdier like tough-PLA, PET-G, ASA or PC. The test builds have been printed with standard Bambulab basic PLA (Not matte/silk). 

Main tip: don't spend too much time printing with low layer-heights. It is not necessary. The sliced files use 0.2mm layer height, but early tests have been printed with 0.28mm layer height and looked fine as well. 

![mgn12h version](/assets/images/mgn12.jpg)

<sub> In the print folder there is a version without 'branding' and 1 branded multicolor version as seen above which you can print with a toolchanger / ams type system. You can also print this multicolor version in 1 color (just delete the letter bodies) to add subtle embossed branding on a normal printer.</sub>

## Assembly:

SOON (after extensive testing)

## PCB

![28V PCB](/assets/images/pcb.png)

Image of the PCB the OSSM ALT was designed for. It uses a CH224Q for 28V over usb-c with PD3.2. The board uses a ESP32-C6 for its 'brains' and also incorporates the RS485 controlelr on-board. This means that everything that is necessary for running the OSSM of a usb-c powerbank/walladapter is already on this board. An extra usb-c connector is added for easier debugging and stable power is ensured by panasonic hybrid polymer capacitors. There is also a WS2812 Status LED although that is currently not used by the RUST firmware. The PCB was designed in Kicad 9 and is optimized for easy / cheap assembly by several well-known fabs.

## Licensing:

As open source as possible. Actual license has to be decided in cooperation with OSSM. 