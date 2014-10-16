Adafruit-Retrogame retrogame.c
==================

Raspberry Pi GPIO-to-USB utility for classic game emulators.

How-to: http://learn.adafruit.com/retro-gaming-with-raspberry-pi

Pre-built version supports the default pin/key mapping shown in the tutorial. For other layouts, edit retrogame.c.

This one still contains the shut down code as well as the KEY_ESC wrapped in an #ifdef block

CrazySpence
===========
Retogame-arcadebox:

This contains my 12 GPIO mappings for my arcade setup

This Also has 3 button combo handlers 
1 for KEY_ESC
1 for KEY_ENTER
1 for shutdown

ESC allows me me leave MAME, ENTER was needed for Quakeforge and the emergency shut down is to handle any application failures or crashes (super mario war 1.8) as it would require a hard lock of the system to thwart retrogame

Retrogame-xbmc:

This contains my shut down button version

The button mask on this version takes a single button to initiate shutdown

SDL 2.0.3 or earlier FIX
=============
Replace the sdl_udev.c in your SDL source directory (src/core/linux/) with the one here and retrogame will work with SDL2 applications

This fix allows both SDL1.2 and 2.0 apps to work with retrogame

Beyond SDL 2.0.3
================
The SDL devs just posted this offical change to the udev handler:
https://bugzilla.libsdl.org/show_bug.cgi?id=2654

Hopefully this means going forward retrogame "just works" again with all breeds of SDL
