+++
showonlyimage = false
draft = false
image = "imgs/rectilinear/traveling_wave_body.png"
date  = "2019-11-05"
title = "Rectilinear Snake Motion."
tags  = ["Snakey","Rectilinear"]
+++

**Abstract:** Rectilinear locomotion is different from but analgous to
caterpillar locomotion. The body undulates vertically only to move
forward. Curving the body leads to turning.
<!--more-->

The easiest gait to analyze, produce, and control is the rectilinear
locomotion gait. It is not because the other gaits are necessarily
harder to work out, but because rectilinear locomotion is so slow!
That permits us the ability to use our overhead tracking system for
performing closed-loop control without worrying about the snake going
out of bounds.  A few gaits of sidewinding and the snake isn't in the
field of view anymore.

Rectilinear locomotion is a bit like caterpillar movement, but different
in terms of the underlying robot-ground interaction.  A travelling
wave propogates from the back-end of the snake to the front-end.  Doing
so creates a rolling-like property that leads to forward motion.
Because our snake is discretized, this forward motion is more of a roll,
then slide, then roll, then slide, depending on whether the scales lie
flat on the ground (slide) or they have angled contact with the ground.

Two visualized scenarios of closed-loop tracking of trajectories
synthesized using optial control are depicted below. You can see a
sample video of the snake in action
[here](https://www.youtube.com/watch?v=zMIiXi-pG18), for the scenarios
depicted below.  The video was sped up 12x because rectilinear motion is
quite slow.  It really is a function of the discretized snake links, as
they are the primary factor in not achieving the theoretically derived
top speed.
<div style="display:flex;flex-flow:row nowrap;padding:0px 0px 0px
0px;margin:0px 0px 0px 0px;justify-content:center;align-items:center">
  <div style="flex:50%">
  <img src="/BioLoco/public/imgs/rectilinear/obst_exper_02_exp_scen.png">
  </div>
  <div style="flex:50%">
  <img src="/BioLoco/public/imgs/rectilinear/obst_exper_03_exp_scen.png">
  </div>
</div>

The method and mathematics was first presented at ICRA in 2017
([abstract](https://ieeexplore.ieee.org/document/7989404)). 
An improved and extended version has been submitted for publication.
