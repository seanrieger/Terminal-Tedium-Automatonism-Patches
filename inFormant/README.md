This is a fairly complex Automatonism patch for the Teminal Tedium that utilizes 1v/o inputs to push 3 oscillators with multiple waveform configurations through 3 seperate formant filters that can be modulated automatically using sample & hold synced to your clock. It also has a ladder filter, and distortion that can be turned on or off with the TT and can also cyle through and display multiple waveforms on your OLED if you have one installed. For full info, see PatchSheet-Informant.jpg ofr instructions. It has been tested on a Raspberry Pi B variant of Terminal Tedium and the only occasional glitch is if you use a gate that is too fast to auto-cycle waveforms, it sometimes stops cycling, but continues ot play. To run it, simply upload the inFormant folder into your patches directory on your Terminal Tedium. SSH into your Pi and then run:

sudo /home/pi/PATH_TO_YOUR_PD_INSTALL/bin/pd -nogui -rt -midiindev 0,1 /home/pi/terminal_tedium/PATH_TO_YOUR_PATCHES_FOLDER/inFormant/main.pd

If you have an OLED installed the command would look like this:

sudo /home/pi/PATH_TO_YOUR_PD_INSTALL/bin/pd -nogui -rt -midiindev 0,1 /home/pi/terminal_tedium/PATH_TO_YOUR_PATCHES_FOLDER/inFormant/main.pd |&1 sudo python /home/pi/terminal_tedium/PATH_TO_YOUR_PATCHES_FOLDER/inFormant/tt-OLED.py

(For more info on installed an OLED to your TT see: https://github.com/oldmanfury/tt_EBS

Then patch your 1v/o CV into knob 1 and audio out to your mixer and test away. The CV input on Knob 1 is normalized to the other two oscillators, which you can then offset if you like. (Chords? Super thick detuning?) You will likely have to tune knob1 but everything should track accordingly.

For info on Terminal Tedium see: https://github.com/mxmxmx/terminal_tedium

For info on Automitonism see: https://www.automatonism.com/

For info on Old Man Fury's tt-Automatonism objects and other cool Terminal Tedium patches see: https://github.com/oldmanfury
