---
layout: post
title: Vinyl Cutter Calibration
date: 2022-09-20
description:
tags: [vinyl cutting]
---

Vinyl cutter was not cutting properly while we were going over the tutorial. No matter how much we increased the force (we went up to 200gf at some point), it was still not going through the vinyl layer.

After an online search, I found that vinyl cutting forces should be within the range of 30-100 gf. Here are force and speed ranges for commonly used materials:

![cutting force and speed](/assets/images/2022-09-20-vinyl-cutter-calibration/chart.png "cutting force and speed")

I inspected the machine and found out that all three screws holding the blade and blade holder in place were loose. I screwed the blade in place according to instructions which can be found [here](https://www.youtube.com/watch?v=baRsXfkb93w&ab_channel=Samcraft) or [here](https://www.youtube.com/watch?v=3asFY_2nTEk&ab_channel=Stahls%27TV) with the correct depth for blade height, which is approximately **half the thickness of a credit card**.

![vinyl cutter](/assets/images/2022-09-20-vinyl-cutter-calibration/20220920_092351-01.jpg "vinyl cutter")

Fixing the screws and blade height did not solve the problem completely. I got to a point where it seemed like the blade was cutting but it was also catching and lifting the corners while cutting. And it was still impossible to remove the background from the cut objects. Therefore I concluded that the blade was also dull. We changed the blade. You can see how to change the blade [here](https://www.youtube.com/watch?v=xq4g-Xsc7_0&ab_channel=PrintPhase).

Ta-daaa. The machine works perfectly now!!!

Ps: I also found [this](https://rolanddga.sharepoint.com/sites/dealers/SupportDocumentation/Forms/AllItems.aspx?id=%2Fsites%2Fdealers%2FSupportDocumentation%2FCutter%20Blade%20Reference%20Guide%2Epdf&parent=%2Fsites%2Fdealers%2FSupportDocumentation&p=true&ga=1) useful handbook from Roland which can answer some of the problems that users might face. One thing I definetely would like to try is the blade offset.

For more information on how to use the machine please read the [manual](https://files.rolanddga.com/Files/GS-24_UsersManual/Responsive_HTML5/#t=GS-24_index.html)

Pss: If your SVG file appears to have no dimensions and Mods cannot read it, then open the SVG file in Notepad and enter the pixel dimensions for X and Y (you can see the overall dimensions of your drawing in Illustrator or similar).