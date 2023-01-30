---
title: "PCB Milling with Modela"
date: 2022-09-27T00:00:00+00:00
author: Asli Aydin Aksan
layout: post
permalink: /pcb-milling-with-modela/
categories: General
tags: [pcb, pcb milling, machines, modela mdx 20, tutorial]
---

![PCB milling](/assets/images/2022-09-27-PCB-milling-with-modela/20220927_150236.jpg "PCB milling")

**Machine: Modela MDX 20**

**Software: Mods**

When you are working with electronics, you can make prototypes with Arduino. However, when you want to embed a programmed microchip in a design you need to design the PCB (Printed Circuit Board) itself to mount.

For this tutorial, we made our own **UART (universal asynchronous receiver-transmitter)**. computer hardware device for asynchronous serial communication in which the data format and transmission speeds are configurable. The UART interface consists of two pins: the Rx and Tx pin. The Rx pin is used to receive data. The Tx pin is used to transmit data. When two devices are connected using a UART, the Rx pin of one device is connected to the Tx pin of the second device.

<img src="/assets/images/2022-09-27-PCB-milling-with-modela/UART.jpg" alt="UART schema" width="50%"/>

Modela bed is made of 4 layers.

![Bed Layers](/assets/images/2022-09-27-PCB-milling-with-modela/BedLayers.jpg "Bed Layers")

Always measure the thickness of the copper plate at several locations and use the thickest measurement.

Clean the sacrificial layer with sticker remover. Fully cover the surface where the copper plate will be placed with double-sided tape but avoid overlaps. Place the copper plate and press firmly on the plate with a or paper towel (avoid touching too much with hands).

---
Useful things to know!

There are two types of copper plates:
- One-sided copper plate: used for surface mount devices (SMD) - this tutorial uses a one-sided copper plate.
- Double-sided copper plate: used for through-hole devices.

Milling bits:
- 0,8 mm thickness: used to make edge cuts
- 0,4 mm thickness: used to make interiors

Flutes on the milling bits:
- 1 flute: Standard (cuts faster; eats away more material at a time) - this tutorial uses a 1-flute milling bit.
- 2 flute: more precise (cuts slower)

We firstly cut the interiors and then the edge cuts.

The design image should have a DPI value of 1000. If it is not the case, you can change this value in Mods later on. In the design image:
- White color: Parts you want to keep
- Black color: Parts you want to remove

---

The files we will use in this tutorial are as follows, first two are interiors and the third is edge cut:

<img src="/assets/images/2022-09-27-PCB-milling-with-modela/Programmer-Serial-D11C-F_Cu.png" alt="UART interior 1" width="33%"/>
<img src="/assets/images/2022-09-27-PCB-milling-with-modela/Programmer-Serial-D11C-USB.png" alt="UART interior 2" width="33%"/>
<img src="/assets/images/2022-09-27-PCB-milling-with-modela/Programmer-Serial-D11C-Edge_Cuts.png" alt="UART edge cut" width="33%"/>

---

Turn ON the machine and make sure it is not in VIEW mode.

![Operation Board](/assets/images/2022-09-27-PCB-milling-with-modela/OperationBoard.jpg "Operation Board")

Open the terminal on the computer the machine is attached to. Go to terminal and type:
- <code>mods</code>
- Cancel the authentication twice

This prompts an explorer page to open with Mods entry. Follow the steps down below to start the machine interface.

![Mods enter](/assets/images/2022-09-27-PCB-milling-with-modela/modsEnter.jpg "Mods enter")

In the Mods screen, follow the steps below to mill your design.

[![Mods job](/assets/images/2022-09-27-PCB-milling-with-modela/Screenshot%20from%202022-09-26%2016-31-46-01.jpg "Mods job")](/assets/images/2022-09-27-PCB-milling-with-modela/Screenshot%20from%202022-09-26%2016-31-46-01.jpg)

[![Mill Raster 2D](/assets/images/2022-09-27-PCB-milling-with-modela/MillRaster2D.jpg "Mill Raster 2D")](/assets/images/2022-09-27-PCB-milling-with-modela/MillRaster2D.jpg)


[![Roland MDX](/assets/images/2022-09-27-PCB-milling-with-modela/RolandMDX.jpg "Roland MDX")](/assets/images/2022-09-27-PCB-milling-with-modela/RolandMDX.jpg)

When the milling is finished Press VIEW on the Operation Board and check everything is good. Once all the milling is done, remove the milled part with a scraper and wash it with soap.

![UART board](/assets/images/2022-09-27-PCB-milling-with-modela/UARTBoard.jpg "UART board")
