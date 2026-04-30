---
title: Create alert group manually
description: Manually create an alert group to organize and manage related alerts when not using scheduled jobs. This provides flexibility to group alerts on-demand for effective resolution.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manual alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create alert group manually

Manually create an alert group to organize and manage related alerts when not using scheduled jobs. This provides flexibility to group alerts on-demand for effective resolution.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Select the alert number to open the alert.

    The alert will be used to create an alert group, designated as the primary alert, to which you can add secondary alerts.

    **Note:** A closed alert cannot be assigned as a parent alert.

3.  Scroll down and in the **Secondary Alerts** tab, select **Add To Group**.

    ![Option to add secondary alerts to the group.](../image/em-secondary-alert-1.png)

4.  Select the check boxes for all alerts you want to add to the group as secondary alerts and select **Add Selected**.

    ![Select the alerts that you want to add as secondary alerts to the group.](../image/em-secondary-alert-2.png)

5.  In the **Secondary Alerts** tab, view the alerts that have been added as secondary.

    ![Secondary alerts are added to the group.](../image/em-secondary-alert-3.png)


**Parent Topic:**[Manual alert grouping](../concept/manual-alert-grouping.md)

