README
======
**Gerber Render**

'gerbrend' renders gerber files into png image(s) that represent what the PCB will look like in real life.

### Status
So far so good

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
 * __-x__ Check temporary working directory, contains the images for all the intermediate steps
 * __-o__ File extension of the outline gerber file
 * __-d__ File extension of the drill gerber file
 * __-f__ File extension of the front copper gerber file
 * __-m__ File extension of the front solder mask gerber file
 * __-s__ File extension of the front silk screen gerber file
 * __-b__ File extension of the back copper gerber file
 * __-n__ File extension of the back solder mask gerber file
 * __-t__ File extension of the back silk screen gerber file
 * __--front_image=...__ File name of the final rendered front image
 * __--back_image=...__ File name of the final rendered front image     
 * __--outline=...__ Path to outline gerber file
 * __--drill=...__ Path to drill gerber file
 * __--front_copper=...__ Path to front copper gerber file
 * __--front_mask=...__ Path to front mask gerber file
 * __--front_silk=...__ Path to front silk gerber file
 * __--back_copper=...__ Path to back copper gerber file
 * __--back_mask=...__ Path to back mask gerber file
 * __--back_silk=...__ Path to back silk gerber file

### License
GerberRender is released under the terms of the MIT. See LICENSE for details.

### Website
 * [HackADay Build Log]()
