---
title: Show that an agent is busy with a non-work order event
description: Block time on agent calendars for events that aren’t related to work orders.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Show that an agent is busy with a non-work order event

Block time on agent calendars for events that aren’t related to work orders.

## Before you begin

Role required: wm\_dispatcher

## About this task

Dispatchers can use non-work order personal events to show an agent is busy. For example, if an agent is in training all day, you can use a personal event to show an agent is busy on the calendar in Dispatcher Workspace.

For information on editing or deleting personal events, see [Edit or delete an event](edit-delete-event.md).

**Note:** You can't create recurring personal events.

Route optimization doesn't change when personal events are scheduled.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  Select the ![Event management](../image/event-manage-coral.png) **Event Management** icon.

4.  On the form, fill in the fields.

<table id="table_q1k_wlg_lzb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

User

</td><td>

The user that the event applies to. You can add more than one user to the event.

</td></tr><tr><td>

Event title

</td><td>

The title of the event shown on the calendar in Dispatcher Workspace.

</td></tr><tr><td>

Type

</td><td>

The type of event you're creating.

</td></tr><tr><td>

Allow double booking with tasks

</td><td>

Allows the task to be scheduled at the same time as existing work order tasks.**Note:**

If you don’t allow double booking, and the event is at the same time that the agent has a scheduled work order task, or the travel time overlaps with a schedule work order task, then the task they’ve assigned is unassigned.

**Allow double booking with tasks** is only available if you have workforce optimization configured.

</td></tr><tr><td>

Show as

</td><td>

The status that shows for the agent or agents during the event.**Note:** **Show as** is only available if you don't have workforce optimization configured.

</td></tr><tr><td>

Start

</td><td>

The start time for the event

</td></tr><tr><td>

End

</td><td>

The end time for the event.

</td></tr><tr><td>

All day event

</td><td>

Option to indicate that the event lasts the entire day.

</td></tr><tr><td>

Location

</td><td>

The location that the event takes place in.**Note:** Locations on events are only available if you have workforce optimization configured. Locations for events are only available for events that have the **Type** set to Meeting or Training.

</td></tr><tr><td>

Time zone

</td><td>

The time zone is determined by the person that is added to the event. If there's more than one person added to the event, then the location of the first person added determines the time zone. If you update the location of the event, then the time zone of the location you entered is used.

</td></tr></tbody>
</table>5.  Select **Save**.


