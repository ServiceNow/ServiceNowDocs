---
title: Remove application services from impact calculation
description: Exclude specific application services from impact calculation to reduce noise and focus on critical components.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Remove application services from impact calculation

Exclude specific application services from impact calculation to reduce noise and focus on critical components.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

Removing or deleting a record from the list won’t necessarily exclude the application service from impact calculation if the CMDB class still exists in em\_impact\_inclusion\_class.list. However, even if the class exists in em\_impact\_inclusion\_class.list, the application service will not be considered for impact calculation if its status is set to **Calculate Impact** = **false** in em\_impact\_filter\_service.list.

For the application service that you want to exclude from the impact calculation, add the application service with **Calculate Impact** = **false**, or change the **Calculate Impact** = **false**, if this record already exist. The procedure shows how to configure this setting.

## Procedure

1.  Navigate to **All** and search for `em_impact_filter_service.list`.

    The Impact Filter Services page opens.

    ![A list of application services that are included in impact calculation.](../image/em-impact-cal-app-services-list.png)

2.  For the application service that you want to exclude from the impact calculation, change the **Calculate impact** status of the application service to **false**.

    This keeps the application service record in the list but excludes it from impact calculation.


