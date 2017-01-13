# What does this fork do?

- fixes bug where multiple monitors are not properly handled when the app is called via CLI https://github.com/hbt/x-tile/commit/d3def6b374b9cd7b7e47af0b797f415a01a5e4e8

# What is it?

x-tile is a desktop app to tile windows. It integrates effortlessly with your window manager and only does one thing well. Tiling.
If you hate using the window app, you can use the CLI app.

# Why build it?

There is [plenty](https://wiki.archlinux.org/index.php/window_manager#List_of_window_managers) of window managers. However, they each do more than needed and often do it poorly.

x-tile follows the unix philosophy: "One program, One purpose."


# What about other features? 

- Keyboard shortcuts = use `xbindkeys`
- remember window positions around workspaces = use `devilspie`
- mapping keyboard = use `xmodmap`
- moving around xinema = use `wmctrl script`
- for the rest, a regular window manager suffices e.g `metacity`


# How to install?

- clone
- ./x-tile

# How to configure it?

- ./x-tile
- Edit > Preferences


# How to map keyboard shortcuts?

```
xbindkeys-config

#tile horizontal
"x-tile h"
    m:0x1c + c:44
    Control+Alt+Mod2 + j 

#tile vertical
"x-tile v"
    m:0x1c + c:45
    Control+Alt+Mod2 + k 


```

# Usage

```
x-tile 

   w => open the x-tile main window without using the panel

   z => undo the latest tiling operation

   v => tile all opened windows vertically

   h => tile all opened windows horizontally

   u => tile all opened windows triangle-up

   d => tile all opened windows triangle-down

   l => tile all opened windows triangle-left

   r => tile all opened windows triangle-right

   q => quad tile all opened windows

   g = g 0 = g 0 0   => tile all opened windows in a grid with automatic rows and columns
   g rows = g rows 0 => tile all opened windows in a grid with given rows and automatic columns
   g 0 cols          => tile all opened windows in a grid with automatic rows and given columns
   g rows cols       => tile all opened windows in a grid with given rows and columns

   1 => custom tile 1 all opened windows

   2 => custom tile 2 all opened windows

   i => invert the order of the latest tiling operation

   y => cycle the order of the latest tiling operation

   m => maximize all opened windows

   M => unmaximize all opened windows

   c => close all opened windows


```


