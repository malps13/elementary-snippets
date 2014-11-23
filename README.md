elementary-snippets
===================

This repository contains some handy scripts made with Elementary OS in thought, but some of these might actually be OK to work with on other distros as well.

# switch-workspace

Simple script for switching between Elementary OS desktops without additional, empty desktop. I've always been finding it annoying with the eOS built-in workspace switching that I had to switch throught this additional, empty one, so here is the fix.

## Installation

1. Copy *src/switch.workspace* file to /usr/local/bin.
2. Install wmctrl:
```
sudo apt-get install wmctrl
```
2. Install xbindkeys:
```
sudo apt-get install xbindkeys
```
3. Generate default config for xbindkeys shortcuts:
```
xbindkeys --defaults > ~/.xbindkeysrc
```
4. Add switch-workspace to ~/.xbindkeysrc file with your custom shortcut, for example:
```
"switch-workspace"
alt+q
```
5. Open *System Settings -> Applications -> Startup* and add custom command: xbindkeys
6. Enjoy!