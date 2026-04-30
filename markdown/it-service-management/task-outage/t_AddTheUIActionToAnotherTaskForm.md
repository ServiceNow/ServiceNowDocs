---
title: Add the Outage UI action to another task form
description: By default, the Create Outage UI action is available on the incident and problem forms, and can be added to other task forms. For new instances from Jakarta only, this feature is also available on the change request form.
locale: en-US
release: zurich
product: Task Outage
classification: task-outage
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Task Outage, IT Service Management]
---

# Add the Outage UI action to another task form

By default, the **Create Outage** UI action is available on the incident and problem forms, and can be added to other task forms. For new instances from Jakarta only, this feature is also available on the change request form.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **UI Actions**.

2.  Select the UI Action **Create Outage** on the Task \[task\] table.

    By default, the condition is:

    `current.getRecordClassName() == 'incident' || current.getRecordClassName() == 'problem'`

3.  Modify the **Conditions** field as described in the following examples.

<table id="choicetable_ayx_s1b_h5"><tbody><tr><td id="d160037e97">

**To add this UI action to the Ticket \[ticket\] table**

</td><td>

`current.getRecordClassName() == 'incident' || current.getRecordClassName() == 'problem' || current.getRecordClassName() == 'ticket'`

</td></tr><tr><td id="d160037e109">

**To use the UI action on only the Problem \[problem\] table**

</td><td>

`current.getRecordClassName() == 'problem'`

</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[Task Outage](../concept/task-outage.md)

