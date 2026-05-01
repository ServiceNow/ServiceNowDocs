---
title: Remove CMDB tables or classes from impact calculation
description: Exclude unnecessary CMDB tables or classes from impact calculation to improve performance and focus on relevant data.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Remove CMDB tables or classes from impact calculation

Exclude unnecessary CMDB tables or classes from impact calculation to improve performance and focus on relevant data.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## Procedure

1.  Navigate to **All** and search for `em_impact_inclusion_class.list`.

    The Impact Inclusion Classes page opens, displaying a list of CMDB classes that are included in impact calculation.

    ![A list of CMDB classes that are included in impact calculation.](../image/em-impact-cal-cmdb-tables-list.png)

2.  Select the CMDB table that you want to remove.

3.  Select the Actions on selected rows menu and then select **Delete**.

4.  In the confirmation window, select **Delete**.

    The CMDB table is removed from the list.


