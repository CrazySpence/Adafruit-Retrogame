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

This Also has 3 button bombo handlers 
1 for KEY_ESC
1 for KEY_ENTER
1 for shutdown

ESC allows me me leave MAME, ENTER was needed for Quakeforge and the emrgency shut down is to handle any applicsation failures or crashes (super mario war 1.8) as it would require a hard lock of the system to thwart retrogame

