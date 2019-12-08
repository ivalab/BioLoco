+++
showonlyimage = false
draft = false
image = "imgs/scales/scale_case.png"
date  = "2019-11-05"
title = "Creating Snake-Like Robot-Ground Interactions."
tags  = ["Snakey"]
+++

**Abstract:** To reproduce the locomotion modalities associated to snakes
requires achieving the same robot-ground contact force interactions.
Following the biomechanics literature we designed a robosnake scale
chassis to put on each of Snakey's joints. Doing so improved locomotion
stability.
<!--more-->

Snake chassis design involved creating a surface with anisotropic
properties. Our initial design involved an exagerated profile for the
scales on the ground contacting portion of the chassis. We elected for
curved extrusions that extended in width while sharpening to a flat
edge. The idea was to act like a sharper version of a fingernail since
close up images of snake scales do look like fingernails.  Close up
views of the scale elements and the chassis are below.

![snakey scale chassis][1]

In addition to the scaled version, we designed the top part of the
chassis to be flat. Wrapping the snake with thick material (obtained
from rugged worker pants) led to an isotropic ground-contact forcing
profile.  This additional modification permitted comparison with the
isotropic baseline, which is a design used when for non-wheeled snake 
robot designs.  Running head-to-head comparisons shows that not only do
the scales enhance distance travelled over different ground substrates,
but it also stabilizes the direction of motion.

The figures below depict the head-to-head comparisons for three
different locomotion gaits on carpet. The upper row is with scales and
the lower row is with the isotropic cloth.

Lateral undulation:
![carpet:lateral:scales][2]
![carpet:lateral:isotropic][3]
Rectilinear locomotion:
![carpet:rectilinear:scales][4]
![carpet:rectilinear:isotropic][5]
Sidewinding:
![carpet:sidewinding:scales][6]
![carpet:sidewinding:isotropic][7]

If the ground was a bit more slippery with less give in it (like
concrete), then the isotropic surface profile had a higher heading
variance and could not move straight. The anisotropic, scaled surface
drifted some, but preserved the direction of motion much better.
For more details the manuscript is
[here](https://doi.org/10.1017/S0263574718001522).   You can also see
some of the head-to-head races on this [YouTube
playlist](https://www.youtube.com/playlist?list=PLWPjf-IY-3dFOkjEfQgY5STX5Bm1tJogE).


[1]: /BioLoco/public/imgs/scales/snakey_cad_design_all.png
[2]: /BioLoco/public/imgs/scales/carpet/tiled_image_lateral_undulation_anisotropic_natural.png
[3]: /BioLoco/public/imgs/scales/carpet/tiled_image_lateral_undulation_isotropic_natural.png
[4]: /BioLoco/public/imgs/scales/carpet/tiled_image_rectilinear_anisotropic_natural.png
[5]: /BioLoco/public/imgs/scales/carpet/tiled_image_rectilinear_isotropic_natural.png
[6]: /BioLoco/public/imgs/scales/carpet/tiled_image_sidewinding_anisotropic_natural.png
[7]: /BioLoco/public/imgs/scales/carpet/tiled_image_sidewinding_isotropic_natural.png

