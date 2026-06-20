---
title: "Aurora Configuration"
weight: 7
---------

Aurora may be modified via a configuration file, which gives you control over many settings and appearance-related variables.

By default, Aurora does not generate a configuration file automatically. To utilize custom settings, create a file named `aurora.toml` in your `~/.config` directory.

```text
~/.config/aurora.toml
```

> [!IMPORTANT]
> Aurora's configuration system is still actively developed, therefore only a limited amount of settings are now accessible.

## Available Sections

### `[settings]`

General Aurora settings.

| Key           | Type      | Description                                                                      | Example               |
| ------------- | --------- | -------------------------------------------------------------------------------- | --------------------- |
| `screensaver` | `boolean` | Enables or disables the Aurora screensaver.                                      | `screensaver = false` |
| `welcome_app` | `boolean` | Enables or disables the Aurora Welcome App, which launches when Hyprland starts. | `welcome_app = true`  |

#### Example

```toml
[settings]
screensaver = false
welcome_app = true
```

---

### `[ghostty]`

Settings related to Ghostty's appearance and behavior.

| Key    | Type      | Description                                                                                                                                                                                                              | Example       |
| ------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- |
| `blur` | `boolean` | Enables Ghostty background blur. When enabled, Aurora disables the default theme-based color palette and uses the blur configuration instead. When disabled, Ghostty continues using Aurora's theme-based color palette. | `blur = true` |

#### Example

```toml
[ghostty]
blur = true
```

---

## Example of Aurora's Configuration

```toml
[ghostty]
blur = true

[settings]
screensaver = false
welcome_app = true
```

## Reloading Aurora
After saving the configuration after every edit, you may run this command to reload and parse Aurora's configuration :-

```text
aurora reload
```