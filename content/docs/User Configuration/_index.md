---
title: "User Configurations"
weight: 5
---

By default it is not recommended to edit any file of `.config/hypr/configs`. It's default configurations which gets overwritten by updates. Users can create multiple files at `.config/hypr/User`. Some choices can get in conflict, such as environment variables, layer rules or window rules of existing services, etc. Please be careful and our installation script do provides option to back up files

To edit monitor configuration, please edit `.config/hypr/monitor.lua`