# DWM
DWM is my favorite window manager by far due to its simplicity, portability, and low resource usage. However, it requires a decent amount of tweaking if you want to be able to use it for standard tasks. That's what I've aimed to do here, creating a user-friendly environment and memorable keybinds.
## Compiling
### Dependencies
X11, xinerama, xcb, freetype
### Instructions
Run `./configure` to properly set up `config.mk`.
#### Linux
`make && sudo make install`
#### FreeBSD, OpenBSD
`gmake && doas gmake install`
## Patches applied
#### These patches were applied with [dwm-flexipatch](https://github.com/bakkeby/dwm-flexipatch) and stripped with [flexipatch-finalizer](https://github.com/bakkeby/flexipatch-finalizer)
```
dwmblocks (statuscmd)
dwmblocks (SIGUSR1)
bar layout symbol -- show window layout in status bar
bar status -- show status in bar
bar tags -- show tag symbols in bar
bar window title -- show window title in bar
bar alpha -- semi-transparency on bar
bar hide vacant tags -- hide tags with no windows
attach aside -- add new windows to stack instead of master
cool autostart -- execute commands on start and have processes owned by dwm
dwmc -- use dwmc program to execute dwm commands (for scriptability)
fullscreen -- applies monocle layout on active window and hides bar
moveresize -- resize dwm windows with keybinds
movestack -- allows to move windows in stack and to become master
no transparent borders -- make window borders always solid
scratchpads -- allow for scratchpad terminals
swallow -- hide terminal window when it spawns a window and freezes itself (not working on OpenBSD)
togglefullscreen -- use a keybind to make a window fullscreen or not
vanitygaps -- add gaps between all windows
xrdb -- allows dwm to read colors from xrdb (.Xresources) at run time
```

## Software Made to Work With This
- [DWMBlocks](https://github.com/maneater2/dwmblocks)
- [DMenu](https://github.com/maneater2/dmenu)
- [ST](https://github.com/maneater2/st)

## Keybinds
All keybinds can be found by running `man dwm`, but here are the important ones:
- `Super + Enter` - Spawn terminal (st)
- `Super + Shift + Enter`, `F12` - Toggle scratchpad terminal
- `Super + h/l` - Shrink/enlarge master window
- `Super + d` - dmenu\_run (program launcher)
- `Super + q` - Kill window
- `Super + b` - Toggle status bar
- `Super + f` - Toggle fullscreen
- `Super + m` - Set window as master
- `Super + o/O` - Increase/decrease number of masters
- `Super + j/k` - Move focus down/up
- `Super + Shift + j/k` - Move window in stack down/up
- `Super + Shift + e`, `Super + Shift + e` - Kill DWM
- `Super + Space` - Set all windows to Floating mode
- `Super + [Arrow]` - Move window in direction of arrow pressed
- `Super + Shift + [Arrow]` - Expand/shrink window in direction of arrow pressed (only works on floating windows)
