elementary-snippets
===================

This repository contains some handy scripts made with Elementary OS in thought, but some of these might actually be OK to work with on other distros as well.

# switch-workspace

Simple script for switching between Elementary OS desktops without additional, empty desktop. I've always been finding it annoying with the eOS built-in workspace switching that I had to switch throught this additional, empty one, so here is the fix.

## Installation

Copy *src/switch.workspace* file to /usr/local/bin.  

Install wmctrl:
```
sudo apt-get install wmctrl
```
Install xbindkeys:
```
sudo apt-get install xbindkeys
```
Generate default config for xbindkeys shortcuts:
```
xbindkeys --defaults > ~/.xbindkeysrc
```
Add switch-workspace to ~/.xbindkeysrc file with your custom shortcut, for example:
```
"switch-workspace"
alt+q
```
Open *System Settings -> Applications -> Startup* and add custom command: xbindkeys  

Enjoy!