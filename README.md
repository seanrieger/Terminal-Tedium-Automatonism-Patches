# Terminal-Tedium-Automatonism-Patches
These are patches built in Automatonism using Old Man Fury's tt-Automatonism objects specifically built to run on the Terminal Tedium, a DIY, Raspberry Pi-based Eurorack Module created by mxmxmx

Each folder contains everything you need to run a patch on your Terminal Tedium. I suggest that you run the very simlple 1V/O Test patch first to orient yourself. It's just a saw wave controlled by a CV input from the first knob on your TT.  To run it, simply upload the 1voauto folder into your patches directory on your Terminal Tedium. SSH into your Pi and then run: 

sudo /home/pi/PATH_TO_YOUR_PD_INSTALL/bin/pd -nogui -rt -midiindev 0,1 /home/pi/terminal_tedium/PATH_TO_YOUR_PATCHES_FOLDER/1vauto/main.pd

If you have an OLED installed the command would look like this:

sudo /home/pi/PATH_TO_YOUR_PD_INSTALL/bin/pd -nogui -rt -midiindev 0,1 /home/pi/terminal_tedium/PATH_TO_YOUR_PATCHES_FOLDER/1voauto/main.pd |&1 sudo python /home/pi/terminal_tedium/PATH_TO_YOUR_PATCHES_FOLDER/1voauto/tt-OLED.py

(For more info on installed an OLED to your TT see: https://github.com/oldmanfury/tt_EBS

Then patch your 1v/o CV into knob 1 and audio out to your mixer and test away. You will likely have to tune knob1 but everything should track accordingly. 

For info on Terminal Tedium see: https://github.com/mxmxmx/terminal_tedium

For info on Automitonism see: https://www.automatonism.com/

For info on Old Man Fury's tt-Automatonism objects and other cool Terminal Tedium patches see: https://github.com/oldmanfury

