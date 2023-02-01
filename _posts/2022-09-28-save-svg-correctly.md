---
layout: post
title: Save SVG Correctly
date: 2022-09-28
description:
tags: [mods, vinyl cutting, pcb milling, howto]
---

You need SVG type files for vinylcutting and pcb milling. Sometimes, you get a dimension error in mods when you upload your file as seen in the image.

![SVG error](/assets/images/2022-09-28-save-svg-correctly/Screenshot%20(860).jpg "SVG error")

One way to solve this problem is to open the SVG file in Illustrator and save it again **without a check mark next to _Responsive_**.

![SVG correction](/assets/images/2022-09-28-save-svg-correctly/Screenshot%20(859).jpg "SVG correction")

What this accomplishes is that the dimensions of the SVG image becomes absolute and not relative to the dimensions of the medium it is viewed in.