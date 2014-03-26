---
layout: post
title: "Adjustable Desk"
date: 2014-03-20 13:19
comments: true
categories: [Standing Desk, Adjustable Desk, Hardware, Trinket, Arduino, Linear Acutator]
---
Hello Internets. I hope you have been doing great. I work at a computer 40+ hours week and sitting for that long isnt good for you. So I been wanting to try out a standing desk. I was defintly not certain I could stand for an 8 hour day and not wanting to be in lots of pain I decided to make an adjustable desk. So my roommate and I built me an adjustable desk. It came out amazingly well. For buildpics and comments click the link.

<!-- more -->
## Planning Process
I thought a lot about making an adjustable desk cheaply, a coworker of mine built an adjustable topper for his desk very cheaply using 2 pieces of plywood an electric drill and a RV jack stand.
Looking at the <a href="http://www.milk.dk"> Milk Desk</a>
I thought about making essentially a milk clone with a large RV jack stand inside the center console.
There were some issues with the format of the milk desk that i don't like.
Mostly with a center column it makes sitting at the center of the desk awkard for your knees and if its not centered then it would be difficult to remain stable.
This led me to this guys build which looked great. So I picked up some linear actuators on ebay for approx $40 each. So I went to homedepot picked up a sheet of cheap hardwood plywood and some aluminum strips we started building.
My roommate is a finish carpenter so he was responsible for all of the wood working awesomeness. That left me responsible for the electronics.
It's a very simple circuit containing an ATX power supply for the +5v(micro) and the +12v & -12V (the actuators run on 24v), adafruit's <a href="https://www.adafruit.com/products/1501">trinket</a>
(to read the buttons and switch the relays), 2 rad looking <a href="https://www.adafruit.com/products/559">buttons</a>
a dpdt relay(to reverse the polarity of the power to the actuators), and dpst relay (on and off power to the actuators).
## Build Pics
The build process took way longer then it should have mostly because I am still bad at making things in the real world. and there were a lot of issues with inductive voltage spikes on switching on/off the actuators.
##Future Additions
There are quite a lot of additions I want to make to the desk. Mostly using a proper H-Bridge motor controller instead of my janky DPDT nonsense. The actuators I have also have built in hall effect sensors, so I really want to be able to read those and
autolevel the desk. but for the most part the desk is working great and looks awesome and I am loving standing most of the day.
