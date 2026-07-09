---
title: Restart Discovery Scout on a Linux system
description: Perform manual restart of an agent when the agent configuration file has been refreshed, or if the agent is unstable. You can perform manual restart only on agents installed in a Windows environment and for Linux-based agents that use systemd.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/restart-collector-on-linux.html
release: zurich
topic_type: task
last_updated: "2025-09-23"
reading_time_minutes: 1
breadcrumb: [Use the OT Discovery Collector, OT Discovery Collector, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Restart Discovery Scout on a Linux system

Perform manual restart of an agent when the agent configuration file has been refreshed, or if the agent is unstable. You can perform manual restart only on agents installed in a Windows environment and for Linux-based agents that use `systemd`.

## Before you begin

Role required: user

## Procedure

1.  SSH to the Linux host.

2.  Use `sudo` or `su` to run the following command with root permissions.

    ```
    systemctl restart SNDiscoveryScout
    ```


## Result

Discovery Scout restarts in the Linux environment.

