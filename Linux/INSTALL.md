# How to install on Linux
1. Clone this repo.
2. Change into the Linux directory.
3. Make the directory `/usr/share/kbd/keymaps/i386/gallium`, then copy the contents of the `console` folder to it.
4. Find the directory `/usr/share/X11/xkb/symbols` (or the same folder in your user directory), then copy the contents of the `xkb` folder to it.
5. To make sure it worked in the console, switch to a Virtual Terminal (TTY3 and 4 are typically unused), then run `loadkeys [the layout you want]`. For example, to use the rowstag layout, run `loadkeys gallium_rowstag`. If this worked without issues, you can make it persistent by following the instructions (here)[https://wiki.archlinux.org/title/Linux_console/Keyboard_configuration#Creating_a_custom_keymap].
6. In order to apply the layout to your graphical environment we need to edit a few system files so they will be viewable, navigate to `/usr/share/X11/xkb/rules` and you will find `evdev.xml, evdev.lst, base.xml and base.lst.` files. Which two you will need to edit will depend on your specific desktop environment (attempt editing evdev files first).
7. In the XML files you will need to create either a new layout entry or a variant entry, navigate to and copy the entry you would like then edit it for your preferred gallium variant.
8. In the LST files you can simply navigate to the bottom of the file and rename the layout named "custom" to the same name you gave your XML entry.
9. To apply your layout in a graphical environment, use your compositor/DE's settings program or configuration file to select your desired gallium variant after editing your system's XKB configuration. Repeat steps 7-9 with `base.xml` and `base.lst` if your layout does not appear.
