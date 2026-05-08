---
title: Configure HR Service Delivery playbook card
description: Use Playbook Card Configuration to view and manage what appears for each card in an activity set.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setting up HR Service Delivery Playbook, HR Service Delivery Playbook, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Configure HR Service Delivery playbook card

Use Playbook Card Configuration to view and manage what appears for each card in an activity set.

## Before you begin

Role required: sn\_hr\_ws.admin

Each activity attempts to show a record \(HR task, HR case, request, and so on\) and goes through the card configuration and attempts to match to the lowest ordered record in the table. For example, the 'Verify Work Authorization' is a 'mark when complete' card that the base system provides.

The properties from the card configuration record are filled in from the record \(HR task, HR case, request, and so on\).

**Note:** For Classic HR Service Delivery Agent Workspace and Agent Workspace for HR Case Management, there are two separate default card configurations and activity overrides. The property **sn\_hr\_agent\_ws.use\_uib\_playbook\_card\_config** \(default value = false\) decides which card configuration is to be used for HR Service Delivery Playbook when you have each Agent Workspace installed. By default, the Classic card configuration will be selected in the card configuration.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Playbook Card Configuration**.

2.  Fill in the fields on the form.

<table id="table_o3b_flt_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name that identifies the HR Playbook Card Configuration.

</td></tr><tr><td>

Table

</td><td>

The record type of the configuration.Determines what card appears for each activity within an activity set \(lane\). Also determines what properties the card uses.

</td></tr><tr><td>

Condition

</td><td>

The conditions that determine if the type values render to an HR Playbook card.**Note:** When defining conditions like case sensitivity or null values, see APIGlideFilter - Scoped, Global.

</td></tr><tr><td>

Activity type

</td><td>

The activity type from a lifecycle event activity. Activity types can be approvals, employee activities, fulfiller activities, notifications, and more. **Note:** For more information, see [Configure the supporting components for a lifecycle event](../concept/configure-supporting-components-for-lifecycle-event.md).

</td></tr><tr><td>

Active

</td><td>

Indicates if the record is active and available for use.

</td></tr><tr><td>

Order

</td><td>

The order in which the activity attempts to match this record. The lowest values are evaluated first.

</td></tr></tbody>
</table>    The Type Values section determines what appears on each card.

<table id="table_e3g_pnt_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Associated table

</td><td>

Not applicable at this time.

</td></tr><tr><td>

Footer

</td><td>

Information you want to appear in the footer of an HR Playbook card.Enter text or click the pill picker icon ![Pill picker icon](../image/playbook-hr-pill-picker-icon.png) to display references you can select from to automate the placement of information.

</td></tr><tr><td>

Associated record

</td><td>

Not applicable at this time.

</td></tr><tr><td>

Icon

</td><td>

Displays an icon that appears in the upper, left-side of the card.Click the Lookup using list icon ![Lookup using list icon](../image/magnifying-glass.png) to select the icon you want to appear.

</td></tr><tr><td>

Description

</td><td>

Select the pill picker icon ![Pill picker icon](../image/playbook-hr-pill-picker-icon.png) to display a description on the card. **Note:** This is not a free-form field, you must select from the available

</td></tr><tr><td>

Attachments read only

</td><td>

Check to indicate existing attachments can only be read. **Note:** This is a read only field and not for adding attachments to the activity. See the **Attachment source** field.

</td></tr><tr><td>

Title

</td><td>

The title of the card. You can enter free-form text or select from the list after clicking the pill picker icon ![Pill picker icon](../image/playbook-hr-pill-picker-icon.png).

</td></tr><tr><td>

Form fields

</td><td>

Displays a vertical column of fields that render below the row of record fields.**Note:** The fields are editable when at least one button on the card says **Form fields required**.

 You can enter comma separated text or select fields by clicking the pill picker icon ![Pill picker icon](../image/playbook-hr-pill-picker-icon.png).

 The fields you select appear as a column on the left-side of the card.

</td></tr><tr><td>

Show SLA

</td><td>

Check to indicate you want the SLA icon to appear at the top, right-side of the card.The icon shows the state of the SLA.

</td></tr><tr><td>

Tagline

</td><td>

Enter or select information that appears at the top of the card above the title.

</td></tr><tr><td>

Attachment source

</td><td>

Use to allow uploading of attachments. Selecting associated\_record allows the user to upload an attachment from the card.

</td></tr><tr><td>

Record fields

</td><td>

Fields you want to appear across the upper section of the card.Enter comma separated list of fields you want to appear on the card or click the xx icon to select references.

</td></tr><tr><td>

Show Checklist

</td><td>

Check to display the checklist from the activity.Users can check off tasks the same way they do on the case form.

</td></tr><tr><td>

Assigned to

</td><td>

Identifies the **Assigned to** agent.You can enter free-form text or select from the references after clicking the pill picker icon ![Pill picker icon](../image/playbook-hr-pill-picker-icon.png).

 The name appears next to the title.

</td></tr><tr><td>

Form View

</td><td>

Works with the **Form fields** and allows you to define an entire section you want to appear on the card.

</td></tr></tbody>
</table>3.  Click **Submit** or **Update**.


