
## 2020-05

On my Xubuntu 20.04 I am using [`settings__xubuntu_snap.json`](./settings__xubuntu_snap.json) file as VSCode settings.


## Theme specifics

- [Qiita theme > Status Bar colors](qiita_theme.md)

<br/>

## Status Bar > BG & FG when Debugging

Settings to customize the foreground and background of the status bar when you are in debug mode and the theme comes with unpleasant colors for the status bar:

```json
{
    "workbench.colorCustomizations": {
        "statusBar.debuggingBackground": "#203447",
        "statusBar.debuggingForeground": "#4B987E",
    },
}
```

## Dart > Closing Labels

You can turn off showing the closing labels using:
```json
{
    "dart.closingLabels": false,
}
```

## Debug Console > A very condensed font

This is what I currently use:
```json
{
    "debug.console.fontFamily": "PhoenicaMono200, '64-SRC-Medium'",
}
```

## Old Note

The current version 1.9.0 does not provide (yet) support (options) for customizing the status bar.

Meanwhile, the following commands can be used from Developer Tools (`Help > Toggle Developer Tools`):
```javascript
document.getElementById("workbench.parts.statusbar").style.background = "#333"
document.getElementById("workbench.parts.statusbar").style.color = "gray"
```
And this is the result:

![](https://github.com/visvadw/design-assets/raw/master/vscode/images/statusbar-custom-dark-1.png)

