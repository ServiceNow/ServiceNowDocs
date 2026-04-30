---
title: Create key values to cluster alerts
description: Create key values to cluster CIs, using the Key Values table. Key values create an additional way to determine commonality between alerts and to combine them into groups. For example, you may want to group alerts on CIs that share the same supplier or location.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Tag cluster alert grouping, Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Create key values to cluster alerts

Create key values to cluster CIs, using the Key Values table. Key values create an additional way to determine commonality between alerts and to combine them into groups. For example, you may want to group alerts on CIs that share the same supplier or location.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  In the navigation window, enter `cmdb_key_value.list`.

2.  In the **Key Values** table, select **New**.

3.  Configure key values for CIs in your system.

4.  Click **Submit**.

    The results appear in the Key Values table.

    ![Key Values table](../image/key-values-table.png "Key Values table")


## Result

Alerts for CIs with the same key value are grouped together to form an alert group.

