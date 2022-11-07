# Configuration files for Marlin 2.1.1 on KP3S with TMC2225 drivers in UART mode
- Based off of [Sample Configuration](https://github.com/MarlinFirmware/Configurations/blob/f52c85b0e3b241f8fabb4a902a4aa53775fdeb93/config/examples/Kingroon/KP3S/Configuration.h)
- Includes changes from https://github.com/bdwilson/KP3S/tree/main/Marlin-2.0.9.3
- Some things I added
  1. Enabled Filament Change (M600)
  2. Rotated Display 180 degrees  (suggest you do a M995 to calibrate)
  3. Set to my Z offset (check EVERY TIME you replace the nozzle)
  4. Includes my PID settings.  Suggest you do a PID calibration right away
  5. TMC2225 are in UART mode

To enable UART mode on the TMC2225 you will have to add a jumper wire from each driver to a header on the motherboard. This sounds scary but if you have basic soldering skills it isn't too bad.  
If you don't know how to solder, you probably don't want to do this.  
Makerbase has a good video on the this, see their [wiki](https://github.com/makerbase-mks/MKS-Robin-Nano-V1.X/wiki/TMC_UART_MODE)
See the [schematic](https://github.com/le3tspeak/Marlin-2.0.X-MKS-Robin-Nano/blob/2ffa19960715aa0fd97bf5f8973691eb2fc0012c/docs/TMC2208SWSERIAL.png) for details but understand the KP3S has nothing in E1 so you don't need to wire that socket.
The **pins_MKS_ROBIN_NANO_common.h** file should go in Marlin/pins/stm32f1/. 

This configuration is for my board which came with TMC2225.  It should work with TMC2208 except the MICROSTEPS in Configuration_adv.h will probably need to be change from 32 to 16.  It might work for TMC2209/TMC2226 but I haven't tested it yet.

Very important:  This configuration has BLTOUCH support using the ZMIN input.  This is not the same as documented on the Kingroon website.  See [3D Touch Installation](https://bubba.org/kp3s/3dTouch/).

## Disclaimer - Warning
**USE AT YOUR OWN RISK** This configuration works on *my* printer. It might not work as-is on yours.

The material and information contained on this blog/website are for general information purposes only. I make no representations or warranties of any kind, express or implied about the completeness, accuracy, reliability, suitability or availability with respect to the website or the information, products, services or related graphics contained on the website for any purpose. Any reliance you place on such material is therefore strictly at your own risk.

Marlin is distruted under the [GPL License](https://github.com/MarlinFirmware/Marlin/blob/e86c78379a4df1351d10d5b1e19312a894cb331b/LICENSE).  This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful but **WITHOUT ANY WARRANTY**; without even the implied warranty of **MERCHANTABILITY** or **FITNESS FOR A PARTICULAR PURPOSE**.  See the GNU General Public License for more details.
