---
title: Create tasks to fulfill an OT incident
description: Create a set of incident tasks to fulfill an Operational Technology \(OT\) incident. Incident tasks help you to split up and categorize the work that is needed to resolve an incident.
locale: en-US
release: australia
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Incident Management, Operational Technology]
---

# Create tasks to fulfill an OT incident

Create a set of incident tasks to fulfill an Operational Technology \(OT\) incident. Incident tasks help you to split up and categorize the work that is needed to resolve an incident.

## Before you begin

Role required: sn\_ot\_incident\_write

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Open the Industrial Workspace list view.

3.  Under the OT Incidents list module, select on of the available lists.

4.  Select the OT incident record that you want to create incident tasks for.

5.  In the OT incident record, select the **Incident Tasks** tab.

6.  Select **New**.

7.  On the Create New Operational Technology Incident Task form, fill in the following fields.

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

Group who works on the incident task. If you leave this field empty, the incident is automatically assigned.**Note:** If needed, you can assign OT incident tasks to IT assignment groups.

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

Users who receive notifications about this incident task when work notes are added. **Note:** You can also add yourself to the work notes list.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the incident task, or the steps that need to be taken to resolve it, if applicable.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

You can view incident tasks in the Industrial Workspace list view in the following places.

-   Incident tasks assigned to you: **OT Tasks** &gt; **Assigned to Me**
-   Incident tasks assigned to your group: **OT Tasks** &gt; **Assigned to My Groups**
-   Unassigned incident tasks: **OT Tasks** &gt; **Unassigned**

**Parent Topic:**[Using Operational Technology Incident Management](../concept/using-operational-technology-incident-mgt.md)

