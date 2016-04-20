# Prism Sort glitch algorithm
Copyright 2016 Mathieu Guimond-Morganti

This program is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/.

## Prerequisites
This Python 3 script requires the Pillow module and its dependencies.  
Try the command `$ pip3 install Pillow`
or visit http://pillow.readthedocs.org/en/3.1.x/installation.html

## Usage
`$ prismsort.py inputfile [options]`

##### Command-line parameters:
```
-a, --angle=NUM     : rotates the glitch effect by this many degrees  
                      (default: 0, i.e. vertical)  
-b, --blocks=NUM    : number of blocks (default: 9)  
                      affects the overlapping of the glitch effect  
                      (higher = more intense)  
-d, --dither        : makes result more noisy, and less blocky  
-f, --fuzzyedges    : in combination with a rotation, will leave a fuzzy black  
                      border around the image  
-h, --help          : displays this help message  
-H, --horizontal    : processes the image horizontally (same as -a 90)  
-i, --intensity=NUM : intensity [recommended: -2~2; default: 0]  
                      will not go lower than (3 - number of blocks)  
-J, --jpeg=NUM      : saves as JPEG at the specified quality  
                      (recommended: 75~95)  
-n, --numoutput=NUM : number of output files to be generated (default: 1)  
                      the output files are in the format:  
                      <originalfilename>_out<number>.<ext>  
                      files are overwritten without warning!  
-P, --png           : saves as PNG (default)  
-r, --resize=NUM    : resize factor (e.g. 2 divides side by sqrt(2); optional)  
-V, --vertical      : processes the image vertically (default; same as -a 0)  
```
##### Examples:
`$ prismsort.py IMG_20160419.jpg -n 10 -r 3 -a 45 -i -2 --fuzzyedges --jpeg 95`  
Creates 10 randomly glitched versions of that photo that are 1/3rd the size of the original, with a diagonal pattern at a 45° angle, and a slightly reduced intensity, with fuzzy (feathered) edges, and saves them in JPEG at 95% quality.
![© 2016 Mathieu Guimond-Morganti, licensed under CC-BY-SA 4.0](http://i.imgur.com/YqUpJrg.jpg)

`$ prismsort.py IMG_20160419.jpg -n 3 -H -d`  
Creates 3 randomly glitched versions of that photo, with a horizontal, dithered pattern.
![© 2016 Mathieu Guimond-Morganti, licensed under CC-BY-SA 4.0](http://i.imgur.com/4G3jSLf.png)

## Derivative Work

Images glitched using this algorithm should be licensed under CC-BY-SA 4.0 as well, with proper attribution, as I believe they constitute derivative work as covered under the terms of the license.

The reason for this humble request is to encourage people to further experiment with this algorithm or its variants, as well as remix other people's artwork.

I don't want this project to be solely "open source"; I want it to be "open art" as well.
If no one credits the use of this algorithm, fewer people will use it. And a world without glitch art would be sad :'(
