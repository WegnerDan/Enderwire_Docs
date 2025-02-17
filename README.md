# Enderwire Docs
![Enclosed Enderwire](DarkDog_Enderwire_rev2_with_enclosure.png)

**NOTE!!! THIS DOCUMENT IS INCOMPLETE AND A WORK IN PROGRESS!!! MANY ITEMS MAY CHANGE OR BE REMOVED/REWORDED!!!**

# Preface:
This repository outlines the steps to convert your Ender 3 into a CoreXZ movement printer based on the Voron Switchwire. There wasn't really a lot of consolidated information about this so I decided to write it up into a guide.

# Community + Additional Info:
* **Voron Community Discord:** https://discord.com/invite/voron
* Select a Country in the Rules channel to be able to see the **#ender_conversion_chat** thread https://discord.com/channels/460117602945990666/658599170734686219
* Some additional mods can be found in the pinned section in the **#ender_conversion_chat** thread as well

# **Disclaimer!**
**Proceed with caution!** Many steps in a conversion could lead to injury especially when dealing with mains wiring.

Do so at your own risk, I take no responsibility or liability for your own actions, this guide is informational only.

# Prerequisites:
**Start here...**
* Your printer is an Ender 3 with either a 2040 or a 4040 Y-axis extrusion.
* Your printer has a 32-bit mainboard (Creality 4.2.2 or 4.2.7) if you plan to reuse the Creality mainboard.
* You have access to a printer that can print ABS parts (the stock Ender 3 with the white PTFE tube and non-all metal hotend is not recommended or even really safe to print ABS with)
* You are familiar or comfortable enough building a 3D printer from scratch, and are able to figure out how to source your own parts and read documentation.

# Models and Repositories
### – Ender Printable Conversion Parts:
*For Enders with a 4040 y-extrusion:*
* **DarkDog's Rev.2 Conversion:** https://github.com/boubounokefalos/Ender_SW/tree/Rev.2

*For Enders with a 2020 y-extrusion:*
* **Gizzle's Non-Pro Conversion:** https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Gizzle/ender-3_(pro)_switchwire
* **Thomasjfen's Non-Pro-to-DarkDogs Conversion: (to fit Gizzles y-axis into the DarkDog Rev.2 Conversion)** https://github.com/thomasfjen/enderwire_nonpro

