+++
showonlyimage = false
draft = false
image = ""
date  = "2017-05-05"
title = "Snakey SLAM-Nav"
+++

**Abstract:** Our lab also researches SLAM (Simultaneous Localization
and Mapping) and Auotnomous Navigation.  We thought it would be fun to
combine these to see what we could get.  Using a wireless camera, we
gave it a shot. 
<!--more-->


Given that we were getting some decent results on monocular SLAM and
autonomous navigation using perception-space local planning, we figured
it would be fun to try to integrate all of the different research
threads to see if it was possible for Snakey to achieve semi-autonomous
locomotion.  We got close. You can see Snakey SLAM-Nav version 1.0 below
and also read about it [here](https://arxiv.org/abs/1908.07101).

{{<youtube UxFHa20I7zs>}} \

The problems we encountered with a monocular camera were sufficient that
we've decided to go with a stereo camera.  To get a monocular camera to
work, we had to use a bunch of older techniques (kind of like
[these](https://smartech.gatech.edu/handle/1853/24697)), plus make some
assumptions about the camera motion since a monocular setup lacks scale
recovery.  We should have some results soon.  Our aim is to submit them
for publication in March 2020.
