# PaneledOpenRectangle
RaspberryPi Pico-powered panels for a stickless controller
  

![image](https://github.com/Armastardo/PaneledOpenRectangle/blob/main/Pictures/KicadRender.png)

Design files are available in this repository. Instructions are still being developed.

![image](https://github.com/Armastardo/PaneledOpenRectangle/blob/main/Pictures/FinishedProduct.png)

## Case

The case requieres 5 different acrylic thickness. 1.5 mm, 3 mm, 5 mm, 6 mm and 8 mm. If you can't source those sizes at least make sure to use 1.5 mm of a different material for the plate since the switches won't clip in otherwise. The 3 mm standoffs are for screwing the pcb to the plates with the 3 mm screws. The 20 mm standoffs are for joining the pieces together.

If you're not using the same acrylic thickness, please adjust this 20 mm accordingly: the sum of the internal pieces, which was 20.5 mm, and you take .5 mm less. Ex: A 22 mm case, should use 15 mm standoffs (assuming the top and the bottom pieces are both 3 mm).

## Ordering

![image](https://github.com/Armastardo/PaneledOpenRectangle/blob/main/Pictures/PCBWayLogo.png)

![image](https://github.com/Armastardo/PaneledOpenRectangle/blob/main/Pictures/SponsoredPCB.png)

A round of prototypes for this project was sponsored by PCBWay. They make really good looking PCBs and have a lot of options on colors and finishes. I'd recommend checking them out. https://www.pcbway.com/

(PCB Folder > Production)

If you're soldering everything by hand, you can use the complete panel and source the parts. Pick whatever color you want and make sure you write "5" in the Different Design section for PCB Specifications. You'll get an additional charge if you don't and it's usually a couple of extra bucks for that.

If you're not soldering everything by hand, please use the individual gerbers to get a quote. This way you can save on costs since PCBA on a paneled board is super expensive. You only need them to solder the USB port and the Schottky diode to the board. You'll end up with 5 of each part anyway since that's the minimum order.

Upload individual gerbers, select the color, leave everything else as is and save them one by one to the cart.

## How to?

This is not a begginners build by no means. Requires a bit of soldering and using the cables can be finicky. My process for this build was:
- Test the pico and drop the firmware.
- Solder the pico on the board with the USB C port + diode and make sure it works (remember the pads on the back for the USB data lines).
- Test again the pico now via the USB C port
- Solder the headers to all of the panels (back side).
- Solder the hotswap sockets.
- Screw the panels to the 1.5 mm layer with the standoffs.
- Place your switches.
- Assemble the case from the top part.
- Connect everything with the duponts.
- Tidy up your cables.
- Close with the bottom layer and screw only a couple of the screws.
- Test again and see if every switch works. Use a multimeter if you're unsure if it is the switch with bend pins or the dupont connection.

## Materials

Necessary pieces:
- 16 x m2x6mm screws - https://aliexpress.com/item/32894693182.html
- 30 x m2x3mm screws - https://aliexpress.com/item/1005004462700273.html 
- 15 x m2x3mm standoffs - https://aliexpress.com/item/32894693182.html
- 20 x m2x20mm standoffs - https://aliexpress.com/item/32894693182.html
- 20 x [Circle Keycaps by Rana Sylvatica](https://github.com/rana-sylvatica/circle-keycaps)
- 20 x Kailh Hotswap Sockets - https://aliexpress.com/item/4001051840976.html
- 14 x 10 cm Dupont connectors (or cable) - https://aliexpress.com/item/4000848184096.html
-  9 x 20 cm Dupong connectors (or cable) - https://aliexpress.com/item/4000848184096.html
- Angled pin headers (not needed if using cable) - https://aliexpress.com/item/32887929634.html
- 20 x MX Switches of your choice
-  1 x Raspberry Pi Pico

If you're not using a PCBA service:
- Schottky Diode (1N5817)* - https://aliexpress.com/item/32800896118.html
- 24 Pin USB C Port* - https://aliexpress.com/item/4001076268359.html

If you're planning on using a GCC cable you don't need neither the diode nor the USB C port.

## Firmware

I'd recommend using either [HayBox](https://github.com/JonnyHaystack/HayBox/) or [pico-rectangle](https://github.com/JulienBernard3383279/pico-rectangle).