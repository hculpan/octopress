---
layout: post
title: "The power supply"
date: 2014-06-04 00:06:48 -0400
comments: true
categories: 
- Arduino
- electronics
---
So, as I indicated in my prior post, I'm going to build an Arduino on a breadboard.  I'll mostly be working from this [tutorial](http://arduino.cc/en/Main/Standalone) on the Arduino site, though I'll also be looking at other sources as well.  To that end, I finished the first step by building the power supply.  

{% img right /images/power_supply.jpg %}

This power supply can take up to 25V and will reduce it to 5V output.  The LM7805 [datasheet](http://www.addicore.com/Addicore-L7805CV-5V-Voltage-Regulators-5-pieces-p/114.htm) says it can handle 1.5A, but someone mentioned that anything over 1A will cause it to overheat without a heat sink.  Fortunately the power supply I'm using (a Trisonic universal AC/DC power supply) only puts only 1A.  As per the tutorial, I also added a green LED to indicate when the power is connected.  I also verified with my multimeter that the output is 5V.  So the circuit appears to be working as intended.  Btw, if you happen to notice that the wires coming from the power supply are tied to the power-in wires from the breadboard, it's because my 2.1mm barrel jack is also coming tomorrow, and I couldn't think of any other way to get the power from the power supply.  It kind of sucks because that basically renders my power supply useless after tonight, but c'est la vie.  

To build this, I used:

*  LM7805
*  2 10uF capacitors
*  1 200 ohm resistor
*  1 green LED

One mystery for me in this circuit as I wired it up was the purpose of the capacitors.  Still being very new to electronics, I didn't know what a capacitor was for, but after a quick consultation with the Internet, I learned that they're basically like little batteries.  But that still didn't answer what they're used for in this circuit, so I turned the power off, removed the two capacitors, and turned it back on.  The light came on, just like before, so no difference there.  But when I measured the output with my multimeter, I noticed it was only 3.9V and not 5V.  As soon as I put the capacitors back, the voltage was back at an expected 5V.  So clearly even in this simple circuit, the capacitors are necessary.  I'm not sure why they're necessary, but the capacitors seem to be needed to boost the voltage back up to 5.  My hypothesis is that despite what the multimeter suggests the voltage isn't actually constant but instead fluctuates a great deal but so quickly that the multimeter doesn't pick it up.  The capacitors then serve to even out this flow, absorbing excess power when the voltage is high and releasing it when it is low, so that it flows at a more consistent 5V when they are there.  I'll have to do more research and/or testing to see if I'm right.

In any case, hopefully tomorrow my other components will arrive and I can build my complete Arduino.  The only thing I'll be missing is a USB interface, so I can't program it the way I can my regular Arduino.  But I should be able to use my UNO to program my breadboard Arduino, which is my plan.