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

This power supply can take up to 25V and will reduce it to 5V output.  The LM7805 [datasheet](http://www.addicore.com/Addicore-L7805CV-5V-Voltage-Regulators-5-pieces-p/114.htm) says it can handle 1.5A, but someone mentioned that anything over 1A will cause it to overheat without a heat sink.  Fortunately the power supply I'm using (a Trisonic universal AC/DC power supply) only puts only 1A.  As per the tutorial, I also added a green LED to indicate when the power is connected.  I also verified with my multimeter that the output is 5V.  So the circuit appears to be working as intended.

To build this, I used:
+  LM7805
+  2 10uF capacitors
+  1 200 ohm resistor
+  1 green LED

The one issue for me is that I don't really understand capacitors, so I don't really understand their purpose in this circuit.  So obviously that's something I need to read on and work through.

So hopefully tomorrow my other components will arrive and I can build my complete Arduino.  The only thing I'll be missing is a USB interface, so I can't program it the way I can my regular Arduino.  But I should be able to use my UNO to program my breadboard Arduino, which is my plan.