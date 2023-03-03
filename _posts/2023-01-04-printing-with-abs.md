---
layout: post
title: Printing with ABS
date: 2023-01-04
description: 
tags: [3d printing]
---

We are building a [Voron 2.4](https://vorondesign.com/voron2.4) printer at the lab. For this printer, you can order the kit with all the metal parts (screws, extrusions, etc.), electronics, wires, motors, sensors, print bed, etc., but you need to print all the connection details. Voron prepared a guideline for printing. The recommendations are:

- FDM printing
- Using ABS
- Layer height: 0.2mm
- Extrusion width: Forced 0.4mm
- Infill type: Grid, Gyroid, Honeycomb, Triangle or Cubic
- Infill Percentage: 40%
- Solid Top/Bottom Layer: 5

They also recommend not using support but some bridges looked a little bit challenging and could use the help of a little support. Therefore, I tried to limit the use of support to minimal.

We ordered [ESUN ABS+](https://www.esun3d.com/abs-pro-product/), which is based on the modification of ABS material. ABS+ filament has higher mechanical properties, lower odor and lower shrinkage rate than conventional ABS materials.

There are a few things you take into consideration when printing with ABS:

- Toxic fumes: when ABS is melted, it produces toxic fumes. Therefore, you need to have an enclosure with proper ventilation. We are using Prusa i3 MK3S and our printer has the [Ikea Lack modified enclosure](https://www.printables.com/model/17-original-prusa-i3-mk3-enclosure-ikea-lack-table-pr#_ga=2.221114328.1966776611.1677844188-756392080.1666601984). But it was not sealed. We sealed the enclosure and also added ventilation.

- Warping: ABS has high shrinkage rate. Therefore you encounter warping. When we started printing, warping usually occured on the bottom layers, causing the parts to bend away from the print bed on the their edges. We countered this problem by using [glue](https://www.kores.com/product/glue-sticks/).

You can <a href="/assets/images/2023-01-04-printing-with-abs/PrusaSlicer_config_bundle.ini" download>download</a> the Prusa Slicer Config Bundle I prepared for printing with ESUN ABS+ and with Voron's printing recommendations. The file comes with "supports everywhere" you need to change it according to how you want to print it. If you do not want supports, choose **supports: none**; if you want to specify the support locations, choose **supports: for support enforcers only**.