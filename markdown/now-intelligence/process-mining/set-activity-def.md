---
title: Set activity definitions
description: Set activity definitions to determine what appears on the process graph, such as State, Assignment group, or Assigned to. This enables you to discover, monitor, and improve processes by visually identifying bottlenecks, deviations, and inefficiencies in workflows.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Scoping your analysis, Create a project or template using Project Builder, Using Process Mining, Process Mining, Platform Analytics]
---

# Set activity definitions

Set activity definitions to determine what appears on the process graph, such as State, Assignment group, or Assigned to. This enables you to discover, monitor, and improve processes by visually identifying bottlenecks, deviations, and inefficiencies in workflows.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

**Note:** You can configure a maximum of five activity definitions for a table. You can’t generate more than 5000 elements for any activity definition.

## About this task

Setting activity definitions is a required task to create a project.

Process Mining gathers audit log field data for the activities that you define. Configure at least one activity to create a Process Mining project.

**Note:** When configuring a project, start by setting up the main \(parent\) table, defining the activity and breakdown definitions. If only one table is needed, generate the full project with the data. For multiple tables, create additional \(child\) tables, relate them to the main table, and define their activity definitions.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Mining Workspace**.

    If you continue from the **Set Objectives** page, you are on the **Scope your analysis** page.

2.  Select **Edit** for the project that you want to edit.

3.  Select the edit button for the **Scope your analysis** section.

    **Tip:** Select **Advanced view** on the top-right corner if you want to edit the project in the Classic view.

4.  Select **Activities** from the left bar.

5.  Select **New** in the Activities area.

    ![Set activity definition](../image/set-activity-def.png)

6.  Fill the form.

<table id="table_cdk_gnq_vkb"><tbody><tr><td>

Select type

</td><td>

The type of values you want to mine.You have the following values:

-   Field Values \(Default\): This is the default selection. This option is available whenever you create an activity definition.

Selecting any journal or textual fields for activity definitions, sets the grouped value to “Group values into a single activity step”.

-   Child Attached: This option is available when you’ve selected two tables for table configuration and have set a child-parent relationship. This option is available only for the parent table configuration. In the graph, you see when the child was attached in the process.
-   Date Time: Uses date time value from the actual record rather than the audit history and is displayed as a grouped node on the process map.
-   Compound: Compound events for 2 or more activity definitions that are updated to any value in certain processes, such as sales, finance, or security. A last-moment change could infer another approval process and potentially impose additional steps and consequently longer resolution time. It could also result in a compliance breach. For example: If you have 4 activity definitions, but only one is updated, it must be captured in the compound event.

To use a compound activity definition, you must have at least one activity definition of a type other than Compound.

You can create a compound activity for any journal or textual fields, such as work notes or comments.

</td></tr><tr><td>

Field

</td><td>

Specify the field or column from the table whose data you want to view in the process graph.

</td></tr><tr><td>

Get recommended fields

</td><td>

This field is available only if you choose **Field Values \(Default\)** in the **Select type** field.This button provides recommendations of fields that are ideal to be set as activity definitions for your project.

These recommendations come from the process configuration set for the table on which the project is based. They’re derived from the Process perspectives section of the Process details page in the Process Configuration Builder.

For more information on Process perspectives, see [Configure process details](process-details.md).

The recommendation is provided even if you don’t specify anything in the process configuration for the table. If nothing is configured on the Process details page, we recommend the fields that have high frequency of change.

Select the button, and a dialog box is displayed to select from the list of recommended fields. Select the fields, and select **Select**.

You can choose to use any other field outside of the recommendation too.

![Recommendations in activity definition based on the setting in process configuration](../image/act-def-recom.gif)

</td></tr><tr><td>

Attached Table Configuration

</td><td>

This field is available only if you choose **Child Attached** in the **Select type** field.Select the table name from the list. However, it displays only the table that is used for the child entity.

</td></tr><tr><td>

Show Related Fields

</td><td>

