---
layout: post
title: Digital Loom Research
date: 2023-02-22
description: 
tags: [internship project]
---

I am making the loom version 2, which will be a digital loom. For this project, I am using:

- Arduino Uno Board
- TMC2209 v2.0 silentstepstick driver for stepper motor
- Unipolar/Bipolar, 200 Steps/Rev, 42×48mm, 4V, 1.2 A/Phase Stepper Motor: NEMA 17 size hybrid motor

[Stepper Motor](https://www.pololu.com/product/1200/resources): look at FAQ for motor to driver wiring

[Stepper Driver](https://learn.watterott.com/silentstepstick/pinconfig/tmc2209/): this is for TMC2209 but this is the closest explanation I could find for pinout.

[Silentstepstick](https://www.trinamic.com/support/eval-kits/details/silentstepstick/)

[Unipolar and Biolar Wiring](https://blog.orientalmotor.com/wiring-basics-unipolar-vs-bipolar#:~:text=The%20main%20difference%20between%20%22unipolar,becomes%20a%20bipolar%2Dseries%20connection.): a general understanding of 

Useful exemplary projects:

- [TMC Stepper Arduino](https://forum.arduino.cc/t/tmcstepper-arduino-tmc2209/956036)
- [Using TMC2209 silent stepper motor driver with an arduino](https://forum.arduino.cc/t/using-a-tmc2209-silent-stepper-motor-driver-with-an-arduino/666992/21)
- [TMC 2209 V2.0 wiring](https://forum.arduino.cc/t/tmc-2209-v2-0-verkabelung/1063991)

The pin labeling is very different in all versions of TMC2209. [This](https://www.pialasse.com/2020/05/tmc2209-v3-0-upgrade-for-i3-mega/) website has a table to show how confusing it is (at least for me).

[TMC2209 Arduino Library](https://www.arduinolibraries.info/libraries/tmc2209)

[Serial1 not declared solved](https://forum.arduino.cc/t/serial1-was-not-declared-in-this-scope/606144)