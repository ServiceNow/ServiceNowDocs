---
title: Restart OT Discovery Collector on a Windows system
description: Perform manual restart of the OT Discovery Collectors when its configuration file has been refreshed, or if it is unstable. You can perform manual restart only on Collectors installed in a Windows environment and for Linux-based agents that use systemd.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the OT Discovery Collector, Operational Technology \(OT\) Discovery Collector, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Restart OT Discovery Collector on a Windows system

Perform manual restart of the OT Discovery Collectors when its configuration file has been refreshed, or if it is unstable. You can perform manual restart only on Collectors installed in a Windows environment and for Linux-based agents that use `systemd`.

## Before you begin

Role required: admin

## Procedure

1.  On a windows system, navigate to the host where Discovery OT Collectors is running.

2.  Open the Services dialog in Windows.

3.  Select SNDiscoveryCollectors.

4.  Select **Restart the service**.


## Result

Discovery OT Collectors restart in the Windows environment.

