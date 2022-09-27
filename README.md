# Open different AWS Sessions in different firefox containers - Leapp Plugin
[**Leapp**](https://github.com/noovolari/leapp) is a Cross-Platform Cloud access App, built on top of [Electron](https://github.com/electron/electron).

[The App](https://github.com/noovolari/leapp) is designed to **manage and secure Cloud Access in multi-account environments,** and it is available for MacOS, Windows, and Linux.

# Requirements
This plugin requires [Open external links in a container](https://addons.mozilla.org/en-US/firefox/addon/open-url-in-container/) extension for Firefox.
This extension adds 'ext+container:' protocol support in Firefox, allowing to choose which container to use when opening an external url.

The 'ext+container' protocol has to be configured as managed by firefox on your OS.
### Windows
Run ```extcontainer.reg``` file, which sets the protocol handler on Windows
```
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\ext+container]
"URL Protocol"=""
[HKEY_CLASSES_ROOT\ext+container\shell]
[HKEY_CLASSES_ROOT\ext+container\shell\open]
[HKEY_CLASSES_ROOT\ext+container\shell\open\command] 
@="\"C:\\Program Files\\Mozilla Firefox\\firefox.exe\" \"%1\""
```

### Linux (Gnome)
```
xdg-mime default firefox.desktop x-scheme-handler/ext+container
```

### Mac OS X
TODO

# How to build this plugin For Leapp

### Install the project locally

```npm install```

You are ready to go.

#### Build plugin.js

Use `npm run build`. A complete project will be created inside the root folder. 

> Note: you can **test your plugin** before submission, by **copying** the output folder of `npm run build` inside `~/.Leapp/plugins/`.

