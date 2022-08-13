## VSCode :: Custom CSS

Install [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css) extension. To successfully run *Enable Custom CSS and JS* command in VSCode, run:
```
sudo chown -R $(whoami) $(which code)
sudo chown -R $(whoami) /usr/share/code
```

Create a CSS file for setting some nice padding and shadowing to Doc Popup and Intellisense (code completion) windows, such as:
```css
/* --- --- Doc Popup Window --- --- */

.monaco-editor .monaco-hover {
  border-radius: 8px 8px 8px 8px;
  box-shadow: 0 0 12px 12px rgba(0, 0, 0, 0.2);
  padding: 8px;
}


/* --- --- IntelliSense Window --- --- */

.monaco-editor .suggest-widget {
  border-radius: 8px 8px 8px 8px;
  box-shadow: 0 0 12px 12px rgba(0, 0, 0, 0.2);
  padding: 8px
}
```

In `settings.json` file, include the full path to that file:
```json
"vscode_custom_css.imports": [
    "file:///home/dxps/dev/dxps-gh/design-assets/vscode/custom_css/vscode_custom.css"
]
```

In VSCode, run *Enable Custom CSS and JS* command (ctrl+shift+p).<br/>
Note: If you update the CSS file, you have to re-run _Enable Custom CSS and JS Loader_ command in VSCode.

