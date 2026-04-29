---
title: Configure territory fields to appear in Territory Planning console
description: Customize the information displayed for territories in the Territory Planning console by configuring the contextual side panel fields. This enhances planning efficiency with personalized data, helping to take informed decisions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Territory Planning Console, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure territory fields to appear in Territory Planning console

Customize the information displayed for territories in the Territory Planning console by configuring the contextual side panel fields. This enhances planning efficiency with personalized data, helping to take informed decisions.

## Before you begin

Role required: wm\_admin

## About this task

You can configure both predefined and calculated fields for territories.

## Procedure

1.  Navigate to **All** &gt; **app\_cmn\_field\_set.list.do**.

    The list of predefined application field sets appear.

2.  To configure pre-defined fields, select **FSM Territory Form Fields**.

    1.  Review the list of available fields such as parent assignment, territory, active, rank, color, and geography.

    2.  To display a field in the Territory Planning console, set the **Default show** field to **true**.

    3.  Organize the order in which the fields appear in the console by entering values in the **Order** column.

3.  To configure calculated fields, select **FSM Territory Form Calculated Fields**.

    1.  Navigate to the calculated fields section, which includes the number of children, qualification groups, dispatched groups, assignment groups, and KPI range.

    2.  To display a field in the Territory Planning console, set the **Default show** field to **true**.

    3.  Organize the order in which the fields appear in the console by entering values in the **Order** column.


## Result

The configured fields appear in the Territory Planning console. To view the changes, log in as a territory planner and navigate to the console. For more information, see [View territory information in contextual side panel](view-territory-details-in-csp.md).

