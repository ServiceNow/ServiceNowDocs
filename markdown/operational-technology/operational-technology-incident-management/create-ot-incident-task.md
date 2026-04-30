---
title: Create tasks to fulfill an incident
description: Create a set of incident tasks to fulfill an Operational Technology \(OT\) incident. Incident tasks help you to split up and categorize the work that is needed to resolve an incident.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Incident Management, Operational Technology]
---

# Create tasks to fulfill an incident

Create a set of incident tasks to fulfill an Operational Technology \(OT\) incident. Incident tasks help you to split up and categorize the work that is needed to resolve an incident.

## Before you begin

Role required: sn\_ot\_incident\_write

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

2.  Open the OT incident record that you want to create a task for.

3.  In the Incident Tasks related list, select **New**.![Create new incident task new button.](../image/incident-task-new-button.png)

    If you don’t see the Incident Tasks related list, you must add it.

4.  On the form, fill in the fields.![Operatioonal Technology incident task form.](../image/ot-incident-task-form-new.png)

<table id="table_jdm_2hn_23b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-generated incident task number.

</td></tr><tr><td>

Incident

</td><td>

Incident with which the task is related.

</td></tr><tr><td>

Site

</td><td>

Affected incident site.**Note:** This field is read-only and is automatically filled in with the related incident site, if applicable.

</td></tr><tr><td>

Equipment Model Entity

</td><td>

Affected equipment model entity.**Note:** This field is read-only and is automatically filled in with the related equipment model entity, if applicable.

</td></tr><tr><td>

OT device

</td><td>

Affected OT device.**Note:** This field is read-only and is automatically filled in with the related OT device, if applicable.

</td></tr><tr><td>

State

</td><td>

State for tracking an incident task through several stages of the incident's resolution.

</td></tr><tr><td>

Priority

</td><td>

Priority of the incident task.

</td></tr><tr><td>

Assignment group

</td><td>

Group who works on the incident task. If you leave this field empty, the incident is automatically assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User to whom the incident task is assigned to work on.**Note:** If the **Assignment group** changes, the **Assigned to** field is cleared.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the incident task.

</td></tr><tr><td>

Description

</td><td>

Detailed explanation on the incident task.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notifications about this incident task when work notes are added. **Note:** You can select the add me icon ![Add me icon.](../../incident-management/image/add-me.png) to add yourself to the work notes list.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the incident task, or the steps that need to be taken to resolve it, if applicable.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

Now, you can view and edit the incident task in the related OT incident record in the **Incident Tasks** tab on either the ServiceNow AI Platform or in the Industrial Workspace.

You can also view incident tasks in the Industrial Workspace list view in the following places.

-   Incident tasks assigned to you: **OT Tasks** &gt; **Assigned to Me**
-   Incident tasks assigned to your group: **OT Tasks** &gt; **Assigned to My Groups**
-   Unassigned incident tasks: **OT Tasks** &gt; **Unassigned**

**Parent Topic:**[Using Operational Technology Incident Management](../concept/using-operational-technology-incident-mgt.md)

