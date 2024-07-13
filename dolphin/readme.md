# A stylesheet for Dolphin

This is a style sheet for Dolphin file manager.
To use it, you need to start Dolphin using `dolphin -stylesheet dolphin.css`

On Gnome desktop environment you can use this "desktop shortcut":

```shell
~ ❯ cat ~/.local/share/applications/dolphin.desktop
[Desktop Entry]
Version=1.0
Type=Application
Name=Dolphin File Manager
Icon=system-file-manager
Exec=dolphin -stylesheet /home/dxps/dev/dxps_gh/design-assets/dolphin/dolphin.css
Comment=Dolphin File Manager
Categories=FileManager;
Terminal=false
StartupWMClass=dolphin
~ ❯
```

Additionally, since Dolphin does not support a default stylesheet, in order to have it correctly started from Pop!\_OS Dock,
I had to do the following customization:

```shell
/usr/bin ❯ ls -l dolphin*
-rwxr-xr-x 1 root root      95 Jul 13 17:34 dolphin
-rwxr-xr-x 1 root root 1034712 Jul  5  2022 dolphin.bin
/usr/bin ❯
/usr/bin ❯ cat dolphin
#!/bin/sh

dolphin.bin -stylesheet /home/dxps/dev/dxps_gh/design-assets/dolphin/dolphin.css &

/usr/bin ❯
```
