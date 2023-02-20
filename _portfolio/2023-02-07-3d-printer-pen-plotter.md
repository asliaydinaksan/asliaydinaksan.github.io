---
layout: post
title: 3D Printer Pen Plotter
tags: [3d printing, rhinoceros, grasshopper]
img: /assets/imagesPortfolio/2023-02-07-pen-plotter/penPlotter.gif
---

The project explores plotting with pen on the Creality Ender 3 printer. The advantage of plotting on a 3d printer is taking advantage of the z-axis of the printer and making non-linear curves, thus changing line thicknesses.

The pen holder for the plotter was designed in Rhinoceros and the gcode generation was created in Grasshopper.

## The Pen Holder

The observation of Creality Ender 3's extruder head indicated to three locations where the pen holder could attach to with minimal intervention to the extruder. I decided to remove the existing screw on the head at point 1 and attach my pen holder at that point (this is the only alteration made to the printer). I also wanted to add clip connection for point 2 and point 3 for extra support so that the pen would not move while in operation.

![pen holder fix](/assets/imagesPortfolio/2023-02-07-pen-plotter/penHolderLoc.jpg)

![pen holder design](/assets/imagesPortfolio/2023-02-07-pen-plotter/renders.jpg)

![mounted 1](/assets/imagesPortfolio/2023-02-07-pen-plotter/IMG_0874.JPG)

![mounted 2](/assets/imagesPortfolio/2023-02-07-pen-plotter/IMG_0876.JPG)

## Plotting Modelled Solids

The first Grasshopper definition generates gcode for modelled solids. The bottom left corner of the solid are located at point (70,90,0) so that they take into account for the offset between the nozzle and the tip of the pen. The z-axis offset is taken care of within Grasshopper so that the nozzle does not hit the print bed during plotting. 

![rhino modelling 0-1](/assets/imagesPortfolio/2023-02-07-pen-plotter/dwgplots-0-1.jpg)

![grasshopper definition 0-1](/assets/imagesPortfolio/2023-02-07-pen-plotter/grasshopper-0-1.jpg)

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/800517287?h=db8c6d6cee&autoplay=0&loop=1&title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

[<img src="/assets/imagesPortfolio/2023-02-07-pen-plotter/plots0.jpg" width="49%"/>](/assets/imagesPortfolio/2023-02-07-pen-plotter/plots0.jpg)
[<img src="/assets/imagesPortfolio/2023-02-07-pen-plotter/plots1.jpg" width="49%"/>](/assets/imagesPortfolio/2023-02-07-pen-plotter/plots1.jpg)

## Plotting a Heightfield Map

A heightfield surface of an image is created in Rhinoceros. As an image, I used one of the Chladni plates I found online. The surface is contoured to create a series of curves. Then the curves are imported into Grasshopper. The direction of curves are flipped for every second curve. So that the final result would be a meandering single curve. The splines are divided to find points at certain intervals.

![rhino modelling 2](/assets/imagesPortfolio/2023-02-07-pen-plotter/dwgplots-2.jpg)

![grasshopper definition 2](/assets/imagesPortfolio/2023-02-07-pen-plotter/grasshopper-2.jpg)

![plot 2](/assets/imagesPortfolio/2023-02-07-pen-plotter/plots2.jpg)

## Plotting Separate Entities

This definition necessitates finding the last and first points of separate curves. At the last point of each curve, the pen lifts, moves to the first point of the next curve and repositions itself back on the paper.

![rhino modelling 3-4-5](/assets/imagesPortfolio/2023-02-07-pen-plotter/dwgplots-3-4-5.jpg)

![grasshopper definition 3-4-5](/assets/imagesPortfolio/2023-02-07-pen-plotter/grasshopper-3-4-5.jpg)

[<img src="/assets/imagesPortfolio/2023-02-07-pen-plotter/plots3.jpg" width="49%"/>](/assets/imagesPortfolio/2023-02-07-pen-plotter/plots3.jpg)
[<img src="/assets/imagesPortfolio/2023-02-07-pen-plotter/plots4.jpg" width="49%"/>](/assets/imagesPortfolio/2023-02-07-pen-plotter/plots4.jpg)
[<img src="/assets/imagesPortfolio/2023-02-07-pen-plotter/plots5.jpg" width="49%"/>](/assets/imagesPortfolio/2023-02-07-pen-plotter/plots5.jpg)
