# This repository contains things that may help making Mahou for linux.

Nothing special, just hooks, event listeners etc.

# Also projects which source code may be helpful:

- xinput
- xev
- ...

# keyboard-testing.py

Uses [keyboard](https://github.com/boppreh/keyboard) framework.
Has ability to change last word on f7 key press, though for it to work you'll need to set keyboard shortcut Alt+Shift to change layout in system settings, clear last word on some keys press **has no mouse clicks clear**.

# X11-Hooks.c

compile with `gcc X11-Hooks.c -pthread -lX11 -lXtst -oX11-Hooks`.
Listens to keyboard and mouse events globally. Has no conversion functions at moment. 
For mouse events support you need to specify your mouse device, for example for me its:
```
./X11-Hooks /dev/input/by-path/platform-i8042-serio-1-event-mouse
```
Also `sudo` is **required** for keyboard/mouse hooks to work globally without errors.

F7 to simulate input of **1** on keyboard. F4 to exit.

# by-dict-conversion.py

Has basic string conversion from english to russian and vice versa keyboard inputs, using dictionary I created in it. 

# current-layout.sh and all-layouts.sh

Details in files.
