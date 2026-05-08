---
title: Update Record activity
description: Update a record with the field values you specify.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Update Record activity

Update a record with the field values you specify.

## Roles and availability

-   This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see Dot-walking examples.

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

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

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

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Table

</td><td>

Table Name

</td><td>

Table containing the record to update.

</td></tr><tr><td>

Record

</td><td>

Reference

</td><td>

Reference to the record you want to update.

</td></tr><tr><td>

Fields

</td><td>

Template Value

</td><td>

Field values to change during record update.

</td></tr><tr><td>

Wait for user input

</td><td>

Choice

</td><td id="wait-process">

Option to pause the playbook until the end user manually completes or skips the activity. Only users with the playbook.admin role can edit this field. By default, the activity waits for user action or data before it completes.

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

Fields to show after update

</td><td>

String

</td><td>

Comma-separated list of fields to display for an updated record.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Table|Table Name|Table containing updated record.|
|Record|Document ID|Reference to record updated.|

## Design considerations

-   **Create form views for activities that you want to render in a playbook**

    Use a form view to display only the fields your users need to update a record. Your view should display required fields or those fields validated by other business logic. See View Management.

-   **Run non-interactive activities before interactive activities**

    If an Update Record activity interactively gathers data from users, it prevents the playbook from starting any dependent activities. For example, an Update Record activity would prevent starting **After Previous** activities, which may be in other stages. Where possible, design your playbooks to run non-interactive activities before interactive activities that could block them.


