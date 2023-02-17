---
layout: post
title: Paper Manipulation
tags: [laser cutting, rhinoceros]
img: /assets/imagesPortfolio/2022-11-04-paper-manipulation/paperManipulation.gif
---

I am interested in changing material behavior via digital fabrication. Paper is a 2d material, however, via creating deliberate cuts and folds, you can create 3d forms with it. In this small project, I wanted to test several approaches to paper folding via laser cutting.

My source of inspiration for these projects were:

- [Eric Gjerde](https://www.ericgjerde.com/portfolio/folding-the-bauhaus-reverse-engineering-josef-albers-preliminary-course/)'s research on Bauhaus' Preliminary Course projects given by Josef Albers.
- [Yoshinobu Miyamoto](https://www.flickr.com/photos/yoshinobu_miyamoto/)'s various folding paper projects.
- [Ron Resch](https://www.youtube.com/watch?v=UXENKmAUL0E&ab_channel=TheNatureOrchestra)'s origami tessellations. I also did a previous research on these patterns, which can be found on my (other) [website](https://asliaydinaksan.wixsite.com/portfolio/schematizing-folding-patterns).

I drew the cut files in Rhinoceros, using only 2D curves.

The first set of patterns were designed by studying procedural cut and fold of strips arrayed around a central point. The first pattern lets the strips find their own bending curvature by only fixing them back on the background at only one point. The second pattern has a fold line along the strips which indicates its flexure point. The location of the lines change along the strips to get different heights for the strips.

![pattern 1](/assets/imagesPortfolio/2022-11-04-paper-manipulation/pattern-01.jpg)

![pattern 2](/assets/imagesPortfolio/2022-11-04-paper-manipulation/pattern-02.jpg)

The second set of patterns are derived from studying the outcomes of Josef Albers' preliminary course projects. They all have central arrangement on a circle. The first pattern is derived by cutting concentric dashed circles. The resulting affect is achieved by pulling on the central circle and letting the material stretch as much as it can without ripping. The second and third pattens create strips of arcs which are then bent at their ends.

![pattern 3](/assets/imagesPortfolio/2022-11-04-paper-manipulation/pattern-03.jpg)

![pattern 4](/assets/imagesPortfolio/2022-11-04-paper-manipulation/pattern-04.jpg)

![pattern 5](/assets/imagesPortfolio/2022-11-04-paper-manipulation/pattern-05.jpg)

The last pattern is an origami patter from Ron Resch's tesellation diagrams. Ron Resch patterns have both valley and mountain folds. If you engrave (engraving does not cut through and through the material, but cuts until a certain point depending on the power and speed factors) lines in the lasercutter, you can only fold the material in one direction and it also decreases the structural strength of the material. So, I decided to use the perforation mode in Lightburn to make dashed cuts. This way, the dashed cuts would allow for folding but not cause the material to lose its structural strength totally. I made a few tests to find the optimum cut to skip ratio for the material I used.

![pattern 6](/assets/imagesPortfolio/2022-11-04-paper-manipulation/pattern-06.jpg)