# Marlin 3D printer firmware for the Ender 3.

This repository mainly exists to let me build it remotely, because I often use my iPad to edit firmware changes due to my printer's location, so I'm looking for an alternative to rdping in to my main machine.

| Hardware   | Details  | URLs  | 
|---|---|---|
| Printer  |  Creality Ender-3S (Basically an Ender 3, pre-built, taobao) |   | 
| Sensor   |  Authentic Creality BLTouch  |   |
| Fan Duct  | Satsana 5015 Remix  | [thingiverse](https://www.thingiverse.com/thing:4647053)  |

All other parts are stock.


# Changes from stock Marlin
- I don't intend to make any crucial changes yet, but primarily
- ABL on the stock marlin firmware provided by BTT was completely fucked on my printer, it thinks that the bed is 10cm above where it actually is, and x/y homing is completely screwed.
- This presets the x/y offsets at the values reccomended in the Satsana, for the z-offset I left it at 0 because I chose to change it through octoprint later and save it to EEProm, with this satsana duct I've found that depending on how tight your belts are it can vary between -1.2x to -1.6x
- The ABL grid mesh is changed to 3x3 instead of 5x5.
- Mostly, the changes in [3DPrintscape](https://www.youtube.com/watch?v=PMG4bC9I3DA) worked for me. I'm still tuning the printer at this point.
