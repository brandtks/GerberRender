README
======
**Gerber Render**

Renders gerber files into png image(s) that represent what the front and back of the PCB will look like in real life. Inspired by the [gerblook](gerblook.org) website and its constant down time.


### Dependencies
 * [gerbv](http://gerbv.geda-project.org/) Renders the gerber files
 * [ImageMagick](https://www.imagemagick.org) Makes everything pretty
 
### Installation and usage
Install the dependencies: `sudo apt install gerbv imagemagick`. 

Clone the GerberRender repository: `git clone https://github.com/brandtks/GerberRender.git`.

GerberRender can be ran by simply running `gerbrend [options...]`. Running the command without any options uses the defaults variables to render both the front and back images and searches the local directory for the gerber files to use. Recommend either moving or creating a link to the gerbrend file to somewhere the terminal can find it. 

### Options
 * __-F__ Only render the front gerber files
 * __-B__ Only render the back gerber files
 * __-r__ Set the final image resolution
 * __-p__ Defines the solder mask/PCB color. Can only be green, red, blue, yellow, black, or white
 * __-w__ Defines the silk screen color. Can only be black or white
 * __-c__ Defines the copper color. Can only be silver and gold
 * __-l__ Directory location containing the gerber files
 * __-x__ Keep temporary working directory, contains the images for all the intermediate steps
 * __-o__ Path to outline gerber file
 * __-d__ Path to drill gerber file
 * __-f__ Path to front copper gerber file
 * __-m__ Path to front solder mask gerber file
 * __-s__ Path to front silk screen gerber file
 * __-b__ Path to back copper gerber file
 * __-n__ Path to back solder mask gerber file
 * __-t__ Path to back silk screen gerber file
 * __-i__ File name of the final rendered front image
 * __-j__ File name of the final rendered front image
 
### Gerber Extensions
The script searches for the different layers based on the following rules:

 * __Outline__ \*.out, \*.oln, \*.gm1, \*.gbr, \*.gml, \*.gko, \*.gm16, \*board.gbr
 * __Drill__ \*.dri, \*.drl, \*.drd, \*.txt
 * __Front Copper__ \*.gtl, \*.cmp, \*.top, \*toplayer\*.ger, \*top\*copper.\*
 * __Front Solder Mask__ \*.gts, \*.stc, \*.smt, \*topsoldermask\*.ger, \*top\*unmask.\*, \*top\*mask.\*
 * __Front Silk Screen__ \*.gto, \*.sst, \*topsilkscreen\*.ger, \*top\*silk.\*
 * __Back Copper__ \*.gbl, \*.sol, \*.bot, \*bottomlayer\*.ger, \*bottom\*copper.\*
 * __Back Solder Mask__ \*.gbs, \*.sts, \*.smb, \*bottomsoldermask\*.ger, \*bottom\*unmask.\*, \*bottom\*mask.\*
 * __Back Silk Screen__ \*.gbo, \*.ssb, \*bottomsilkscreen\*.ger, \*bottom\*silk.\*

### License
GerberRender is released under the terms of the MIT. See LICENSE for details.

### Website
 * [HackADay Build Log]()
