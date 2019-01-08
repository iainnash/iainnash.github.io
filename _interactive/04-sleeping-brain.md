---
title: sleeping brain
date: 09/09/2017
collaboration: hackathon team
action: view installation overview
link: https://medium.com/@isiain/visualizing-your-sleeping-brain-1bbf0917ef25
summary: built a visualization of the brain during sleep with opengl shaders and touchdesigner 
img: /img/dreaming-bg.png
tech: opengl, touchdesigner, osc, gsgl, python
---

at the 2017 ars electronica festival in linz iain worked on a team of scientists and coders
to visualize the sleeping brain

this classifier picked up signals from the motor cortex (signals of intention to move muscles) and differentiated movements from the left and the right side of the body. The classifier was built using Linear Discriminant Analysis —a method to classify a linear combination of data that characterizes classes of objects or events — in this case motor cortex movement activity. Since the motor cortex is active during sleep in some way, we can use this data to visualize what movement intentions are occurring during a dream or sleep and plot those into a space.

to export the data from Matlab into TouchDesigner using a custom python bridge that replayed the processed data capture from Matlab to an Open Sound Control (OSC) protocol. We chose to use OSC because it allowed for real-time streaming of complex sets of data easily into touch designer, allowing us to use those variables to influence the progression of the visualization. After some iteration and brainstorming, we decided to build a simpler star field animation that would add particles and increase a visual glow intensity given alpha wave brain activity