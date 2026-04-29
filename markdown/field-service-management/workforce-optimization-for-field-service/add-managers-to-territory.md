---
title: Add managers to a territory
description: Add managers and provide access to a territory to manage a territory or manage resources of an assigned territory.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure resources, Territory Planning, Set up workforce, Configure, Field Service Management]
---

# Add managers to a territory

Add managers and provide access to a territory to manage a territory or manage resources of an assigned territory.

## Before you begin

Role required: sn\_fsm\_tp.territory\_planner

## About this task

You can add different types of managers to a territory:

-   Primary manager: The primary manager is the permanent managers for a dedicated territory.
-   Secondary manager: The secondary manager can improve and manage territory when primary manager is not available.
-   Territory manager: The territory manager can access and manage all territories.
-   Resource manager: The resource manager has restricted access only to manage resources and create child territories in the assigned territory.

To understand the difference between the manager types and their access rights, see [Managing territories and agents from Territory Planning console](../concept/using-territory-planning-console.md) and [Field Service Territory Planning components](../reference/territory-planning-components-fsm.md#).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territories**.

2.  From the territories list, open the territory where you want to assign managers.

3.  In the related list for the territory managers, select **New**.

4.  On the form, fill in the fields.

<table id="table_olb_tzs_stb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Territory

</td><td>

Name of the territory.

</td></tr><tr><td>

Membership type

</td><td>

Manager type for the group, either territory manager or resource manager, that sets the access and priority for assignments in a territory.**Note:** You can add a resource manager for only a specified duration.

</td></tr><tr><td>

Manager

</td><td>

Name of the manager.

</td></tr><tr><td>

Primary

</td><td>

Option to indicate whether the manager is primarily dedicated for all activities in the territory.**Note:** Do not select the option if you want to add a secondary manager for a specified duration.

</td></tr><tr><td>

From

</td><td>

Manage territory from the selected date.

</td></tr><tr><td>

To

</td><td>

Manage territory until the selected date.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The manager is added to the territory and can access the Territory Planning console to manage their assigned territory and related child territories.


## Result

The manager appears in the **Territory Managers** related list when you open the territory.

