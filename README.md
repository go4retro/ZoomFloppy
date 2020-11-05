# ZoomFloppy

[![ZoomFloppy PCB (Assembled)](http://www.go4retro.com/wp-content/uploads/2010/12/IMG_2118-Large-223x300.jpg)](http://www.go4retro.com/wp-content/uploads/2010/12/IMG_2118-Large.jpg)ZoomFloppy PCB (Assembled)

## Introduction

ZoomFloppy brings Commodore disk archival into the 21st  Century, bridging the gap between the both the IEEE-488 and IEC-based  disk intelligent Commodore™ disk drive line and contemporary personal  computers. Taking up the baton from the ever-popular X\*-1541 line of  parallel port interfaces, ZoomFloppy provides complete functionality for newer machines running multitasking and multi-user operating systems  and those systems lacking the legacy parallel port upon which the  X\*-1541 interfaces depend.

Designed by Commodore enthusiast Nate Lawson, ZoomFloppy utilizes the ubiquitous [OpenCBM](http://sourceforge.net/projects/opencbm/) Commodore device access libraries and application utilities for  operation. In addition, applications like the VICE Emulator that include OpenCBM support will work with ZoomFloppy as well. Use ZoomFloppy and  VICE to access actual Commodore IEC-based serial devices like the  VIC-1541 disk drive or IEEE-488 based devices like the CBM 8050 from  your emulator!

ZoomFloppy can be used with any OpenCBM supported operating system,  including Unix/Linux/*BSD systems, Macintosh OS X machines, as well as  Microsoft Windows XP, Windows Vista, Windows 7, and Windows 10. OpenCBM developer  Spiro Trikaliotis has provided a convenient installation [manual](http://opencbm.trikaliotis.net/opencbm-8.html) for multi-platform installation. 

ZoomFloppy offers unparalleled performance and robustness for the  serious Commodore enthusiast. Archive data while playing games, writing letters, or listening to videos without any loss of data fidelity.  Designed for the sometimes demanding nature of today’s applications,  ZoomFloppy handles such requirements with ease. ZoomFloppy will find a  cherished home in your Commodore computer setup.

Here’s a talk I gave on ZoomFloppy at the 2011 World of Commodore Expo: https://www.youtube.com/watch?v=RNcVtMDFbOg



## Specifications

ZoomFloppy comprises a circuit board containing an Atmel ATMEGA32U2  microcontroller and support circuitry. The ZoomFloppy interface  includes on board ports for IEC-based disk drives, connectors for the  various Commodore drive parallel cabling systems, and IEEE-488  connectors for future expansion capabilities. The entire unit can be  installed in a standard Hammond plastic enclosure for a truly  professional look. A mini-USB port provides power and PC connectivity.

The [ZoomFloppy Schematic and PCB](http://www.go4retro.com/downloads/ZoomFloppy/ZoomFloppy_PCB_v1.0.zip) are released under GPL v2 in both EAGLE CAD and high resolution PNG file formats.

## Requirements

- PC/Mac with available USB 2.0 port
- USB to mini-USB cable (not supplied)
- IEC disk drive cable (available separately).

## Support

Users can ask questions and discuss their units on the [ZoomFloppy Users](http://groups.google.com/group/zoomfloppy-users) web forum/mailing list, while obtaining more information on software usage via the [OpenCBM](http://www.google.com/url?sa=t&source=web&cd=1&ved=0CB8QFjAA&url=http%3A%2F%2Fsourceforge.net%2Fmailarchive%2Fforum.php%3Fforum_name%3Dopencbm-user&rct=j&q=OpenCBM mailing list&ei=PioxTaiILsOC8gaP_JySCQ&usg=AFQjCNGlR3aicpQ-CuwXIOeiP2u_3X8Rmg&sig2=Rk0b3CW-eDP5HwQT3dLldw&cad=rja) mailing list.

Units come with a 30 days return policy and 1 year warranty.

## Purchase

ZoomFloppy can be purchased at the [RETRO Innovations online store](http://store.go4retro.com/products/ZoomFloppy.html).

## Frequently Asked Questions

### How is the Zoom Floppy different then the XU1541?

- Faster

- 25-second backup without optimizing (parallel transfer, needs cable in drive).
- Still faster even for serial xfers.
- Nibble protected disks

- supports Burst Nibbler protocol via nibtools. Allows raw g64 backups (read and write). Works with vmax/epyx etc etc.
- More reliable

-  interrupt xfers in the middle (^C), start another transfer, and everything gets reset and restarted properly
-  Supports infinite holdoff 
-  Cheap

- currently $35 USD
- IEEE-488 Support

-  ZoomFloppy is one of a few solutions for USB access to the IEE-488 drives, and the only one that understands PET/CBM IEEE commands.
- Future Expansion

- All signals are available on the X5 Expansion Port.
-  only 7 KB used out of 32 KB FLASH on microcontroller

### Can I use the ZoomFloppy to copy D64 images to real disks?

Yes, simply install the OpenCBM software and then use d64copy to transfer D64 images to a real 1541.

### Will ZoomFloppy allow parallel cables to operate?

Yes, ZoomFloppy provides both DB15-M, a 2×8 header, and a 12/24 .156″ connector for various parallel cable options. XAP1541-compatible  cables will plug into the DB15 connector, while old user port cables can connect to the 12/24 edge connector on the board.

### Does RETRO Innovations sell parallel cable kits?

Not yet. RETRO Innovations is planning a parallel cable kit (DB15-F  connector and 6522 daughterboard for the 1541 and a DB15M-F cable), but  current purchasers can create their own cable via Peter Scheper’s [Parallel Cable](http://ist.uwaterloo.ca/~schepers/cables.html) page.

### How does ZoomFloppy compare to a XUM1541 device?

ZoomFloppy is an implementation of an XUM1541-compliant interface.  XUM1541 specifies a protocol that is used to transfer data from the  interface to the OpenCBM libraries. In many cases, the terms can be  used interchangeably, though they do not mean exactly the same thing.  Incidentally, ZoomFloppy is partially named after the “xum” in XUM1541,  which many people pronounce as “zoom” .

### I received the unit and plugged it in, but it does not work. What do I do?

Are you using a USB hub? If so, try plugging the ZF directly into the PC’s USB port and not into the hub. The hub may be flaky or not have  enough current to support all the devices on USB. If so, one thing that  might help is plugging in an external power source to your hub.

### How do I diagnose a drive issue?

1. Connect just one drive via IEC, no parallel. If that doesn’t work at all, it’s probably the drive. Try a different drive.
2. Add the parallel cable (if any) and retest.
3. Add other drives on IEC bus (up to 4 total) one at a time. Make sure each is powered on and attached via a short serial cable. See if each  is detected after adding.

## Copyright

This project's PCB files are free designs; you can redistribute them 
and/or modify them under the terms of the Creative Commons
Attribution-ShareAlike 4.0 International License.

You should have received a copy of the license along with this
work. If not, see <http://creativecommons.org/licenses/by-sa/4.0/>.

These files are distributed in the hope that they will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
license for more details.

