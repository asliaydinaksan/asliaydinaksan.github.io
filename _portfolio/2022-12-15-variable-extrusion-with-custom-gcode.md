---
layout: post
title: Variable Extrusion with Custom G Code
tags: [3d printing, rhinoceros, grasshopper]
img: /assets/imagesPortfolio/2022-12-15-variable-extrusion/startfish2.gif
---

![all](/assets/imagesPortfolio/2022-12-15-variable-extrusion/allFish.jpg)

The project explores creating custom gcodes for 3d printers. It focuses on finding optimum extrusion and later on variating extrusion amounts for each distance within controlled parameters. Consumer available slicers (such as Prusa Slicer and Cura) do not give this kind of freedom to users. Therefore, I created a design workflow which allows for freedom in extrusion amounts.

Project was designed in Rhinoceros and Grasshopper, printed in Prusa i3 MK3S.

## Design

The beginning form is designed in Rhinoceros. It consists of 3 curves placed 20mm and 10mm away from each other vertically. Their centers are located at the same x,y coordinates. The curves, then, are lofted to create a surface. The base of the form is a spiral starting from the center of the bottom curve towards its perimeter. This form is actually only a vessel and can be replaced with forms of similar topology.

![design](/assets/imagesPortfolio/2022-12-15-variable-extrusion/design-01.jpg)

The algorithm to generate the gcode is created in Grasshopper.

<hr>
### About gcodes for 3d printers

Gcode is the most widely-used computer numerical control programming language for machines as well as 3d printers. Each line of code tells the printer to perform one specific action. Every line has a letter address. G codes direct the machine's motion and function, while M codes direct the operations outside movements.

Gcodes for 3dprinters have 3 parts: the start code, the middle part and the end code. The start code prepares the machine for 3d printing: such as machine preparation, bed leveling, setting extruder and bed temperature. In the middle part, series of coordinates and extrusion amounts define the movement and printing of the forms. When the printing is finished, the end code prepares the machine to stop with commands for cooling, moving nozzle away from the print job, etc.

You can learn more about gcodes from [Marlin's website](https://marlinfw.org/meta/gcode/).
<hr>

Since I used the Prusa i3 MK3S printer, I looked at a gcode file I created previously with Prusa Slicer to obtain and modify the start and end gcodes.

I created an algorithm which imports spiral curve and lofted form from Rhinoceros. Lofted form is contoured to create a series of contour curves. All the curves are divided by a certain number to obtain points along them. The points are broken down to their x,y,z coordinates. 

The x, y and z coordinates are directly fed to the middle part of the gcode as coordinates. The **E** variable in middle part, which is the extrusion amount, is found by a factor of the distance between two consecutive points. First I created a fixed extrusion component to find optimum extrusion. Later on, I wanted to give randomness to the extrusion amount within bounds which would print without problem. In the definition below, you can activate fixed extrusion by connecting **f** line and random extrusion by connecting **r** line to the division component (click on the image to see it bigger).

[<img src="/assets/imagesPortfolio/2022-12-15-variable-extrusion/grasshopper-01.jpg"/>](/assets/imagesPortfolio/2022-12-15-variable-extrusion/grasshopper-01.jpg)

## 3d printing

I found a used 10mm thick plywood sheet of dimensions 700mm by 1200mm with glue residue and drilled holes on it. Since the irregularities did not interfere with the overall design, I wanted to reuse this plywood. I sanded the glue residue and checked the material for leftover nails or screws (it is really important that there is no metal on the sheet. If the drill bit of the ShopBot hits a metal part there is a risk of metal shavings reaching the wood dust collection bag and starting fire.) before laying it on the milling bed.

In VCarve Pro, I created separate toolpaths for drilling, pockets, inner profiles and outer profiles. I cut the drilling toolpath and fixed the plywood sheet on the milling bed with Woodies. I sent the test part toolpaths to the machine without allowances.

<!-- insert an image the test pieces here -->

<hr>
### About Allowances

In a digital world, the parts do not need any tolerance to fit together. The faces of the parts can be flush and they do not create a problem. In the physical world, however, the material frictions, irregularities and the function of the part require creating allowances. Allowance is a planned deviation between an exact dimension and an intended final dimension.
<hr>

In the test parts, no detail was able to slide or fit into each other as expected. However, I was able to calculate the required allowances based on how much the final dimensions (the dimensions of the fabricated parts) deviated from exact dimensions (the dimensions in the digital model). Then, I created toolpaths for the sliding lid, sliding bottom panel and press fit parts separately, giving each an allowance offset. The Sliding lid and bottom panel pockets have different allowances beacuse I want the bottom panel to slide in with force and stay in its place afterwards, whereas, I wanted the sliding lid to have some room around it so it can slide in and out without force during use. I further separated inner pocket toolpaths according to their raster direction. You want the rastering direction along the longest side of the shapes.

(All the images are clickable if you want to see the values and specifics of each toolpath)

The material definition in VCarve Pro:

[<img src="/assets/imagesPortfolio/2022-10-21-personal-box/1.jpg" width="50%"/>](/assets/imagesPortfolio/2022-10-21-personal-box/1.jpg)

Drilling toolpath for locating the places of screws:

[<img src="/assets/imagesPortfolio/2022-10-21-personal-box/2.jpg" width="50%"/>](/assets/imagesPortfolio/2022-10-21-personal-box/2.jpg)

Pocket toolpath for sliding lid part and lid handles with raster angle 180° and allowance of -1.00mm:

[<img src="/assets/imagesPortfolio/2022-10-21-personal-box/7.jpg" width="50%"/>](/assets/imagesPortfolio/2022-10-21-personal-box/7.jpg)

Pocket toolpath for sliding lid part with raster angle 90° and allowance of -1.0mm:

[<img src="/assets/imagesPortfolio/2022-10-21-personal-box/8.jpg" width="50%"/>](/assets/imagesPortfolio/2022-10-21-personal-box/8.jpg)

Pocket toolpath for sliding bottom part with raster angle 90° and allowance of -0.5mm:

[<img src="/assets/imagesPortfolio/2022-10-21-personal-box/9.jpg" width="50%"/>](/assets/imagesPortfolio/2022-10-21-personal-box/9.jpg)

Inner profile toolpath with inside vectors and allowance of -0.5mm:

[<img src="/assets/imagesPortfolio/2022-10-21-personal-box/10.jpg" width="50%"/>](/assets/imagesPortfolio/2022-10-21-personal-box/10.jpg)

Outer profile toolpath with outside vectors and allowance of -0.3mm:

[<img src="/assets/imagesPortfolio/2022-10-21-personal-box/11.jpg" width="50%"/>](/assets/imagesPortfolio/2022-10-21-personal-box/11.jpg)

3D preview of all toolpaths:

[<img src="/assets/imagesPortfolio/2022-10-21-personal-box/13.jpg" width="50%"/>](/assets/imagesPortfolio/2022-10-21-personal-box/13.jpg)

A few seconds of the milling job. CNC milling machines are really powerful machines. Therefore, they need to be carried out with great focus and observation of the process. Please refer to this [documentation on CNC milling](/_posts/2022-10-12-CNC-milling-with-shopbot.md) for further instructions on how to run the machine and follow the safety protocols.

