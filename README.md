# screencast-script
Screencast script using ffmpeg
###Reminders
- As for audio input `-i hw:1`, since the default audio capturing device is different on each machine, we can issue `arecord -l` to get a list of recording cards/devices available.
- As for video input `-i :0.0+1366,0`, this means recording the screen starting with the upper-left corner at (x=1366, y=0), cuz I'm using an external monitor and I just want to record that monitor instead of recording both.
- I'm using `libx264` as my video codec, it accepts options like `-preset`, `-threads`. Here I've set `-preset ultrafast`, there are also `superfast`, `veryfast`, `faster`, etc. Read more [here](https://trac.ffmpeg.org/wiki/Encode/H.264#a2.Chooseapreset). I left `-threads` unset to use the default, also optimal (says [here](http://superuser.com/a/726379)).
