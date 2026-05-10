---
title: Create Record activity
description: Pause the playbook and prompt the end user to create a record in a form view. Use this activity to allow the end user to create a record. This activity requires you to configure the desired table for which record to create, and the desired form view that the end user will see when creating the record.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Create Record activity

Pause the playbook and prompt the end user to create a record in a form view. Use this activity to allow the end user to create a record. This activity requires you to configure the desired table for which record to create, and the desired form view that the end user will see when creating the record.

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

Table in which to insert new record.

</td></tr><tr><td>

Create Record View

</td><td>

String

</td><td>

Form view to use for record creation. If you don't provide a form view, the system uses the default view. Use the **new tab** button ![a button that opens a new tab](../images/new-tab-button.png)to open and edit a form view with Form Builder in a new Workflow Studio tab.**Note:** Many form views are not supported in Workspace.

</td></tr><tr><td>

Template Fields

</td><td>

Template Value

</td><td>

Field values to set during record creation.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Table|Table Name|Table containing new record.|
|Create Record View|String|Form view used for record creation.|
|Record Created|Sys ID|Unique identifier of the record that this activity created.|

## Design considerations

-   **Create form views for activities that you want to render in a playbook during runtime.**

    Use a form view to display only the fields your users need to create a record. Your view should display required fields or those fields validated by other business logic. See [View Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/view-management-overview.md).

-   **Run non-interactive activities before interactive activities**

    While a Create Record activity interactively gathers data from users, it prevents the playbook from starting any dependent activities. For example, a Create Record activity would prevent starting **After Previous** activities, which may be in other stages. Where possible, design your playbooks to run non-interactive activities before interactive activities that could block them.


