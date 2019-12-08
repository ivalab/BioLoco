+++
showonlyimage = false
draft = false
image = "imgs/rectilinear/traveling_wave_body.png"
date  = "2019-11-05"
title = "Rectilinear Snake Motion."
tags  = ["Snakey","Rectilinear"]
+++

**Abstract:** Rectilinear locomotion is different from but analagous to
caterpillar locomotion. The body undulates vertically to move
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
You can see an overhead video [here](https://youtu.be/Q9hvddTjHXw).
Because our snake is discretized, this forward motion is more of a roll,
then slide, then roll, then slide, depending on whether the scales lie
flat on the ground (slide) or they have angled contact with the ground.

Two visualized scenarios of closed-loop tracking of trajectories
synthesized using optial control are depicted below. You can see 
sample videos of the snake in action at this
[playlist](https://www.youtube.com/playlist?list=PLWPjf-IY-3dFbyMUB6BIKD1s9-LehFwie), for the scenarios
depicted below.  The playlist has different versions of our trajectory
planning and tracking algorithms to date. The video are typically sped
up 12x or so because rectilinear motion is quite slow.  Our snake
travels at around 22 mm/s.  It really is a function of the discretized
snake links, as they are the primary factor in not achieving the
theoretically derived top speed (of around 150-200 mm/s).
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
An improved and extended version has been submitted for publication,
while a more complete bendable model has also been implemented using
the methods from our 
[Bendable Lp
paper](https://arxiv.org/abs/1712.06021). Snakey gets modeled as a
tube.  We are working on this publication.  

#### Trajectory Planning and Tracking

How to successfully plan and execute trajectories for snake robots
still requires investigation.  Besides working out the dynamics, it is
important to also work out the body - environment interactions.  For
example, if the robotic snake should not touch or hit any obstacles,
then incorporating that into the planning is interesting because 
Snakey is an articulated robot.  Its shape can change based on the
motor commands.  First we modeled snakey as points, then as a set of
three smaller boxes, and finally as a bending tube (in 2D and 3D).
This progression got tougher and tougher to model and incorporate
mathematically, which meant that we had to create new approaches to
synthesize the trajectories.  Our latest version of cotnrolling Snakey
during rectilinear locomotion using the tube model is below.  

{{<youtube ewzWINxfBKc>}}

You can see the tube overlay in yellow.  Sometimes the tube
doesn't exactly fit. This is because it takes time for Snakey to change
from one shape to the next.  Within a second or so, it should match the
overlay.  The obstacle boundaries and their inflated versions, for
safety, are also depicted around the obstacle regions.  The overlays
basically show you what the trajectory planner knows or has computed.
Stability of Snakey limits how much Snakey can curve before
tipping to the side, which also limits how quickly Snakey can turn.
That means this gait is not good for scenarios requiring tight turns.
For that Snakey will have to learn a new gait for moving forward, or
will have to learn how to turn-in-place. right now we are focused on
having Snakey turn in place.  After that, we will look into other more
manueverable gaits.
