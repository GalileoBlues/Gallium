# How to install on Linux
1. Clone this repo.
2. Change into the Linux directory.
3. Make the directory `/usr/share/kbd/keymaps/i386/gallium`, then copy the contents of the `console` folder to it.
4. Find the directory `/usr/share/X11/xkb/symbols`, then copy the contents of the `xkb` folder to it.
5. To make sure it worked in the console, switch to a Virtual Terminal (TTY3 and 4 are typically unused), then run `loadkeys [the layout you want]`. For example, to use the rowstag layout, run `loadkeys gallium_rowstag`. If this worked without issues, you can make it persistent by following the instructions (here)[https://wiki.archlinux.org/title/Linux_console/Keyboard_configuration#Creating_a_custom_keymap].
6. To make it apply in a graphical environment, use your compositor/DE's settings program or configuration file to select either `gallium_rowstag` or `gallium_colstag` after editing your system's or user XKB `evdev.xml` file.
