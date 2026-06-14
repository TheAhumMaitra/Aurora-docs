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
To disable Aurora's screensaver, please follow these steps :-

### Edit `hypridle` configuration
Use your preferred code editor to edit `hypridle` configuration which is located at `.config/hypr/hypridle.conf`

#### Comment this following part
```
# Start Aurora screensaver
listener {
    timeout = 150 
    on-timeout = aurora-launch-screensaver
}
```