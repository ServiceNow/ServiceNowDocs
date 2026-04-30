---
title: Configure event body fields
description: Administrators can add fields to event bodies so Dispatchers have more information about events when they’re viewing the calendar in Dispatcher Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Configure event body fields

Administrators can add fields to event bodies so Dispatchers have more information about events when they’re viewing the calendar in Dispatcher Workspace.

## About this task

Administrators can show up to five fields on the event body in Dispatcher Workspace. Dispatchers can choose what fields show on event bodies in the Dispatcher Settings under the Events tab. For more information on the Events tab, see [Enable Dispatcher Workspace settings](dispatcher-wrkspc-settings.md).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Calendar Work Order Task Fields**.

2.  Select **New**.

3.  On the form sill in the fields.

<table id="table_kbg_kvf_5cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Name

</td><td>

The field that shows on event bodies in Dispatcher Workspace.

</td></tr><tr><td>

Name

</td><td>

The name of the field that shows in Dispatcher Workspace.

</td></tr><tr><td>

Always show

</td><td>

Forces the field to show for all dispatchers. Dispatchers can’t turn off the field when Always show is set to True. If this field is set to false, then Dispatchers can turn the event field on or off.

</td></tr><tr><td>

Default show

</td><td>

If the field shows in event bodies

</td></tr><tr><td>

Order

</td><td>

The order that the field shows on an event body in relation to the other fields. The lower the value, the higher the field shows on an event body. **Note:** There can be a maximum of five fields on event bodies. If there are more than five fields, only the five with the lowest order numbers show.

</td></tr></tbody>
</table>4.  Select **Submit**.


