---
layout: post
title: "Remote Controlled Junction Power Outlet"
date: 2013-12-23 12:29
comments: true
sharing: true
categories: [Electronics, wireless, 315 Mhz, laser light shows]
---
Was on adafruit a few weeks backs and found <a href="https://www.adafruit.com/products/1097"> this little guy </a> and <a href="https://www.adafruit.com/products/1095"> the corresponding remote </a>.
I immeditely purchased that I had one of these <a href="http://www.amazon.com/BeesClover-4-Channel-interface-dupont-15-20mA/dp/B00E4HJA0Q/ref=sr_1_7?ie=UTF8&qid=1387830865&sr=8-7&keywords=relay+board"> relay boards </a> lying around in my closet. So i decided to make a 315 Mhz controlled junction box for turning on my lights with a remote. Here is a video of the finished product <video>
Here is how I made this little guy.
<!-- more -->
<b> Parts List: </b><br>
<a href="https://www.adafruit.com/products/1097"> Remote Board </a> <br>
<a href="https://www.adafruit.com/products/1095"> KeyFob </a><br>
<a href="http://www.amazon.com/BeesClover-4-Channel-interface-dupont-15-20mA/dp/B00E4HJA0Q/ref=sr_1_7?ie=UTF8&qid=1387830865&sr=8-7&keywords=relay+board"> Relay Board</a><br>
<a href="http://www.homedepot.com/p/Steel-City-2-Gang-Square-Electrical-Box-521711234EW-30R/202590467#"> Junction Box </a><br>
<a href="http://www.homedepot.com/p/Leviton-15-Amp-Duplex-Outlet-White-R52-05320-00W/202066670#"> 2x Outlets </a><br>
<a href="http://www.homedepot.com/p/Leviton-2-Gang-Duplex-Outlet-Wall-Plate-Ivory-R51-86016-00I/100046108?N=arcd%2FNtk-All%2FNtt-Outlet%252BWall%252BPlate%3FNs%3DP_REP_PRC_MODE%257C0%26NCNI-5#"> Outlet Cover </a> <br>
<b> Stuff I had laying around </b><br>
5v old cell phone charger <br>
Old computer power supply cable <br>
fiber glass resin (optional) <br>


<b> Step 1:</b><br>
Look at the location of the vcc gnd and control pins on your relay board and match them up as best as possible with your remote board.
<iframe src="https://www.flickr.com/photos/108066226@N08/11520002913/player/924bb87a6d" height="480" width="640"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
<br>
<b> Step 2:</b><br>
Solder the corresponding pins from the relay to the remote. (there is a orange wire in in the back/underneath hooking up my vcc)
<iframe src="https://www.flickr.com/photos/108066226@N08/11519997473/player/65477bd33d" height="480" width="640"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

<br>
<b> Step 3:</b><br>
Attach longer leads to ground and vcc to allow for connection to a power supply.
<iframe src="https://www.flickr.com/photos/108066226@N08/11519888165/player/f1702f4226" height="480" width="640"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

<br>
<b> Step 4:</b><br>
Take the junction box and line the inside with electrical tape. this will keep things from shorting accidentally. Also if you decide to try and waterproof it will take the resin from seeping through the holes.<br>
<iframe src="https://www.flickr.com/photos/108066226@N08/11519881095/player/6367fb057d" height="640" width="480"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
<br>
<b> Step 5:</b><br>
Take the outlets and on the cold side (big prong) on both outlets break off the tab connecting the 2 junctions together. If you look closely in the picture I have broken off the tab on the plug on the right but not yet for the one on the left. <br>
<iframe src="https://www.flickr.com/photos/108066226@N08/11519879395/player/a87c0062bf" height="640" width="480"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

<br>
<b> Step 6:</b><br>
Connect 4 wires to the middle slot of each relay and solder them together
<iframe src="https://www.flickr.com/photos/108066226@N08/11519955486/player/dd19df626d" height="640" width="480"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
<br>
<b> Step 7:</b><br>
Grab an old cellphone charger (the smaller the better) and connect 5v to vcc and gnd to gnd.
<iframe src="https://www.flickr.com/photos/108066226@N08/11519973103/player/f2cec6a0ae" height="640" width="480"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
<br>

<b> Step 8:</b><br>
Attach the the 4 cold pins to the left post of the relay.
If you want specific order in which outlet is controlled by which button this is the time to figure this out.
Depending on how you soldered the controller make sure your desired button controls the corresponding desired outlet.
(You can always test this by powering up the dc power supply and seeing which lights on the relay board switch when specific buttons are pressed and wiring the desired outlets from there.)
<iframe src="https://www.flickr.com/photos/108066226@N08/11519884284/player/2aea9368c8" height="640" width="480"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

<br>
<b> Step 9:</b><br>
Connect the neutral line to the 4 lines coming out of the outlets (2 green and 2 black for me), and connect the hot line to the 4 lines that you soldered together in step 6. Then hook up the cellphone power supply to the 120v hot and nuetral lines to give it power.
Connect the ground pin of the power cords to the ground lead on one of the electrical outlets. This will wire the case to ground and provide some saftey if something accidentally shorts against the housing.
Then double check everything is taped and heat shrunked safely and plug it in and test and make sure everything works.
<iframe src="https://www.flickr.com/photos/108066226@N08/11519878864/player/769618d50b" height="480" width="640"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
<br>


<br>
<b> Step 10:</b><br>
Carefully cram everything into the junction box and tighten all the screws
<iframe src="https://www.flickr.com/photos/108066226@N08/11519966443/player/aa82b20a6a" height="480" width="640"  frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
<br>

<b>Step 11:(I havent tried this one yet...)</b><br>
To make the electronics inside water resistant fill the junction box with fiberglass resin. this will allow the box to be used outside and get rained on....or you could spend a little more money and just buy a water proof junction box and outlets from the start and be significantly safer...but where is the fun in that?
<br>
Questions? Comments? Let me know what you think!
