# Colormaps

A collection of custom colormaps for use in Python. Built using the viscm tool.
* See file cm_tester.ipynb for demos.

## run: 
* `python3 -m viscm edit cm.jscm`
* can leave off the cm.jscm
* Edit file, then save --> cm.jscm.
* Do file --> export py to get the corresponding python file.
* Note, creating a reversed map at the bottom

## To make the image file (pgm) using the ImageMagick convert tool:
* `convert jet.gif -colorspace gray -compress none -depth 8 jet.pgm`
* (Need a "plain" pgm file to get ascii, hence the compress and depth above.)
* Then reformat this to be 1-D. The first line is not part of the data (commented).

In viscm, the light intensity is 99 (100 didn't work) to get close to white, 
then, in `*cm.py` file, manually extrapolated last couple points and forcing 1.0 1.0 1.0.

For viridis and inferno, started with the python files for these. 
Then, multiply the x,y points by 0.8 to get them to live in the "valid" region in viscm.

