---
title: "FAQ"
weight: 6
---

## How to change my keyboard layout

Do you need to alter the layout of your keyboard? Don't worry, just be open:

```text
~/.config/hypr/configs/input.lua 
```

You'll find something like this in the file:
```lua 
kb_layout = "gb,us" 
```

Your default keyboard layout is the first one on the list. Aurora will begin with the **GB (United Kingdom)** layout in the aforementioned scenario.

Additionally, you can add more layouts by using commas to separate them. **For instance:**
```lua 
kb_layout = "us,de" 
```

This will have **German** as a backup layout and **US English** as the primary layout.

Once several layouts are set up, you may use **SUPER + SPACE** to flip between them whenever you want.

Aurora is preconfigured with the **GB keyboard layout** by default.