This field is available only if you choose **Field Values \(Default\)** or **Date Time** in the **Select type** field.If you want to see the list of related fields, select the Related Fields icon \(![Related list](../image/act-def-rel-list.png)\), and select a field.

This field helps you set dot-walking on records.

</td></tr><tr><td>

Display name

</td><td>

Name to display for this activity. If no name is entered, the **Display name** displays the value provided for **Field**.

</td></tr><tr><td>

Display order

</td><td>

This field isn’t available if you select **Contextual activity**.The value in this field decides which events must be displayed first on the process graph when multiple activity definitions have the same timestamp.

When multiple activity definitions have the same display order, the alphabetic order is applied.

Provide any value \(only integers\). The default value is set to 50.

</td></tr><tr><td>

Select specific activity values

</td><td>

This field is available only if you choose **Field Values \(Default\)** in the **Select type** field.You can choose to mine specific activity values for the selected field. Select the specific activity values that you want to analyze.

You can select the values and choose to include or exclude.

![List of values](../image/ad-listofvalues.png)

For example, you have chosen the **Incident** table. Now, you want to see records that went through Assignment group Service Desk and Assignment group Database. To see this data, you must select **Assignment group** as the **Field** and add **Service Desk** and **Database** from **List of values**.

</td></tr><tr><td>

Group activities

</td><td>

This field enables you to choose whether you want to view all the changes for an activity definition grouped as one node or view each change for an activity definition as a separate node.

 When you select the field as journal or textual fields for **Field Values \(Default\)** type or when you select the **Compound** type, this field is selected and is unavailable for any change.

 This field has two options:

-   **Display each unique value as separate activity steps**: If you select this option, the process map reflects the group of changes for the activity as separate item.

**Note:** This is by default disabled for Field Values \(Default\), Child Attached, Date Time, and Compound.

-   **Group unique values and display as a single activity step**: If you select this option, the process map reflects the group of changes for the activity as one change item.
 For example, configure Assignment group and State to report on. Select **Group unique values and display as a single activity step** for Assignment group and **Display each unique value as separate activity steps** for State.

 Changes to assignment group are displayed as one node 'Assignment group changed'. You can view the records or view the details to see which records are affected and how. Every change to State is displayed as an individual node.

 ![Show changes as group](../image/show-changes-group.png "Changes are grouped")

 In the next scenario, configure Assignment group and State to report on and select **Display each unique value as separate activity steps** for Assignment group and State.

 Every change to Assignment group and State is displayed as individual nodes.

 ![Changes are not grouped](../image/dont-show-changes-group.png "Changes aren’t grouped")

</td></tr><tr><td>

Grouped Activities name

</td><td>

Name for the grouped activities.If you select the **Group unique values and display as a single activity step** option, then the **Grouped Activities name** field is displayed.

By default, the name that is displayed is &lt;field-name changed&gt;. For example, 'Assignment group changed'.

</td></tr><tr><td>

Contextual activity

</td><td>

This field is available only if you have not chosen to group activities.

When this option is selected, activity definitions don’t appear on the process graph, but can be used in the findings and transitions.

</td></tr><tr><td>

Start node

</td><td>

This field is available only if you choose **Field Values \(Default\)** in the **Select type** field.When this option is selected, an empty node on the process graph is displayed when the selected activity definition field is empty at the time of record creation.

</td></tr></tbody>
</table>    **Note:** To edit an activity definition, select the activity definition from the list and make edits. To delete an activity definition, select the activity definition from the list and select the Delete icon \(![Delete icon](../image/act-def-delete.png)\).

7.  Select **Save**.

    The list of activity definitions that you have created is displayed.

8.  Select **Breakdowns**, **Use cases**, or **Add child entity** in the side panel if you want to add any of these entities.

9.  Select improvement opportunities to set improvement opportunities.

    For more information, see [Set improvement opportunities](improve-opportunities.md)


**Parent Topic:**[Scoping your analysis](../concept/scope-analysis.md)

**Related topics**  


[Set breakdown definitions](breakdown.md)

[Set use cases](adv-settings.md)

[Add a child entity](child-entity.md)

