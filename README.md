# Marlin 3D printer firmware for the Ender 3.

![marlin](https://img.shields.io/badge/marlin-2.0.9.x-green)

This repository mainly exists to let me build it remotely, because I often use my iPad to edit firmware changes due to my printer's location, so I'm looking for an alternative to rdping in to my main machine.

| Hardware   | Details  | URLs/Notes  | 
|---|---|---|
| Printer  |  Creality Ender-3S (Basically an Ender 3, pre-built, taobao) |   | 
| Sensor   |  Authentic Creality BLTouch  |   |
| Motherboard   |  SKR Mini E3 V2.0  |  5 port configuration, not split 3-2. Plug into the z-probe.  |
| Fan Duct  | Satsana 5015 Remix  | [thingiverse](https://www.thingiverse.com/thing:4647053)  |

All other parts are stock.

I initially used the Creality Silent board (4.2.7), and I eventually switched away, because of several annoying things
- Lack of EEProm, and saving to SDCard didn't work, which meant that I either had to compile firmware for it, or just have to resend my settings everytime
- You can't mount the SDCard through USB, which means that I can't set up a CI/CD pipeline for me to send firmware updates to my ender 3 through the octoprint
- The screw terminals were really bad and my hotend screw terminal broke.

In the end, If you're considering either the 4.2.7 or the E3 v2, I'd say to not waste your money and just get the E3 v2 right off the bat.

If you're changing your motherboard, get a set of ferrules and the ferrule crimpers, cut your wires, and properly crimp your wires with ferrules. Fire hazards aside, the screw terminals hold the ferrules so much better than just the exposed/tinned wires.

# Changes from stock Marlin
- I don't intend to make any crucial changes yet, but primarily
- ABL on the stock marlin firmware provided by BTT was completely fucked on my printer, it thinks that the bed is 10cm above where it actually is, and x/y homing is completely screwed.
- This presets the x/y offsets at the values reccomended in the Satsana, for the z-offset I left it at 0 because I chose to change it through octoprint later and save it to EEProm, with this satsana duct I've found that depending on how tight your belts are it can vary between -1.2x to -1.6x
- The ABL grid mesh is changed to 3x3 instead of 5x5.
- Mostly, the changes in [3DPrintscape](https://www.youtube.com/watch?v=PMG4bC9I3DA)'s video worked for me. I'm still tuning the printer at this point.

