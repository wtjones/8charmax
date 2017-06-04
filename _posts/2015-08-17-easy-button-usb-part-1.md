---
layout: post
title:  "Easy Button USB Mod Part 1"
date:   2015-08-17 19:43:11
categories: arduino
---

## Background

I've had an [Arduino UNO](https://www.arduino.cc/en/Main/ArduinoBoardUno) for some time now, but couldn't come up with a project to put it to use. I recently realized that I have an old [Easy Button](http://www.staples.com/sbd/cre/marketing/easybutton/index.html) on my shelf that could probably function as an input device. A [Kerbal Space Program](http://kerbalspaceprogram.com) launch button comes to mind. :)

I'm sure there are existing recipies for something similar, but my goal is to come up with an original design as a learning experience.


## The Button

{:refdef: style="text-align: center;"}
![easy button apart]({{ site.basecdn }}/images/posts/easy-button-1.jpg)
{: refdef}

Disassembly reveals a since circuit board that controls the speech that occurs when the button is pressed. I don't care to utilize the speaker, so for now I will just leave out the batteries.


I need a way to detect a button press, so I set my tested for resistance and touched different spots on the board. When the circled (in red) points are connected, a button press appears to show up as a short.

{:refdef: style="text-align: center;"}
![easy button points]({{ site.basecdn }}/images/posts/easy-button-board-points.jpg)
{: refdef}


## Detecting a button press

Lacking an electronics starter kit, I found an old redbook audio and asked a friend to crimp some dupont pins. This picture is before I removed the shielding.

{:refdef: style="text-align: center;"}
![audio cable before]({{ site.basecdn }}/images/posts/cd-wires.jpg)
{: refdef}

As a test, I connected wires to the points on the easy button board and the dupont pins to the analog 0 and ground pins on the arduino. When the button is pressed, the sensor reads 0 as opposed to ~400 when not.

Is the correct way to handle a button? Probably not, at least according to the [arduino site](https://www.arduino.cc/en/tutorial/button). So far this is working so I am sticking to the plan.


## Next up...

I plan on sharing my experience in coaxing the Arduino into behaving as a HID (Human Input Device).

### Update

[Part 2]({{ site.baseurl }}{% post_url 2017-06-04-easy-button-usb-part-2 %}) is now available.