# 5.25" drive bay USB hub

## Why?
My PC case lacks front IO, due to it being from the early 90s. As such, all the USB headers
are located at the back of the motherboard. The pin headers for front IO on my motherboard
are unused, so this project should rectify that.

## What?
The aim is to create a 4-port USB hub, able to be mounted within a 5.25" PC drive bay.
More (semi-)detailed specifications below:
- Have 4 downstream USB 2.0 high-speed capable ports
- Be powered by standard Molex connector (aka 4-pin peripheral power connectors)
- Include current sensing on a port-by-port basis (don't kill all ports if only one overcurrents)
- Need no configuration from the user (work automatically once connected)
- Not to kill my motherboard or power supply

## Current Status
- Schematic designed fully [done]
- Initial PCB layout designed [working]
- First boards manufactured & tested [not yet]
- Revised boards [not yet]
- Outer case designed & printed [not yet]

## Schematic Details
The design is based of the Microchip USB2504, a 4-port USB 2.0 hub controller IC. 
The schematic largely follows the design of the evaluation board schematic, with
changes to limit certain functionality (no LEDs, EVB uses ganged current sensing, etc.)

Note that this schematic uses the TPS2560 for current sensing. The OUT1, OUT2 pins
are mis-assigned in the KiCad library as Output instead of Power Output. Please ignore
any errors generated in the DRC due to this.
