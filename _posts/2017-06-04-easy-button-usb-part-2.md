---
layout: post
title:  "Easy Button USB Mod Part 2"
date:   2017-06-04
categories: arduino
---

Continued from [part 1]({{ site.baseurl }}{% post_url 2015-08-17-easy-button-usb-part-1 %})

## Dealing with physics

My original plan of simply reading the leads via an analog pin fell apart once I closed up the unit and retested. The values became sporadic and unreliable. The solution is to treat the original board as a [pushbutton](https://www.arduino.cc/en/Tutorial/Pushbutton). 


### New configuration

* plug a 2k resistor into 5v
* from the other end of the resistor, run one lead to both:
  *  digital pin 2
  *  a pushbutton lead
* run the other pushbutton lead to ground

The state of the button can now be read via pin 2


### Testing the new configuration

I purchased a cheap [electronics kit](https://www.amazon.com/gp/product/B01ERP6WL4/ref=oh_aui_detailpage_o08_s01?ie=UTF8&psc=1), complete with breadboard, resistors, LEDs, and power source.


{:refdef: style="text-align: center;"}
![easy button apart]({{ site.basecdn }}/images/posts/easy-button-breadboard-1.jpg)
{: refdef}


## More trouble

When I put everything together in a mock assembly:

* The button responded poorly or not at all
* The Easy Button to made noise (!?)

The source of the noise was a speaker attached to the pcb. I'm not sure why this behavior started, but desoldering it cleared up both issues.

{:refdef: style="text-align: center;"}
![first attempt at soldering]({{ site.basecdn }}/images/posts/easy-button-solder-1.jpg)
{: refdef}


{:refdef: style="text-align: center;"}
![what a mess]({{ site.basecdn }}/images/posts/easy-button-solder-2.jpg)
{: refdef}


## The base

I found an acrylic Arduino case to use as the base. With some modification, It can be attached via two of the bottom screws of the button shell.


{:refdef: style="text-align: center;"}
![a case as the base]({{ site.basecdn }}/images/posts/easy-button-case-1.jpg)
{: refdef}


## Closing it up

{:refdef: style="text-align: center;"}
![what a mess]({{ site.basecdn }}/images/posts/easy-button-arduino-1.jpg)
{: refdef}


{:refdef: style="text-align: center;"}
![what a mess]({{ site.basecdn }}/images/posts/easy-button-arduino-3.jpg)
{: refdef}

## The software

The _HID-Project_ library is used in a simple [sketch](https://github.com/wtjones/EasyButtonLaunch/blob/master/EasyButtonLaunch.ino) to handle the button debounce and HID output. It could easily be modified to output as a keyboard instead.


## Testing it out

### Control Panel

In the Game Controllers control panel, the device registers as _Arduino Leonardo_. Pressing the button controls gamepad button 1.

{:refdef: style="text-align: center;"}
![validating the input]({{ site.basecdn }}/images/posts/easy-button-properties.png)
{: refdef}


### Kerbal setup

As mentioned in [part 1]({{ site.baseurl }}{% post_url 2015-08-17-easy-button-usb-part-1 %}), the only read-world purpose that I can think of at the moment is to use it as a _launch stage_ binding in [Kerbal Space Program](https://kerbalspaceprogram.com). Simple bind it from the main menu. Make sure to unbind space bar in order to eliminate accidental staging (the whole point !)

{:refdef: style="text-align: center;"}
![validating the input]({{ site.basecdn }}/images/posts/easy-button-ksp.png)
{: refdef}


## The final result

Mostly pointless? Yes, but it was an excuse to put an Arduino to work as well as provide an electronics refresher.

{:refdef: style="text-align: center;"}
![final product]({{ site.basecdn }}/images/posts/easy-button-action-1.jpg)
{: refdef}



