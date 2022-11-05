# Configuration files for Marlin 2.0.9.3 on KP3S
- Based off https://github.com/bdwilson/KP3S/tree/main/Marlin-2.0.9.3
- Some things I added
  1. Enabled Filament Change (M600)
  2. Set to my Z offset (check EVERY TIME you replace the nozzle)
  3. Includes my PID settings.  Suggest you do a PID calibration right away

Very important:  This configuration has BLTOUCH support using the ZMIN input.  This is not the same as documented on the Kingroon website.  See [3D Touch Installation](https://bubba.org/kp3s/3dTouch/).

## Disclaimer - Warning
**USE AT YOUR OWN RISK** This configuration works on *my* printer. It might not work as-is on yours.

The material and information contained on this blog/website are for general information purposes only. I make no representations or warranties of any kind, express or implied about the completeness, accuracy, reliability, suitability or availability with respect to the website or the information, products, services or related graphics contained on the website for any purpose. Any reliance you place on such material is therefore strictly at your own risk.

Marlin is distruted under the [GPL License](https://github.com/MarlinFirmware/Marlin/blob/e86c78379a4df1351d10d5b1e19312a894cb331b/LICENSE).  This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful but **WITHOUT ANY WARRANTY**; without even the implied warranty of **MERCHANTABILITY** or **FITNESS FOR A PARTICULAR PURPOSE**.  See the GNU General Public License for more details.
