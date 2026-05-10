---
title: User Form activity
description: Use this activity to surface a record to the end user. This activity requires you to select a table and record, and the desired form view that should be surfaced to the end user in your playbook. The end user can then interact with this record accordingly. Display a form during runtime to collect input values for your playbook.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# User Form activity

Use this activity to surface a record to the end user. This activity requires you to select a table and record, and the desired form view that should be surfaced to the end user in your playbook. The end user can then interact with this record accordingly. Display a form during runtime to collect input values for your playbook.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dot-walking-examples.md).

<table id="table_ajt_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

String

</td><td>

Title to display as activity and playbook card.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Information to display about activity usage or outcome.

</td></tr><tr><td>

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when your stage should start running:-   **When process starts**: Your stage starts running as soon as the playbook starts.
-   **After specific stages**: Your stage starts running after specified stage\(s\) have finished running.

Under Schedule &gt; Start Rule, select a start rule for when your activity should start running:-   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **After specific activities**: Your activity starts running after specified activities have finished running.

</td></tr><tr><td>

Tagline

</td><td>

String

</td><td>

Header tagline to display to end users.

</td></tr><tr><td>

Record fields

</td><td>

Reference

</td><td>

Any additional record fields you want in the form.**Note:** This field cannot be edited during a playbook run.

</td></tr><tr><td>

Associated table

</td><td>

Table Name

</td><td>

Table containing activity or playbook data.

</td></tr><tr><td>

Associated record

</td><td>

Reference

</td><td>

Reference to the record you want to display.

</td></tr><tr><td>

Form View

</td><td>

String

</td><td>

Form view to use for data collection. If you don't provide a form view, the system uses the default view. Use the **new tab** button ![a button that opens a new tab](../images/new-tab-button.png)to open and edit a form view with Form Builder in a new Workflow Studio tab.**Note:** Many form views are not supported in Workspace.

</td></tr><tr><td>

Form Fields

</td><td>

String

</td><td>

Comma-separated list of fields names to display on the card for the form.**Note:** Make sure to include the form fields in the default view or the view of your choice, so that the fields are displayed in the playbook.

</td></tr><tr><td>

Attachment source

</td><td>

Choice

</td><td>

The attachment record containing the attachments that end users can upload during runtime.

</td></tr></tbody>
</table>## Advanced inputs

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

<table id="table_cjj_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment Group

</td><td>

Reference.Group \[sys\_user\_group\]

</td><td>

Group responsible for completing the task associated with the activity.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Assigned To

</td><td>

Reference.User \[sys\_user\]

</td><td>

User responsible for completing the task associated with the activity.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Display Order

</td><td>

Choice

</td><td>

The order in which the activity card appears during a playbook run.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Restart rules

</td><td>

Choice

</td><td>

What an activity or stage does during restart:-   **Skip on restart**: The stage or activity only runs during a playbook's initial run. It does not run on restart.

**Note:** This setting is helpful if you don't want new tasks or records to be created during a restarted run, because the original execution and resulting record is still relevant.

-   **Run always**: The stage or activity always runs, whether during an initial or restarted run.
-   **Skip on first run**: The stage or activity runs only on restart. It never runs during an initial run.

To learn more about enabling and configuring restart for playbooks, stages, and activities, see [Configure restart for Playbooks](../task/enable-define-restart.md).

**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Experience Status Table

</td><td>

Table Name

</td><td>

Table containing the Experience Status Record. By default, set to the table containing the flow data record created by this activity's underlying flow, subflow, or action.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Experience Status Record

</td><td>

Reference

</td><td>

The flow data record with the status that you want to map with this activity's state. Changes made to the state in the activity card are mapped to the flow data record, and from the flow data record to the activity card. By default, this is the data record created by this activity's underlying flow, subflow, or action.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Icon

</td><td>

Reference.Icon \[st\_sys\_design\_system\_icon\]

</td><td>

Displays an icon on the activity card.Start entering the icon name and select the icon you want to appear.

**Note:** Select **Show additional options** to see this field.

</td></tr><tr id="activity-input-title"><td>

Title

</td><td>

String

</td><td>

Title displayed to end users in the activity card. You can enter text or use the pill picker.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Description

</td><td>

Reference

</td><td>

Details to display to end users in the activity card. This is not a string field, use the pill picker to choose a description to show in the activity card.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Pending State Title

</td><td>

String

</td><td>

Title displayed to end users for a pending activity. You can enter text or use the pill picker.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Pending State Description

</td><td>

String

</td><td>

Details to display to end users in a pending activity.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Attachments read only

</td><td>

True/False

</td><td>

If enabled, prevents end users from renaming or deleting the existing attachments.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Footer

</td><td>

String

</td><td>

Footer text to display to end users. **Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Show Attachments

</td><td>

True/False

</td><td>

Option to include attachments in the user form.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Show SLA

</td><td>

True/False

</td><td>

Option to show SLA countdown details for the task.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Show Checklist

</td><td>

True/False

</td><td>

Option to show record checklist items.**Note:** Select **Show additional options** to see this field.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Table|Table Name|Name of the table associated with the activity.|
|Record|Reference.Task\[task\]|Reference to the record associated with the activity.|

