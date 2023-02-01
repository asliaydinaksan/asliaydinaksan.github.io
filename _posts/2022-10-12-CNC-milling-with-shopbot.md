---
layout: post
title: CNC Milling with Shopbot
date: 2022-10-11
description:
tags: [cnc milling, how to]
---

![CNC milling](/assets/images/2022-10-12-CNC-milling-with-shopbot/20221014_095046.jpg "CNC milling")

**Machine: Shopbot**

**Software: Shopbot 3, VCarve Pro**

We have a Shopbot milling machine at the lab. For this tutorial, we prepared an example cut file within VCarve Pro.

---

## Here are the Milling Steps:


<details>
<summary><b><font size= "+1">General cleaning around the machine</font></b></summary>
- Check around the machine for clear movement in all three axis. The paths of movement should be free of obstructions.
<br>
- Clean the bed of the CNC milling machine, use a vacuum cleaner if necessary.
<br>
- Check for protruding screw marks on the sacrificial layer. If found, eliminate them with sand paper.
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Check and place your material</font></b></summary>
- Measure the thickness of your material at several locations (we are going to use the maximum value).
<br>
- Measure the length and width of the sheet.
<br>
- Remove any foreign objects/screws from the material. Especially metal objects are dangerous. They create high resistance for the milling bit which rotates at 18000 rpm. And if metal shavings enter the ventilation and reach the dust collection bags, they can cause fires.
<br>
- Place your material on the sacrificial layer.
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Turn on the CNC milling machine</font></b></summary>
- Rotate the knob clockwise.
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_141343.jpg" alt= "cnc on/off" width="300px">
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Open Shopbot 3 software</font></b></summary>
- In command box, type <b>K</b> to open the keypad.
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/k.jpg" alt= "shopbot 3">
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_163440.jpg" alt= "keypad">
<br>
- Bring the milling head towards you to change the collet and milling bit:
<br>
<b>UP</b>, <b>DOWN</b>, <b>LEFT</b> and <b>RIGHT</b> keys: control the movement in X- and Y-axis.
<br>
<b>PAGE UP</b> and <b>PAGE DOWN</b> keys: control the movement in Z-axis.
<br>
<b>Ctrl + control keys</b>: moves the milling head faster.
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Change the collet and milling bit</font></b></summary>
- Put the skirt down by loosening the butterfly nut at the back.
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_143551.jpg" alt= "skirt and butterfly nut" width="300px">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_143637.jpg" alt= "skirt down" width="300px">
<br>
- Use the wrenches to loosen the clamping nut.
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_143741.jpg" alt= "wrenches" width="300px">
<br>
- When the clamping nut is loose, unscrew it from the milling head and take out the collet and the milling bit.
<br>
- Pick the milling bit and its corresponding collet you would like to use in your project.
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_135731.jpg" alt= "milling end" width="300px">
<br>
- Place the collet in the clamping nut and push until you hear a click. Then place the milling bit in the collet up until it is flush with the inner set of teeth inside the collet.
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_140106.jpg" alt= "collet and bit" width="300px">
<br>
- Assemble the whole part back following the steps of removal backwards.
<br>
<br>
Milling bits are divided into types according the their the shape of their tip, diameter and number of flutes. <b>DIAMETER</b>: the diameter decision depends on the detailing of the project. The bigger the diameter, the harder to produce fine details. <b>TIP SHAPE</b>: We use ball nose (rounded) and end mill (flat) type bits frequently at Fablab. End mill is used for regular cutting and pocketing jobs. Ball nose mill is used for rounded details. It is good for producing relief-like 2.5D work. <b>FLUTE</b>: Deep spiraled grooves along the bit. When you look perpendicular to the tip end, you can recognize how many flutes there are on the milling bit. The more flutes there are, the more precise the job is. 
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Open VCarve Pro software</font></b></summary>
<br>
<font size= "+0.5"><u>OPEN NEW FILE</u></font>
<br>
<br>
<font size= "+0.5"><u>JOB SETUP</u></font>
<br>
Job size (X & Y): indicates the maximum extents the tool will go. The maximum values can be the length and width of the material. The orientation of the material on bed should be the same as the orientation on the screen.
<br>
Material (Z): Enter the maximum material thickness measured. Pick the bottom of the material for jobs that will cut through the whole material. Pick the top of the material for carve-in jobs.
<br>
XY Datum: Usually, left bottom corner is selected.
<br>
Unit: mm
<br>
Hit save.
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/10.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/10.JPG" alt= "job setup">
</a>
<br>
<font size= "+0.5"><u>DRAWING</u></font>
<br>
We bring in a drawing we have drawn before. The supported file types are: <b>dwg, eps, ai, pdf, pvc, v3d, v3m, crv, skp</b>. However, we drew our own cut drawing for this tutorial.
<br>
Either way, first start with drawing circles where you want to put the screw holes. You will later use these holes to fix your material on the sacrificial layer.
<br>
Fillets: The thickness of the milling bit does not allow making straight 90 degree angle cuts in the pockets and interior profiles. Therefore, it is especially important to add T-bone or Dog-bone fillets if you will use the cut profile to fit parts together. 
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/9.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/9.JPG" alt= "fillet">
</a>
<br>
<br>
<font size= "+0.5"><u>SAVE FILE</u></font>
<br>
VCarve Pro's file extension is <b>*.crv</b>
<br>
<br>
<font size= "+0.5"><u>TOOLPATHS</u></font>
<br>
The order of toolpath creation should be: drilling, pockets, inner profiles, outer profiles. Everytime you make a change, hit <b>Calculate</b>.
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/1.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/1.JPG" alt= "toolpath">
</a>
<br>
<em><u>1. Drilling toolpath</u></em>
<br>
Start depth: 0 mm
<br>
Cut depth: 2 mm (it should be only deep enough to indicate places of the screws)
<br>
Tool: Select a tool from the list of preset tools. If you are going to make changes, do it in edit mode (so that the original settings do not change).
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/3.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/3.JPG" alt= "drilling toolpath">
</a>
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/4.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/4.JPG" alt= "tool selection">
</a>
<br>
<em><u>2. Pocket toolpath (raster)</u></em>
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/5.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/5.JPG" alt= "pocket raster toolpath">
</a>
<br>
<em><u>3. Pocket toolpath (offset)</u></em>
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/6.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/6.JPG" alt= "pocket offset toolpath">
</a>
<br>
<em><u>4. Profile toolpath (for inner profiles)</u></em>
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/7.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/7.JPG" alt= "profile inner toolpath">
</a>
<br>
<em><u>5. Profile toolpath (for outer profiles)</u></em>
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/8.JPG">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/8.JPG" alt= "profile outer toolpath">
</a>
<br>
<br>
<font size= "+0.5"><u>SAVE TOOLPATHS</u></font>
<br>
File type for Shopbot 3 is <b>*.sbp</b>
<br>
IMPORTANT: <b>Save drilling toolpath separately from the rest of the toolpaths.</b> Because firstly, you will use the drilling toolpath to make marks for screws and then put screws there. And then you will run the rest of your milling job.
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Safety First</font></b></summary>
- Always Use safety earmuffs and safety glasses, while operating the machine.
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Go back to Shopbot 3 software</font></b></summary>
- Click on <b>Zero XY</b>: this will move the milling head to the absolute XY origin.
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_162650.jpg">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_162650.jpg" alt= "zero xy">
</a>
<br>
- Move the milling head to the location where you want the new XY origin to be with keypad.
<br>
- Hit <b>Zero > Zero [2] axes (X)</b>: this will save the X and Y coordinates as the job's origin.
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_163102.jpg">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_163102.jpg" alt= "zero 2 axes">
</a>
<br>
- Record coordinate values for X and Y on the Position screen somewhere. If anything happens and you need to stop the job, you can use these values to reset the job origin.
<br>
- To Zero the Z-axis: move the milling head above a clear surface on the sacrificial layer. Pick the metal plate from the milling head and touch it to the end of the milling bit. Touching the plate to the bit should close an electric current. If the current closes the left-most <b>Stop, Inp 1 circle</b> should turn green. Repeat this a couple of times to make certain the current is closed. This step is important because Z-axis will automatically move down and it should stop when it touches the metal plate. Put the matel plate under the milling bit on the sacrificial surface. Press <b>Zero Z</b>.
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_163540.jpg">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_163540.jpg" alt= "zero z">
</a>
<br>
- Load the drilling toolpath.
<br>
<a href="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_164203.jpg">
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_164203.jpg" alt= "load toolpath">
</a>
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Start the milling job</font></b></summary>
- Put the key attached to the wrench in the keyhole underneath the machine on/off knob and turn it. The milling bit should start spinning.
<br>
- Put the spindle speed to 18000 on the varispeed box manually.
<br>
- Turn on the ventilation and wait for a minute until it gains full power.
<br>
- Go back to Shopbot 3 screen and <b>START</b> job without changing anything.
<br>
- Hover your hand above <b>SPACEBAR</b> until you are sure the milling bit is moving according to expectations. Spacebar pauses the job if necessary.
<br>
- When drilling job is finished, screw the material on the sacrifical layer.
<br>
- Load the toolpath for the rest of the job and hit <b>START</b> again without changing anything.
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_165545.jpg" alt= "cnc milling in process">
<br>
- When the job is finished, move the milling head away with keypad controls.
<br>
<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221011_170040.jpg" alt= "cnc milling finished">
<br>
<br>
</details>



<details>
<summary><b><font size= "+1">Post-processing</font></b></summary>
- Turn off the ventilation and the CNC machine.
<br>
- Unscrew the material from the sacrificial layer and move it away from the bed.
<br>
- Clean around the machine, use the vacuum cleaner where necessary.
<br>
- Break the tabs around the cut shapes to remove them from the sheet material.
<br>
- Sand the irregularities around the milled parts.
<br>
<br>
</details>


<img src="/assets/images/2022-10-12-CNC-milling-with-shopbot/20221012_165920.jpg" alt= "cnc milled part">