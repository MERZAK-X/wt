# Windows Terminal Tweaks
![wt](https://raw.githubusercontent.com/microsoft/terminal/master/res/terminal.ico)
## [wt.reg](https://github.com/MERZAK-X/wt/blob/master/wt.reg)
> This registry will make you able to have an _Open in Windows Terminal_ option for folders like the one in Linux distros

![wt](https://i.imgur.com/ZhjShTy.png)

Before installing this registry you must change **{USERNAME}** with your current _user folder name_ in the [Line 12](https://github.com/MERZAK-X/wt/blob/master/wt.reg#L12) & optionally specify an [icon](https://raw.githubusercontent.com/microsoft/terminal/master/res/terminal.ico) by uncommenting and setting its path in the [`wt.reg`](https://github.com/MERZAK-X/wt/blob/master/wt.reg#L8).

``` reg
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\Background\shell\WindowsTerminal]
@="Open in Windows Terminal"

; Uncoment and set your custom icon path
;"Icon"="%USERPROFILE%\\AppData\\Local\\Icons\\wt.ico"

[HKEY_CLASSES_ROOT\Directory\Background\shell\WindowsTerminal\command]
@="\"C:\\Users\\{USERNAME}\\AppData\\Local\\Microsoft\\WindowsApps\\wt.exe\" -d ."

```

<br>

## Uninstall

Open `regedit` from `Win + R` Run prompt, go to `Computer\HKEY_CLASSES_ROOT\Directory\Background\shell\WindowsTerminal` from the path bar, then right click the *Windows Terminal* folder and click delete.

![rm wt.reg](https://i.imgur.com/yJzaGww.png)
