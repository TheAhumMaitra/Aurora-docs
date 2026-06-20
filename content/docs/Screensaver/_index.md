---
title: "Screensaver"
weight: 4
---

Aurora provides very cool screensaver support. It uses a TUI called `termflix` to provide 42 live effects

## Preview
{{< video
  src="/videos/screensaver.mp4"  width="800"
>}}

## How to disable
There are some ways to disable **screensaver**

### 1. Using Aurora's cli
Run the following command to disable screensaver :-

```text
aurora settings screensaver off
```

### 2. By editing Aurora's configuration.
You can also disable the screensaver by modifying the Aurora configuration file manually.

To disable the screensaver:
```toml 
[settings] screensaver = false

```
After saving the file, you need to reload by running :-

```text
aurora reload
```

### 3. Manually Edit `hypridle` configuration
Use your preferred code editor to edit `hypridle` configuration which is located at `.config/hypr/hypridle.conf`

#### Comment this following part
```text
# Start Aurora screensaver
listener {
    timeout = 150 
    on-timeout = aurora-launch-screensaver
}
```