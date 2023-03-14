# 3d-simple
Very simple 3d engine in Python via Jupyter Lab

## Scope
I've made this project for finding out if I could create a simple 3d engine from basically scratch purely based on what I know about 3d graphics and what my intuition tells me. Turns out: Yes, apparently I can.

⚠️ This 3d engine is neither complete nor optimized or production ready. Feel free to play around with it and have some fun.

## What it does
This 3d engine
- renders objects consisting of arbitrary n-gons with flat colors and an outlines
- honors colors with alpha
- supports perspective
- tries (badly) to sort drawing order by z-depth of the faces
- supports arbitrary rotation via euler angles
- applies fuzzy dithering as an effect to simulate image noise
- applies line shifting as an effect to simulate VCR tracking artefacts
- supports very simple math based animations
- renders any nummber of frames into a gif

## What it does not

This 3d engine does not
- load 3d model files
- shade faces based on light sources or normal direction (because it knows nothing about normals)
- render textures
- have optimized image effects for faster than realtime rendering of frames
- work well with extreme perspective values or coordinates in the far back
- have easily changeable parameters for a lot of things

## What I would change

This project met my needs and I got some nice animations out of it that I will use as logo animations for my next personal website.

If I were to continue this project I would
- create a more robust data format, probably split into a list of vertices and a list of faces referencing vertices
- implement a more robust way to determine z-depth of a face
- implement vertex colors (optional)
- immplement proper scaling or vertices based on depth so that they can't overshoot an arbitrary point but will shrink indefinitely the farther they are
- implement a proper camera system
- implement normal vectors for the faces to facilitate light based shading, fresnel shading and LUT based shading
- add keyframe based animation
- put all the parts that should be variable into a nice config object
- honestly … reimplement it in another programming laguage than Python
- think hard about why anyone would want to have a generalized simple 3d rendering engine that renders purely CPU based in a world where every computer supports opengl in some way
