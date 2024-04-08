## What is this fork?

This is a fork of the original Grumpy where instead of the lower pinky key, upper pinky key is used.
This is similar to the [Hummingbird keyboard](https://github.com/PJE66/hummingbird)'s key layout.
(Also see the [awesome-hummingbirds](https://github.com/jcmkk3/awesome-hummingbirds) list!)

Compared to the original repo, the changes are:
- Modified [`case/grumpy_case_build123d.py`](case/grumpy_case_build123d.py):
  - Moved pinky key stagger up
  - Added bumpon locations to the bottom corners
  - Added a USB cutout so controller can fit
- Replaced [`prod/case/grumpy.stl`](prod/case/grumpy.stl) with the export of the above script
  - Note: The file in the original repo doesn't seem to be a direct export, since it is hollowed out on the bottom (via some post-processing?)

What is **not changed** and thus is incompatible with above:
- PCB files
- Firmware files

I built one with the modified case and handwired it to a Xiao using per-key PCBs.

### Pictures

![grumpy](https://github.com/caksoylar/Grumpy/assets/7876996/462c3a0c-0b0a-4231-99af-fba80e3f8a7c)
![grumpy2](https://github.com/caksoylar/Grumpy/assets/7876996/9f202d73-1733-4714-9ed7-8b38ccd2d00c)
![IMG_5391](https://github.com/caksoylar/Grumpy/assets/7876996/a59af8d1-7c42-4f42-8bfa-96f20ef8aa9c)


## Original README

### grumpy

28 key (3-row) angled unibody keyboard with col stagger 

![top](img/grumpy.png)

## Features

- Hotswap sockets (MX)
- Seeed Xiao Controller
	- RP2040 (w/ QMK, Vial)
	- BLE (w/ZMK)
	- SAMD21 (should work, don't have one to test)
- gerber and case files are supplied (kicad files, stl as well as cadquery files)
- completely open source, permissive license ([CERN-OHL-P](https://cern-ohl.web.cern.ch/home))

## Want one?

All production files you need to build your own board can be found [here](./prod/).

The case has no bottom and ends right below the HS Sockets. You may either use it as is, but preferably use some 2-3mm self-adhesive neopren on the whole pcb. The case will be hard to print on a FDM Printer, so maybe use a service to print it in resin or nylon.

Apart from the pcb and optionally a case you need:
- 28 hotswap sockets
- 28 diodes (1N4148 int SOT-123)
- 28 of your favourite switches
- 1 Controller

### firmware
firmware configs for qmk and vial can be found in the [firmware folder](./firmware).

The first time the pcb is plugged in, the bootloader will provide a drive to upload the firmware file. 

### the rest

Everything in this repository is free to use however you might see fit. If you want to support me and my projects, please consider linking back to this repository if you build/change/use anything.

If you would like to send me a tip, you could do it [here](https://ko-fi.com/weteor) (Please don't feel like you have to).

### more pictures

![top](img/grumpy_mjf.png)
