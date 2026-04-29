---
title: Create an incident task
description: Create an incident task to communicate and request work from assignment groups other than the one initially assigned to the incident.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Create an incident task

Create an incident task to communicate and request work from assignment groups other than the one initially assigned to the incident.

## Before you begin

Role required: itil, sn\_incident\_write, or admin

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open the incident record.

3.  In the **Incident Tasks** related list, click **New**.

    If you don't see the **Incident Tasks** related list, you need to add it. For information on how to add a related list, see [Add a related list to a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&section=t_AddARelatedList&ft:locale=en-US).

    Alternatively, you can also right-click on the header form and on the context menu, and then select **Create Incident Task**.

4.  On the form, fill in the fields.

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

Incident with which the task is associated.

</td></tr><tr><td>

Configuration item

</td><td>

The affected CI.

</td></tr><tr><td>

State

</td><td>

The state is updated and tracks the incident task through several stages of resolution.**Note:** When an incident task is closed, you can no longer edit the field values in the incident task form.

</td></tr><tr><td>

Priority

</td><td>

Priority level of the incident task.

</td></tr><tr><td>

Assignment group

</td><td>

Group who works on the incident task. If you leave it blank, the incident is automatically assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User to whom the incident task is assigned.**Note:** If the **Assignment group** changes, the **Assigned to** field is cleared.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the incident task.

</td></tr><tr><td>

Description

</td><td>

Detailed explanation on the incident task.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notifications about this incident task when work notes are added. **Note:** You can the add me icon ![Add me icon](../image/add-me.png) to add yourself to the work notes list.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the incident task, or steps taken to resolve it, if applicable.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

When an incident task is closed, you can no longer edit the field values in the incident task form.

