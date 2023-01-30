---
title: "Vinyl Cutter and Heat Press"
date: 2022-09-19T00:00:00+00:00
author: Asli Aydin Aksan
layout: post
permalink: /vinyl-cutter-and-heat-press/
categories: General
tags: [vinylcutting, heat press, machines, roland gx-24 gs-24, vevor 8-in-1, tutorial]
---

![vinyl cutter main](/assets/images/2022-09-19-vinyl-cutter/20220927_150340.jpg "vinyl cutter main")

**Machine: Roland GS-24 and Vevor 8-in-1 Heat Press**

**Software: Mods**

We have Roland GS-24 vinyl cutter and Vevor Heat Press at the lab. We use [Mods](http://modsproject.org/) interface with the cutter.

---
## Vinyl Cutting

Turn on the vinyl cutter. Make sure the handle at the back left is down, then feed your material from back to front. Adjust the left pinch roller and right pinch roller within white sections. The rollers hold and roll the material back and forth while the cutting is in progress. Pull the handle up so the rollers catch the material and do not let it slip. One the machine screen, select the type of material via going through option with arrow keys and then pressing ENTER. In my case, I picked ROLL.

![vinyl cutter](/assets/images/2022-09-19-vinyl-cutter/20220916_135319.jpg "vinyl cutter")

Open the terminal on the computer the machine is attached to. Go to terminal and type:
- <code>cd mods</code>
- <code>bash mods</code>

This prompts an explorer page to open with Mods entry. Follow the steps down below to start the machine interface.

![mods](/assets/images/2022-09-19-vinyl-cutter/Screenshot%20from%202022-09-16%2013-47-27.jpg "mods")

Mods works with **.svg** files. SVG stands for Scalable Vector Graphics. A few pointers for preparing a file for cutting:
- Create a black and white file. Black parts should indicate your design and white parts should indicate the background. Mods captures the contrast between black and white to define cut lines.
- Make an appoximately 2mm border around your design.
- If you are going to use heat press to transfer your design on an object, make the mirror of your design.

I redrew a tile from the Alhambra Palace following the tutorial [here](https://www.youtube.com/watch?v=dxYAKI028YI&list=PLHG5uxhiqH9X3a2ryA4rtvRSP-6zDpsJY&ab_channel=ConReglayComp%C3%A1s). I created a gradient of line thicknesses to show hierarchical parts and wholes in the tiling.

<img src="/assets/images/2022-09-19-vinyl-cutter/pattern3.svg" alt="Alhambra tiling" width="50%"/>

In the Mods screen, follow the steps below to cut your design.

[![Mods cut steps](/assets/images/2022-09-19-vinyl-cutter/Screenshot%20from%202022-09-19%2011-39-07-01.jpg "Mods cut steps")](/assets/images/2022-09-19-vinyl-cutter/Screenshot%20from%202022-09-19%2011-39-07-01.jpg)

Remove the background with the help of tweezers, place a transfer tape on your design and go over it with a rigid object to make sure vinyl sticks to the tape. Stick the tape with the vinyl on the desired surface and remove the tape carefully.

<img src="/assets/images/2022-09-19-vinyl-cutter/20220919_120547.jpg" alt="Vinyl 1" width="49.75%"/>
<img src="/assets/images/2022-09-19-vinyl-cutter/20220919_124427.jpg" alt="Vinyl 2" width="49.75%"/>

<img src="/assets/images/2022-09-19-vinyl-cutter/20220919_125146.jpg" alt="Vinyl 3" width="49.75%"/>
<img src="/assets/images/2022-09-19-vinyl-cutter/20220919_125549.jpg" alt="Vinyl 4" width="49.75%"/>

![Vinyl 5](/assets/images/2022-09-19-vinyl-cutter/20220919_130019.jpg "Vinyl 5")

---

## Heat Press

For the heat press tutorial, I used the voronoi definition I developed in Rhinoceros, Grasshopper. Each cell in the pattern scale according to their distance from attractor points.

<img src="/assets/images/2022-09-19-vinyl-cutter/voronoiThermalPrint.svg" alt="Voronoi" width="50%"/>

- Turn on the machine with the switch
- Set initial temperature, highest temperature and time. You can go through options via **MODE** and adjust each option with **-** and **+** buttons (the machine works with Fahrenheit).
- Stack the layers as seen below.

![Heat Press Section](/assets/images/2022-09-19-vinyl-cutter/section.jpg "Heat Press Section")

- Wait 5-10 mins total for the machine to heat up.
- When you hear the beep, press the handle and hit &#x23EF;
- Wait the suggested time and when you hear the beep again, release the handle.
- Remove the transparent sticker carefully.

![Heat Press Steps](/assets/images/2022-09-19-vinyl-cutter/HeatPress.jpg "Heat Press Steps")

Below is a table explaining temperature and time requirements for various surfaces:

| Press Object | Initial Temperature (°F) | Highest Temperature (°F) | Proper Heating Time (s) |
| ---- | ---- | ---- | ---- |
|  Mugs | 230 | 330 | 40 |
| Tiles | 230 | 330 | 40 |
| Metal board | 230 | 300 | 40 |
| Plate | 230 | 355 | 150 |
| T-shirt | 230 | 355 | Sublimation paper: 30-50 |
| | | | T-shirt Paper: 10-20 |