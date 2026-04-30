---
title: Set activity definitions
description: Specify the activity definition to determine what to show on the process graph, often choosing activities such as State, Assignment group, and Assigned to. Activity definition enables you to discover, monitor, and improve real processes through the visual representation. The visual representation enables you to understand behaviors and performances by identifying bottlenecks, deviations, and inefficiencies in the workflows.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Scoping your analysis, Create a project or template using Project Builder, Using Process Mining, Process Mining, Platform Analytics]
---

# Set activity definitions

Specify the activity definition to determine what to show on the process graph, often choosing activities such as State, Assignment group, and Assigned to. Activity definition enables you to discover, monitor, and improve real processes through the visual representation. The visual representation enables you to understand behaviors and performances by identifying bottlenecks, deviations, and inefficiencies in the workflows.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

**Note:**

You can configure a maximum of five activity definitions for a table. You can’t generate more than 5000 elements for any activity definition.

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

6.  Fill the form.

<table id="table_cdk_gnq_vkb"><tbody><tr><td>

Select type

</td><td>

The type of values you want to mine.You have the following values:

-   Field Values \(Default\): This is the default selection. This option is available whenever you create an activity definition.
-   Child Attached: This option is available when you’ve selected two tables for table configuration and have set a child-parent relationship. This option is available only for the parent table configuration. In the graph, you see when the child was attached in the process.
-   Date Time: Uses date time value from the actual record rather than the audit history and is displayed as a grouped node on the process map.
-   Compound: Compound events for 2 or more activity definitions that are updated to any value in certain processes, such as sales, finance, or security. A last moment change could infer another approval process and potentially impose additional steps and consequently longer resolution time. It could also result in a compliance breach. For example: if you have 4 activity definitions, but only one is updated, it must be captured in the compound event.

To use a compound activity definition, you must have at least one activity definition of a type other than Compound.

</td></tr><tr><td>

Field

</td><td>

Specify the field or column from the table whose data you want to view in the process graph.

</td></tr><tr><td>

Attached Table Configuration

</td><td>

This field is available only if you choose **Child Attached** in the **Select type** field.Select the table name from the list. However, it displays only the table that is used for the child entity.

</td></tr><tr><td>

Show Related Fields

</td><td>

This field is available only if you choose **Field Values \(Default\)** or **Date Time** in the **Select type** field.If you want to see the list of related fields, select the Related Fields icon \(![Related list](../image/act-def-rel-list.png)\), and select a field.

This field helps you set dot walking on records.

</td></tr><tr><td>

Display name

</td><td>

This field is available only if you select **Field Values \(Default\)** in the **Select type** field.Name to display for this activity. If no name is entered, the **Display name** displays the value provided for **Field**.

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

This field allows you to choose whether you want to view all the changes for an activity definition grouped as one node or view each change for an activity definition as a separate node.

 This field has two options:

-   **Display each unique value as separate activity steps**: If you select this option, the process map reflects the group of changes for the activity as separate item.

**Note:** This is by default disabled for Field Values \(Default\), Child Attached, Date Time, and Compound.

-   **Group unique values and display as a single activity step**: If you select this option, the process map reflects the group of changes for the activity as one change item.
 For example, configure Assignment group and State to report on. Select **Group unique values and display as a single activity step** for Assignment group and **Display each unique value as separate activity steps** for State.

 Changes to assignment group are displayed as one node 'Assignment group changed'. You can view the records or view the details to see which records are affected and how. Every change to State is displayed as an individual node.

 ![Show changes as group](../image/show-changes-group.png "Changes are grouped")

 In the next scenario, configure Assignment group and State to report on and select **Display each unique value as separate activity steps** for Assignment group and State.

 Every change to Assignment group and State are displayed as individual nodes.

 ![Changes are not grouped](../image/dont-show-changes-group.png "Changes aren’t grouped")

</td></tr><tr><td>

Grouped Activities name

</td><td>

Name for the grouped activities.If you select the **Group unique values and display as a single activity step** option, then the **Grouped Activities name** field is displayed.

By default, the name that is displayed is &lt;field-name changed&gt;. For example, 'Assignment group changed'.

</td></tr><tr><td>

Activity of Interest

</td><td>

This field is available only if you have not chosen to group activities.

When this option is selected, activity definitions do not appear on the process graph, but can be used in the findings and transitions.

</td></tr><tr><td>

Start node

</td><td>

This field is available only if you choose **Field Values \(Default\)** in the **Select type** field.When this option is selected, an empty node on the process graph is displayed when the selected activity definition field is empty at the time of record creation.

</td></tr></tbody>
</table>    **Note:** To edit an activity definition, select the activity definition from the list and make edits. To delete an activity definition, select the activity definition from the list and select the Delete icon \(![Delete icon](../image/act-def-delete.png)\).

7.  Select **Save**.

    You will see the list of activity definitions that you have created.

8.  Select **Breakdowns**, **Use cases**, or **Add child entity** in the left panel if you want to add any of these entities.

9.  Select improvement opportunities to set improvement opportunities.

    For more information, see [Set improvement opportunities](improve-opportunities.md)


**Parent Topic:**[Scoping your analysis](../concept/scope-analysis.md)

**Related topics**  


[Set breakdown definitions](breakdown.md)

[Set use cases](adv-settings.md)

[Add a child entity](child-entity.md)

