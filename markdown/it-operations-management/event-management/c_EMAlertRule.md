---
title: Alert lifecycle configuration
description: Event Management provides various modules, templates, and properties for configuring alerts and the actions that execute for these alerts.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert lifecycle configuration

Event Management provides various modules, templates, and properties for configuring alerts and the actions that execute for these alerts.

-   **[Configure the alert active interval](../task/t_EMSetTheAlertActiveInterval.md)**  
The active interval property \(**evt\_mgmt.active\_interval**\) determines how Event Management handles a new event that is similar to events that appear on an existing closed alert. Based on the active interval, event, and existing closed alert information, the alert is reopened and the event information is added to the existing alert or a new alert is created.
-   **[Configure alert flapping](../task/t_EMConfigAlertStateFlapDetect.md)**  
Set flapping properties to determine when an alert enters and exits the flapping state. Flapping can indicate configuration problems \(that is, thresholds set too low\), troublesome services, or real network problems.

**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

