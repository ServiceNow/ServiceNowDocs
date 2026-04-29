---
title: Agent location
description: The Field Service Management application calculates your location from a set of geographical coordinates.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Execute from the agent map, Execute work order tasks, Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# Agent location

The Field Service Management application calculates your location from a set of geographical coordinates.

These coordinates are updated at a predefined interval based on geolocation data returned by your mobile device. Your position at the beginning of the day might be calculated from mobile device coordinates or from the location of the home office, whichever is more current. If you are starting the day completing a task that carried over from the previous day, the system uses the location of that task as your starting position. The system uses your precise location throughout the day to calculate accurate travel times, route your tasks automatically, and schedule fixed time windows.

**Note:** The actions such as start travel, start work, pause work, resume work, close complete, and close incomplete performed either from the desktop application or mobile application generate an entry in the geolocation history table with the following additional details:

-   Action description
-   Work order task number
-   Location timestamp

