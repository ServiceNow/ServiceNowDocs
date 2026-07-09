---
title: Restart Discovery Scout on a Windows system
description: Perform manual restart of an agent when the agent configuration file has been refreshed, or if the agent is unstable. You can perform manual restart only on agents installed in a Windows environment and for Linux-based agents that use systemd.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/restart-discovery-collector-on-windows.html
release: zurich
topic_type: task
last_updated: "2025-09-12"
reading_time_minutes: 1
breadcrumb: [Use the OT Discovery Collector, OT Discovery Collector, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Restart Discovery Scout on a Windows system

Perform manual restart of an agent when the agent configuration file has been refreshed, or if the agent is unstable. You can perform manual restart only on agents installed in a Windows environment and for Linux-based agents that use `systemd`.

## Before you begin

Role required: admin

## Procedure

1.  On a windows system, navigate to the host where Discovery Scout is running.

2.  Open the Services dialog in Windows.

3.  Select SNDiscoveryScout.

4.  Select **Restart the service**.


## Result

Discovery Scout restarts in the Windows environment.

