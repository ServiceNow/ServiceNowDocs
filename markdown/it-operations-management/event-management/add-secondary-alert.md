---
title: Add secondary alert manually to an existing alert group
description: Add any relevant alert discovered during the review of an automated alert group as a secondary alert to improve the group's completeness and utility for incident troubleshooting.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-08"
reading_time_minutes: 1
breadcrumb: [Manual alert grouping, Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Add secondary alert manually to an existing alert group

Add any relevant alert discovered during the review of an automated alert group as a secondary alert to improve the group's completeness and utility for incident troubleshooting.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The alert you select to add to a new group may already be part of another group. Adding it to the new group will automatically remove it from its current group, changing its group association. Alternatively, you can update the alert’s parent to move it to a different group. By specifying a new parent, the alert is transferred to the new parent’s group and removed from the previous one. This can be accomplished by updating the **Parent** field on the alert form or by modifying the **Parent** column in the Alerts list.

**Note:** When an alert is added to a group, feedback is logged as part of the process. Currently, the feedback option is available but does not trigger further actions after being logged.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Select the alert number to open the alert.

3.  In the **Parent** field, search for the alert you want to assign as the parent for the selected alert.

    ![Window from which you can choose a primary alert to add the current alert as a secondary alert.](../image/em-parent-alert.png)

4.  Select the parent alert number.

5.  Select **Update**.


## Result

The alert is added as a secondary alert to the selected parent alert.

**Parent Topic:**[Manual alert grouping](../concept/manual-alert-grouping.md)

