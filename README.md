OverlapPolygonVS
================

Show the overlap of two polygons in 3d space(Visual Studio 2010 Version)

1. What does this program do?

This program transforms (including rotation, panning and zooming) rotates two polygons in the 3D space and show their overlap part of the two polygons
in real time.

2. How to run and use this program?

Use Visual Studio 2010 to run this program. 

Two parallel triangles(one Cyan, one Red) are shown in the 3D space are shown in the glut window. The overlap part of the
two triangles is shown with Black color. When you rotate the triangles(i.e. see two triangles from differnt view), you 
can see the changing overlap part in real time.

3. How do I implement this program?

The depth buffer(i.e. Z-buffer) is used to check whether two polygons overlap or not for each pixel. 

Baic Steps of checking overlap:

a. Draw first polygon P1 and read the Z-buffer Z1 for all pixels.

b. Clear the color buffer and Z-buffer. 

c. Draw second polygon P2 and read the Z-buffer Z2 for all pixels.

d. Clear the color buffer and Z-buffer. 

e. Draw P1 and P2 again.

f. For the pixles whose depth of Z1 and Z2 are both not infinite(i.e. pixels occupied by both P1 and P2), draw them with
black color. Draw other not overlapping pixels with transparent color.

4. Languages and Tools 
OpenGL, C++, Visual Studio 2010

5. Ackowledgement

The mouse interaction part is from Gordon Wetzstein's SimpleGlut program. 
