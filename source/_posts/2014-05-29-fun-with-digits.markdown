---
layout: post
title: "Fun with digits"
date: 2014-05-29 22:51:22 -0400
comments: true
categories: 
- Arduino 
- electronics
---

So my latest Arduino build was a two-digit display.  Each digit is a separate 7-segment common cathode display, and I'm using two 74HC595 8-bit shift registers to drive them.  The wiring was certainly the most complex thing I've done so far, though I'm finding it pretty simple to follow the schematics and actually only screwed up one thing (switched pins 1 and 2 going into the left digit), but that was easily tracked down.  The coding was also very, very simple.  I pulled this straight out of the *Arduino Workshop*.

Here's a picture of the circuit:
{% img left http://code.culpan.net/piduino/images/fun_with_digits.jpg %}

So one thing this shows is my new, larger breadboard.  I **love** this [Elenco 9440 Breadboard](http://www.amazon.com/gp/product/B0002H4W0U/ref=oh_details_o02_s00_i00?ie=UTF8&psc=1).  It just gives so much room to build circuits.  At almost $40, it wasn't cheap, but given how much I hope to use it, I think it was worth it.  Also I like wires that came with it.  The wires that arc over the breadboard came with my other sets, and they're definitely nice, but I hate having so many of them on the board at one time becomes it really becomes very cluttered.  But the breadboard came with the flat wires which can really replace the other wires for a lot of shorter connections where they don't have to cross other wires.  I even used them to keep clutter away from the digits in the lower left corner by running the red wires from the bottom of the LED to the left of the board, and then connecting using the arcing wires to the 74HC595.  Wish I had thought to do that with the right digit...  I placed the right digit first, got it working, then placed the left - which is why the wiring at the bottom is done differently.  I was too lazy to remove the clutter from the right digit, so you have the annoying red wire cutting through the view to the digits.

Here's a video of it running, counting from 0 to 99:
{% video http://code.culpan.net/piduino/videos/fun_with_digits.mp4 %}