---
title: Configure an event load order in Workforce Optimization for ITSM
description: Add a system property to display your preferred event categories first on the calendar.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure event categories for the ITSM Manager Workspace, Setting up, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Configure an event load order in Workforce Optimization for ITSM

Add a system property to display your preferred event categories first on the calendar.

## Before you begin

Set the map application scope to **Shift Planning**. For information on how to set the scope, see Set map application scope.

Role required: admin

## Procedure

1.  In the application navigator, enter `sys_properties.list`.

2.  Click **New**.

3.  Enter the following field values.

<table id="table_yfh_h3p_f4b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Suffix

</td><td>

`sn_shift_planning.event_load_order`

</td></tr><tr><td>

Application scope

</td><td>

Shift Planning

</td></tr><tr><td>

Type

</td><td>

String

</td></tr><tr><td>

Value

</td><td>

```
{
   "fastLoad":[
      "07e433f449a11010f877de942e7c1d18"
 ]
}
```

 where fastLoad is the array of sys\_ids for event categories that you would like to load first. The remaining custom event categories will be loaded after all event categories with fastLoad categories are loaded and updated on the calendar.

</td></tr><tr><td>

Read roles

</td><td>

sn\_shift\_planning.agent

</td></tr><tr><td>

Write roles

</td><td>

sn\_shift\_planning.admin

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configure event categories for the ITSM Manager Workspace](categorize-events-configurable-wfo-itsm.md)

