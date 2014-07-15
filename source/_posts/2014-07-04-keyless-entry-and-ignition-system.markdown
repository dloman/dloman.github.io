---
layout: post
title: "Key-less entry and ignition system"
date: 2014-07-04 14:11
comments: true
categories: [Key-less Entry, Key-less Ignition, Arduino, UCSB, PHYS128BL]
---
This project, is an old project I did as my final exam for UCSB Physics 128BL, Digital Electronics Lab. watch the video for a demonstration or click through for more (albeit sparse) details.
<iframe width="420" height="315" src="//www.youtube.com/embed/wIs6U7mWE40" frameborder="0" allowfullscreen></iframe>
<!-- more -->
This project was very simple. And unfortunately I didn't document the process of installing this system into my car.
Pictures of cutting a hole in the side of my car would be awesome to have...
None the less this system is an off the shelf ($15 swap meet) key-less ignition system wired into
the cars' starter and an Arduino wired to 2 keypads.
One of the keypad is outside the car for lock/unlock,
and the other keypad is on the inside of the door for ignition.
The Arduino listens for the correct password on the keypad
and then triggers an npn transistor wired to the remote of the key-less ignition system
or the lock unlock switch of the car.
The youtube video is really the only documentation I took of the entire project,
but figured I would do a small writeup because this worked pretty well for such a simple solution.

