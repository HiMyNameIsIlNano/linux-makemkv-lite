MakeMKV
-------

http://www.makemkv.com/

MakeMKV for Linux: http://www.makemkv.com/forum2/viewtopic.php?f=3&t=224

The makemkv program has two parts.  First part is the core of
makemkv.  Its a console command -- makemkvcon, and its binary.
Second part of makemkv is client front-end, written on QT4, and
this part is open-source.

Currently, its possible to run a lightweight version of makemkv using the
linux emulation layer under FreeBSD10.

-------------
Requirements:
-------------
1. the linux emulation layer for freebsd (see https://www.freebsd.org/doc/handbook/linuxemu-lbc-install.html)

----------------------------------
How to install linux-makemkv-lite:
----------------------------------
1. Download the zip file from https://github.com/HiMyNameIsIlNano/linux-makemkv-lite/archive/master.zip 
(e.g. curl https://github.com/HiMyNameIsIlNano/linux-makemkv-lite/archive/master.zip -o /tmp/linux-makemkv-lite.zip);
2. Unzip it (e.g. under /tmp/linux-makemkv-lite);
3. as root cd into linux-makemkv-lite/extra and run ./install-udf2;
4. as root cd into linux-makemkv-lite and run "./install-makemkv-lite -s /path/to/unzipped/linux-makemkv-lite".

------------------------------
How-to run linux-makemkv-lite:
------------------------------
1. insert a Blu-Ray inside your Blu-Ray disc reader;
2. mount -t udf2 /dev/cd0 /path/to/mount_folder/ (e.g. /media/);
3. as root run makemkv-lite -s /path/to/mount_folder/;
4. as a normal user it is now possible to run play-stream -fp mpv (i.e. it forces the usage of the media player "mpv").

-------------------------------
How-to update the beta key:
-------------------------------
1. as root run update-license-key;

----------------------------------------
How-to update the aacs key database:
----------------------------------------
1. as root run update-aacs-key;

Facts:
1. if a given Blu-Ray cannot be played please try and update the aacs key database and re-run makemkv-lite.
2. during my tests I have noticed that the best player to use for reproducing the ripped contents is "mpv". Even though the "play-stream"
scripts supports "mplayer" most of the times the stream cannot be reproduced. I will try to improve the support for "mplayer" in the near future. 

To-do:
bug fixing 
