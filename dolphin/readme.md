# A stylesheet for Dolphin

This is the style sheet that I use for Dolphin file manager.
To use it, Dolphin needs to know about it through a flag: `dolphin -stylesheet dolphin.css`

On Gnome desktop environment, a "desktop shortcut" can be used for this purpose:

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

<br/>

## Additional Customizations

### Start with the stylesheet by default

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

<br/>

### QT5 Customizations

Besides installing Dolphin using:

```shell
sudo add-apt-repository ppa:kubuntu-ppa/backports
sudo apt update
sudo apt install dolphin
```

I also installed _Qt5 Settings_ tool using `sudo apt install qt5ct`.

Added `QT_QPA_PLATFORMTHEME=qt5ct` to `/etc/environment` file.

Started _Qt5 Settings_ and:

-   in Appearance tab, set Style: gtk2
-   in Fonts tab, set General: Fira Sans 11 and Fixed width: 64-SRC-DZ-MEdium-NerdFont 10
