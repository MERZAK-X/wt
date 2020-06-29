# Windows Terminal Tweaks
![wt](https://raw.githubusercontent.com/microsoft/terminal/master/res/terminal.ico)
## [wt.reg](https://github.com/MERZAK-X/wt/blob/master/wt.reg)
> This registry will make you able to have an _Open in Windows Terminal_ option for folders like the one in Linux distros

Before installing this registry you must change **{USERNAME}** with your current _user folder name_ & optionally specify an icon (download the one above and set its path in the `wt.reg`).

``` reg
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\Background\shell\WindowsTerminal]
@="Open in Windows Terminal"

; Uncoment and set your custom icon path
;"Icon"="%USERPROFILE%\\AppData\\Local\\Icons\\wt.ico"

[HKEY_CLASSES_ROOT\Directory\Background\shell\WindowsTerminal\command]
@="\"C:\\Users\\{USERNAME}\\AppData\\Local\\Microsoft\\WindowsApps\\wt.exe\" -d ."

```
