---
title: "Aurora's CLI"
weight: 4
---
Aurora's cli is automatically insatlled when you use the installtion script or if you followed manual installation script correctly. You can do many things with Aurora's cli. 

## Some useful commands
`aurora --help` to view all available commands and flags.

```bash
aurora apply-theme "THEME_NAME"
```
This command can apply your instructed theme

```bash 
aurora list-themes
```
This will show all available themes

## All sub-commands
## Available Commands

| Command                                      | Description                                       |
| -------------------------------------------- | ------------------------------------------------- |
| `aurora version`                             | Show Aurora and Aurora CLI versions               |
| `aurora apply-theme <THEME_NAME>`            | Apply a theme globally                            |
| `aurora list-themes`                         | List all installed themes                         |
| `aurora information`                         | Display information about Aurora                  |
| `aurora theme-info`                          | Show information about the currently active theme |
| `aurora download-theme <GIT_REPOSITORY_URL>` | Download and install a theme                      |
| `aurora update-themes`                       | Update all installed external themes              |
| `aurora refresh`                             | Refresh Aurora                                    |
| `aurora reload`                              | Reload Aurora's configuration                     |
| `aurora runscript <BINARY_NAME>`             | Execute a script or binary available in `PATH`    |
| `aurora ghostty blur <on/off>`               | Enable or disable Ghostty blur                    |
| `aurora settings screensaver <on/off>`       | Enable or disable the Aurora screensaver          |
| `aurora settings welcome-app <true/false>`   | Enable or disable Welcome App autostart           |

## Settings Sub Commands

### Screensaver

| Command                           | Action                         |
| --------------------------------- | ------------------------------ |
| `aurora settings screensaver on`  | Enable the Aurora screensaver  |
| `aurora settings screensaver off` | Disable the Aurora screensaver |

### Welcome App

| Command                             | Action                        |
| ----------------------------------- | ----------------------------- |
| `aurora settings welcome-app true`  | Enable Welcome App autostart  |
| `aurora settings welcome-app false` | Disable Welcome App autostart |

## Ghostty Sub Commands

### Blur

| Command                   | Action               |
| ------------------------- | -------------------- |
| `aurora ghostty blur on`  | Enable Ghostty blur  |
| `aurora ghostty blur off` | Disable Ghostty blur |
