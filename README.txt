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

How to install:

1. cd to linux-makemkv-lite/extra and run ./install-udf2 as root
2. cd to linux-makemkv-lite and run "./install-makemkv-lite -s /path/to/unzipped/linux-makemkv-lite" as root
3. insert a Blu-Ray inside your disc device
4. mount -t udf2 /dev/cd0 /media/
5. makemkv-lite -s /media/

as a normal user it is now possible to run:
6. play-media 
