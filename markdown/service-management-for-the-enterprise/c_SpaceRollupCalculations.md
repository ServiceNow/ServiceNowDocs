---
title: Space roll up calculations
description: The Facilities Service Management application can roll up occupancy, area, and usage information from lower to higher levels in the space hierarchy. Roll ups apply to spaces that are designated as 'occupiable'. The occupancy values from that space are rolled up to the level above them.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customer-created maps, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Space roll up calculations

The Facilities Service Management application can roll up occupancy, area, and usage information from lower to higher levels in the space hierarchy. Roll ups apply to spaces that are designated as 'occupiable'. The occupancy values from that space are rolled up to the level above them.

An occupiable space is designated by selecting the check box on the facility space record. The **Current occupancy** and **Percent occupied** fields rely on the **Occupiable** option. Roll up calculations are modified in a script include.

![image is a screen shot showing the Occupiable check box and dependant fields](../image/Occupiable.png "Occupiable selected and dependent fields")

The values that roll up are:

-   occupancy
-   max occupancy
-   assignable area

The percent occupied calculation takes place based on the current and max occupancy values.

**Parent Topic:**[Customer-created maps](../reference/r_Manually-builtMaps.md)

