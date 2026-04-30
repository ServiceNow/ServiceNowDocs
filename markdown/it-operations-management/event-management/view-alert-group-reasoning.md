---
title: Configure work notes to capture alert grouping justifications
description: As alerts are added to a group, a message is recorded in the alert’s Work notes field to explain why the alert was included in the group. Define alert types for creating these worknotes related to alert group reasoning.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure work notes to capture alert grouping justifications

As alerts are added to a group, a message is recorded in the alert’s Work notes field to explain why the alert was included in the group. Define alert types for creating these worknotes related to alert group reasoning.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the property **evt\_mgmt.alert\_groups\_reasoning.enable\_worknotes**.

3.  Open the property.

    ![Property page where you can define alert types for creating worknotes related to alert group reasoning.](../image/em_work_notes_alert_grp.png)

4.  In the **Choices** field, define alert types for creating worknotes related to alert group reasoning.

    |Value|Description|
    |-----|-----------|
    |All Alerts|Work note information is generated for every alert.|
    |Primary Alerts|Work note information is generated only for primary alerts.|
    |Secondary Alerts|Work note information is generated only for secondary alerts.|
    |None|No work note information is generated.|

5.  Select **Update**.


**Related topics**  


[Alert grouping types](../concept/Alert-Groups.md)

