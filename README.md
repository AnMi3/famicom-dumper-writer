# Famicom Dumper/Writer


## Overview

This is simple dumper/writer for Famicom cartridges and Famicom Disc System cards. This version is much faster compared to
the [old one](https://github.com/ClusterM/famicom-dumper). It's using very accurate M2 cycle simulation and usinc FSMC
(Flexible Static Memory Controller) to access PRG and CHR memory. FSMC is precisely synchronized with the M2 clock signal
using CPLD chip. Also new version uses fast on-chip USB controller instead of slow FT232 USB-UART converter.


![Dumper](photos/dumper.jpg)

You can use it to:
* Dump cartridges, so you can play copy of your cartridge on emulator
* Read/write battery backed saves, so you can continue your saved game on emulator/console
* Write special cartridges like [COOLGIRL](https://github.com/ClusterM/coolgirl-famicom-multicard)
* Rewrite ultracheap chinese COOLBOY cartridges. Soldering is required for old versions but it's very simple. New versions can be rewrited without soldering
* Test your cartridges
* Read and frite Famicom Disk System cards using FDS drive with RAM adapter
* Some reverse engineering
* Anything else that requires Famicom bus simulation


## Schematic:

![Schematic](schematic/schematic.png)

Bill of Materials:

![BoM](schematic/bom.png)


## Firmware

You need to write two firmwares: to the STM32 chip using ST-Link programmer and the EPM1270 CPLD chip using USB Blaster programmer.


## Software

[https://github.com/ClusterM/famicom-dumper-client](https://github.com/ClusterM/famicom-dumper-client)
