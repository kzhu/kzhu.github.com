---
layout: blog_entry
title: Visualising Pi
image: /img/pi.jpg
category: blog
preview: As part of my plan to get more fluent with prototyping in code, I decided to build a 3D, animated visualisation of Pi using <a href="http://processingjs.org">Processing.JS</a>.
extra_css: css/pi_vis.css
extra_js: 
- files/processing.js
- files/pi_vis.js
---

As part of my plan to get more fluent with prototyping in code, I decided to build a 3D, animated visualisation of Pi using [Processing.JS](http://processingjs.org). The result is here:
<code>
	<canvas id="pi_vis" data-processing-sources="files/sphere_master_v3.pde" style="image-rendering: -webkit-optimize-contrast !important;"></canvas>
</code>

Pi is an [enigmatic concept](http://en.wikipedia.org/wiki/Pi). On the one hand we can look at it simply as the ratio between the diameter of a circle and its circumference. On the other its an infinitely long number that, if proven to be randomly distributed, theoreticallys contain [all possible information in the universe](http://math.stackexchange.com/questions/216343/does-pi-contain-all-possible-number-combinations). For the purposes of this hack I decided to choose the former interpretation.

To begin with I generated a long string of Pi digits using [Machin's formula](http://www.craig-wood.com/nick/articles/pi-machin/). Fortunately, I could pull the bulk of the implementation from this [tutorial](http://docs.oracle.com/javase/tutorial/rmi/client.html). I then displayed these digits as circles of varying size distributed on the surface of a sphere. This was simply a matter of plotting spherical polar coordinates in 3D space. Finally, I used panned the camera angle to give the appearance of movement.

Main Lesson learnt; __Processing Sucks Ass__. There is no easy way to debug you program. Switching between Processing and ProcessingJS results in various parts breaking. Don't ge me wrong, it allowed me to get up and running very fast. I am happy with the end result, however, in future I will probably first attempt to use a modern language such as Python.

_Apologies if this doesn't display properly on your device. If anyone can suggest how to make the sketch responsive I'm all ears.<br>
The source code for this project is on [Github](https://github.com/kzhu/pi).<br>
The header photo is courtesy of [sarahwynne.](http://www.flickr.com/photos/goddess-arts/)_