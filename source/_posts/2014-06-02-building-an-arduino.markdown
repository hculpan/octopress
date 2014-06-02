---
layout: post
title: "Building an Arduino"
date: 2014-06-02 00:15:52 -0400
comments: true
categories: 
- Arduino
- electronics
- AVR
- Atmega328
---
While I have a number of projects in mind for my Arduino, I really have one main idea in mind.  I want to do a dice roller.  The idea is to have a set of buttons, each representing a die type - d4, d6, d8, d10, d12, d20, and d100 (all very familiar to any player of role-playing games like Dungeons & Dragons).  When a button is pressed, the device would randomly generate a number in the range of the die type and display it on two LED digit displays (see my [Fun With Digits](http://piduino.info/blog/2014/05/29/fun-with-digits/) post).  I want to take this project all the way from a breadboard prototype to a final "production" product.  I say production not because I actually plan to sell this, but I do want to construct something that would be a finished product that I could give away to several friends.

Part of the reason that the goal of a finished device is important to me is because I want to explore the entire process of making such a device.  And that forces me to think about a lot of things that I might not otherwise consider.  For example, one thing it's forced me to think about is how do I package up an Arduino for inclusion in such a device.  Obviously I wouldn't, since the Arduino is really too big and most of what the board can do I don't need, for example, a USB interface.

This has led me down the path of considering how to build my own microcontroller system.  The Atmega328, the chip that powers the Arduino UNO board that I'm using, is readily available as a standalone product, so that seems like an ideal platform for me to build on.  And the nice thing is that just buying the components I need should be cheaper than having to purchase a whole Arduino, and it should take up a whole lot less space.

{% img right http://ecx.images-amazon.com/images/I/51brDteSDZL._BO2,204,203,200_PIsitb-sticker-v3-big,TopRight,0,-55_SX278_SY278_PIkin4,BottomRight,1,22_AA300_SH20_OU01_.jpg %}

So to start off I'm going to follow this tutorial to [build an Arduino on a breadboard](http://arduino.cc/en/Main/Standalone), sans the USB interface (though I might add this later).  I've ordered the parts I need, but of course it will be a few days before they get here.  Until then, I'll be reading [AVR Programming](http://www.amazon.com/Make-Programming-Learning-Software-Hardware-ebook/dp/B00I2YHM2K/ref=sr_1_2?ie=UTF8&qid=1401686715&sr=8-2&keywords=avr).  At the very least, I want to figure out how to dump the Arduino IDE (which, while being a nice beginner IDE, is really not that good for an experienced programmer) and switch to programming the Arduino with C.  Then when I get the parts in, I can build my breadboard Arduino and figure out how to integrate that into my final die roller circuit.
