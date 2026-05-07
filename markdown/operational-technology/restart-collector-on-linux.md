---
title: Restart OT Discovery Collector on a Linux system
description: Perform manual restart of Collector when its configuration file has been refreshed, or if the OT Discovery Collectors is unstable. You can perform manual restart only on the Collectors installed in a Windows environment and for Linux-based agents that use systemd.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the OT Discovery Collector, OT Discovery Collector, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Restart OT Discovery Collector on a Linux system

Perform manual restart of Collector when its configuration file has been refreshed, or if the OT Discovery Collectors is unstable. You can perform manual restart only on the Collectors installed in a Windows environment and for Linux-based agents that use `systemd`.

## Before you begin

Role required: admin

## Procedure

1.  Use SSH to access the Linux host.

2.  Use `sudo` or `su` to run the following command with root permissions.

    ```
    systemctl restart SNDiscoveryCollectors
    ```


## Result

Discovery Scout restarts in the Linux environment.