If you have a non-pro Ender 3 (aka: the 2040 y-extrusion version) it's recommended to print the majority of DarkDog's parts, and use the y-axis parts from Gizzle or Thomasjfens repositories. (You'll have to mix and match and figure out what will work since the non-pro is not really a mainstream conversion)

**_Cut Guide:_**
You should also download and print [this cut guide](https://www.printables.com/model/329851-2020-extrusion-cut-guide) for use later in the step where you need to cut your x-extrusion down.

**The official Voron recommendations for printing your own parts are:**
* **Material** - ABS (possibly ASA)
* **Layer Height** - Recommended: 0.2mm
* **Extrusion Width** - Recommended: Forced 0.4mm
* **Infill Type** - Grid, Gyroid, Honeycomb, Triangle or Cubic
* **Infill Percentage** - Recommended: 40%
* **Wall Count** - Recommended: 4
* **Solid Top/Bottom Layers** - Recommended: 5

### – Stealthburner Repository:
The Enderwire conversion you can really use whatever hotend and toolhead you can find parts for (again, you'll have to do the legwork to find models and info about these not-commonly-used setups) -- however for the easiest time it's recommended to use the Stealthburner toolhead.

The repository for the Stealthburner toolhead can be found here: https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs

# Parts:
### – Bill of Materials (BOM):
These are the parts that you will need to source (aka: buy) to make the conversion happen.

If you are unsure where to get parts for the BOM - use the official Voron Sourcing Guide to help you get started - https://vorondesign.com/sourcing_guide

**You also need to source all the parts listed in the Stealthburner BOM!!** Found here: https://vorondesign.com/voron_stealthburner

**Notes:**
* Fasteners quantities include an additional 10% over what is required just in case.  (I tried my best consolidating the various user-created fastener BOMs, so the counts/bolt types may not be totally accurate.)
* The Linear Rails, you only need 4 if you are doing a non-pro conversion).
* The Drag Chain, usually ONE chain will do, but you'll need to buy 2 additional *sets* of ends for it then.

**Printed Parts**
|Part|Quantity|
|----------|----------|
|Gantry, Electronics|All|
|Aesthetic (Grills, Extensions, Panel Mounting, Misc)|All|
|Toolhead (Stealthburner)|All|

**Electrical Parts**
|Part|Quantity|
|----------|----------|
|16awg Silicone Wire (mains to PSU)|12 feet|
|24awg Silicone Wire (5v PSU to Pi)|6 feet|
|18awg FEP/PTFE Wire (Heatbed to MCU)|6 feet|
|20awg FEP/PTFE Wire (MCU to Toolhead Heater)|100 feet|
|24awg FEP/PTFE Wire (MCU to Toolhead)|12 feet|
|24awg FEP/PTFE Wire (Heatbed limit switch and thermistor)|12 feet|
|Mean Well RS-25-5 PSU (For RPi)|1|
|Mean Well LRS-350-24 (Optional, recommended)|1|
|Axial Fan 6040 or 6020 24v (chassis fan)|1|
|Raspberry Pi 3b+ or better|1|
|Bigtreetech SKR Mini E3 v3 (Optional, recommended)|1|
|Omron TL-Q5MC2 - NPN Inductive Probe|1|
|SPDT KW10 Limit Micro Switch (X and Y limit switches)|2|
|BAT85 Diode|1|
|NEMA17 Stepper Motor 17HS15-1504S1 (Optional, recommended)|3|
|Mini 12864 Display (Optional)|1|
|LED Strip 240mm 24v (Optional)|2|
|Inlet Power Socket IEC320 C14 (Optional, recommended)|1|

**Fasteners + Hardware**
|Part|Quantity|
|----------|----------|
|m3x5x4 Heat Set Inserts|100|
|2020 m3 Roll-in T-nuts|50|
|2020 m5 Roll-in T-nuts|75|
|m3 x 8mm Socket Head Cap Screws|90|
|m3 x 10mm Socket Head Cap Screws|2|
|m3 x 12mm Socket Head Cap Screws|35|
|m3 x 16mm Socket Head Cap Screws|12|
|m3 x 20mm Socket Head Cap Screws|5|
|m3 x 25mm Socket Head Cap Screws|10|
|m3 x 30mm Socket Head Cap Screws|20|
|m3 x 40mm Socket Head Cap Screws (???)|10|
|m3 x 50mm Socket Head Cap Screws (???)|5|
|m4 x 20mm Socket Head Cap Screws|5|
|m5 x 40 Socket Head Cap Screws|10|
|m3 x 6mm Button Head Cap Screws|5|
|m4 x 6mm Button Head Cap Screws|5|
|m5 x 10mm Button Head Cap Screws|35|
|m5 x 16mm Button Head Cap Screws|35|
|m5 x 20mm Button Head Cap Screws|5|
|m5 x 30mm Button Head Cap Screws|5(+10 for Ender3 V2)|
|m3 x 6mm Flat Head Cap Screws|20|
|m3 x 8mm Flat Head Cap Screws|5|
|m2 x 10mm Self Tapping Screws|10|
|m3 Washers|10|
|m5 x 2mm ABS Spacers/Washers|20|
|m5 x 1mm Shims|25|
|m3 Nylock Nuts|4|
|m4 Nylock Nuts|4|
|m5 Nylock Nuts|4|

**Motion System**
|Part|Quantity|
|----------|----------|
|Linear Rail 12H 300mm, Stainless Steel LDO-SLR12H-300|5|
|F695-2RS Bearings|20|
|Key-bak **Super48** - 13oz - 36"|1|
|Pulley, 2GT, 20T, (5mm ID 6mm W)|3|
|Gates Open Belt, 2GT, 6mm|4 meters|
|Drag Chain, 10x10mm, R18, 15 links|1|
|Drag Chain, 10x10mm, R18, 18 links|1|
|Drag Chain, 10x10mm, R18, 26 links|1|

**Toolhead**
|Part|Quantity|
|----------|----------|
|PTFE Teflon Tube (4mm OD 2mm ID) - 10cm|1|
|PTFE Teflon Tube (4mm OD 3mm ID) - 1.2m|1|

**Enclosure and Deck**
|Part|Quantity|
|----------|----------|
|6x3mm Neodymium Magnets|10|
|3M VHB Tape (3/4")|1 roll|
|Acrylic Panel(s)|???|
|ACM or ABS Panels|???|

### – Reuseable Parts:
These are the parts that you will reuse from your existing Ender 3 (assuming it is a stock Ender 3, if you replaced stuff, your mileage may vary)

* **Frame** - all parts of your Ender 3 frame will be used for the conversion -- **NOTE:** The x-axis extrusion will need to be cut shorter. Details to follow.
* **Mainboard** (MCU) - if you have the v4.2.2 or v4.2.7 32-bit Creality mainboard, that will be enough for the conversion
* **Power Supply** - the stock 350w 24v 15a power supply will be good enough
* **Stepper Motors** - you will only need the X, Y, and Z motors. The extruder motor is not used (see Stealthburner section)
* **Power Inlet** - this is the part where you plug the power cord into the Ender. It will be needed to complete the conversion.
* **Hotend** - Sort of. You *can* get away with this hotend, but it's recommended to get an e3d v6 or better hotend.
* **Heatbed and Heatbed Y-Carriage** - The heatbed is actually pretty good (Note: You will have to drill out your y-carriage if you have the Non-Pro Ender 3 with the 2040 Y-axis extrusion)

# The Build:
To get an idea of what is involved in a build, it is highly recommended that you pre-read the official Switchwire assembly manual, as it will contain a **LOT** of information that will be relevant when performing your Enderwire conversion.

The manual can be found here: **https://github.com/VoronDesign/Voron-Switchwire/raw/master/Manuals/Assembly_Manual_SW.pdf**

----------- WORK IN PROGRESS -- TO BE ADDED -------------

MY STEP ORDER FOR ASSEMBLY ARE A LITTLE UNUSUAL BUT MAKE SENSE TO ME SO...

### – The Teardown:
* Steps to tear down the stock Ender 3... (or leave people to figure that out on their own?)

### – Grill Assembly - Front

### – Grill Assembly - Rear

### – Extensions Assembly - Left

### – Extensions Assembly - Right

### – Skirt Assembly - Left

### – Skirt Assembly - Right

### – Electrics Bay
**_Mounting 350w PSU:_**
* ...

**_Mounting 5v PSU:_**
* ...

**_Mounting Mainboard:_**
* ...

**_Mounting Raspberry Pi:_**
* ...

### – Y-Axis
**_Motor Mounting:_**
* ...

**_Idler Mounting:_**
* ...

**_Linear Rail Mounting:_**
* Install left side rail
* Install right side rail
* Install y-axis limit switch
* Install bed to carrier adapter
* Install y-axis belt and clamp

**_Bed Carriage Preparation and Mounting:_**
* Drilling bed carriage (ONLY if you have the 2040 y-extrusion, aka: the Non-Pro Ender 3)
* Installing drag chain guide
* Mounting carriage to carrier adapter

**_Hotbed Mounting and Pre-wiring:_**
* ...

### X-Axis
