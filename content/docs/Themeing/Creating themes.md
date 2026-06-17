---
title: "Creating Themess"
weight: 2
---

Aurora provides developers unique features to customize their theme. In your theme folder, create essential services folders - `hypr`, `rofi`, `waybar`, `wlogout`, `rofi`, etc and a default wallpaper (which should be named `default.png`). You can look our official 4 themes folders for understanding theming structure. 

## Supported Applications
**It supports various default applications**
1. `waybar`
2. `hyprland`
3. `Visual Studio Code`
4. `btop`
5. `rofi`
6. `Neovim (With Lazyvim)`
7. `wlogout`
8. `All Aurora's GUI`
9. `GTK`
10. `Zed`

> [!IMPORTANT]
> If your theme requires any external GTK themes, packages you need to create installation script to install them. Also please write instructions to run the installation script on `README.md`

### Example structure of a theme 

```yml
Aurora Default 
      backgrounds
         wallpaper1.jpg
         wallpaper2.png
         wallpaper3.png
         main.png #If you want users to switch to default background also
      hypr 
         colors.lua
      rofi 
         colors.rasi
      waybar
         colors.css
      wlogout
         colors.css
      nvim/lua/plugins
         colorscheme.lua
      zed/themes
         theme.json
      btop/themes
         current.theme
      custom.css #the colorscheme file for all Aurora GUIS
      default.png #Default Wallpaper
      config.toml
```

## Configuration of the theme 
You need to create a `toml` configuration file called `config.toml` in the theme's root directory. There you can provide essential details!

### Supported options for configuration file of theme
| Section      | Key              | Type          | Required | Description                                          | Example                                                    |
| ------------ | ---------------- | ------------- | -------- | ---------------------------------------------------- | ---------------------------------------------------------- |
| Root         | `name`           | String        | Yes      | Human-readable name of the theme/profile.            | `"Aurora Default"`                                         |
| Root         | `version`        | String        | Yes      | Configuration version.                               | `"0.1.0"`                                                  |
| Root         | `authors`        | Array`<String>` | No       | List of authors and maintainers.                     | `["Ahum Maitra (@TheAhumMaitra) example@gmail.com"]` |
| Root         | `repo_url`        | String | No       | Git repository url                   | `https://github.com/TheAhumMaitra/Aurora` |
| Root         | `wallpaper_sources`        | Array`<String>` | No       | All wallpaper sources URL(s) | `[https://github.com/TheAhumMaitra/Wallpapers]` |
| Root         | `license`        | String        | No       | SPDX License identifier for the configuration.            | `"GPL-3.0-or-later"`                                       |
| `[settings]` | `script`         | String        | No      | A script to execute with custom interpreter | `"default.lua"`                                            |
| `[settings]` | `interpreter`    | String        | No      | Interpreter used to run the script. (must be installed)                  | `"lua"`                                                    |
| `[gtk]`      | `theme_name`     | String        | Yes       | GTK theme name to apply.                             | `"Yaru-dark"`                                              |
| `[gtk]`      | `icon_theme`     | String        | Yes       | GTK icon theme name to apply.                        | `"Yaru-grey"`                                              |
| `[vscode]`   | `publisher`      | String        | Yes       | VS Code extension publisher identifier.              | `"Aliqyan-21"`                                             |
| `[vscode]`   | `extension_name` | String        | Yes       | VS Code extension name.                              | `"darkvoid"`                                               |
| `[vscode]`   | `theme_name`     | String        | Yes       | Theme name within the VS Code extension.             | `"darkvoid"`|
| `[zed]`   | `theme_name`     | String        | Yes       | The theme you want tto set by default             | `"darkvoid"` |

> [!TIP]
> You can create a `install.sh` script to install required packages (such as interpreters, GTK themes, etc)

> [!TIP]
> You can import multiple external scripts on the main script

**You can look an official Aurora's theme to understand - [`Aurora theme`](https://github.com/TheAhumMaitra/Aurora/tree/master/dotfiles/.config/themes/Dracula)**


## Terminal emulators
In Aurora, Ghostty is a backup terminal emulator, while Kitty is the default. At the moment, Kitty doesn't change its color scheme according to the current theme; instead, it has a fixed blurred appearance. In contrast, Ghostty is intended to be more closely integrated with Aurora's theming system, mirroring your chosen theme automatically and giving you a more vibrant, richer look.