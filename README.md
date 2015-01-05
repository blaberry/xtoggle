What is xtoggle?
======
xtoggle is a small script for pausing and unpausing processes by clicking an X11 window connected to a process.
You run it, then you click a window, pretty much like xkill, the window's PID is then taken from the X11 window hints.
If a PID is found, the script figures out whether the process is paused or not and sends the approriate signal. (SIGSTOP/SIGCONT)

Caveats
------
X11 hints are mostly volountary to include and a lot of small programs don't include them.
xkill doesn't use PIDs, it simply tells X11 to close the window client connection, which makes the process die as well. This isn't an alternative when you want to send specific signals, afaik. 

Dependencies
------
It depends on xwinfo, kill, ps and grep.

License
------
This software is licensed under [GPLv3](http://www.gnu.org/copyleft/gpl.html).

Enjoy ❤❤❤