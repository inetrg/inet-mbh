# inet-mbh
The Modular Board Holder design for the inet-nm from the INET working group.

## Purpose
The goal of this (aside from learning) is to create a stackable, expandable case
to hold the many different types of embedded development kits we use.
We would like to have an easy way to connect and disconnect these development
kits to a server via USB hubs (similar to quick swap HDDs or drives).

## Glossary
- `bc_s` (Board Clip - Single) - A pcb board holder clip fitting a single position.
- `bc_d` (Board Clip - Dual) - A pcb board holder clip fitting a two positions.
- `bh` (Board Holder) - The flat slot that the board and usb will clip into.
- `mbh` (Modular Board Holder) - The overall project.
- `mc` (Modular Container) - The large box that interconnects.
- `src` (Sliding Ratchet Clip) - Is a clip used to fasten the SRH to a specific position acting like the other size  of the zip tie.
- `srh` (Sliding Ratchet Holder) - Holds the center of a USB cable in a position, it has ridges similar to a zip tie that can be used to adjust an axis.
- `umh` (USB Modular Holder)

- ~~`cbc` (Corner Board Clip) - A clip that connects to bh that holds the corner of boards~~
- ~~`sbc` (Side Board Clip) - A clip that connects to bh that holds the side of boards~~
- ~~`ube` (USB Bunny Ears) - The spring mechanism to push the usb cable up~~
- ~~`uc` (USB Cap) - The usb specific cap that clips in over top of the usb casing~~

## Requirements

Software version used to model this:
```
freecad-0.21.1
```

Slicer for the 3D printing:
```
prusaslicer-2.7.1
```

Panel Mount USB connector
```
Manufacturer Product Number: 4055
Manufacturer: Adafruit Industries LLC
url: https://www.digikey.de/en/products/detail/adafruit-industries-llc/4055/10107220
```

USB Hub (has power control with [uhubctl](https://github.com/mvp/uhubctl))
```
Manufacturer Product Number: HU9003V1EBL
Manufacturer: Amazon Basics
url: https://www.amazon.de/-/en/Amazon-Basics-Ports-Power-Adapter/dp/B076YKYHCB/ref=sr_1_1?crid=WG8Y976FZ4DN&keywords=HU9003V1EBL&qid=1695201660&sprefix=hu9003v1ebl%2Caps%2C189&sr=8-1
```

## Flashy Pictures

20 connected with 5 `mc`s offset
![mbh-full-front](./resources/mbh-full-front.jpg)

Different form factor boards
![bh-4-boards](./resources/bh-4-boards.jpg)

Empty `mc`
![mc-empty](./resources/mc-empty.jpg)

All the different pieces:
![bh-ube-uc-cbc-seperated](./resources/bh-ube-uc-cbc-seperated.jpg)

## Roadmap

- Create a "service" where some basic parameters are entered and out pops an
stl for those given parameters.
- Automate releases to provide all the stl files in a reproducible way.
- Add a place to label the `mc` for location
- Add an open PCB
    - 4x USB hub
    - Bussed power
    - Power control
    - Indicator LEDs
    - Bussed communications
