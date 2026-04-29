---
title: Activity definition form
description: Use the Activity Definition form to report on steps that occur within your business process.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Process Mining, Platform Analytics]
---

# Activity definition form

Use the Activity Definition form to report on steps that occur within your business process.

<table id="table_cdk_gnq_vkb"><tbody><tr><td>

Field

</td><td>

Specify the field or column from the table whose data you want to view in the process graph.

</td></tr><tr><td>

Type

</td><td>

The type of values you want to mine.You have the following values:

-   Field Values \(Default\): This is the default selection. This option is available whenever you create an activity definition.
-   Date Time: Uses date time value from the actual record rather than the audit history and is displayed as a grouped node on the process map.
-   Compound: One node or process graph representing change in the multiple field value from the actual record rather than the audit history.
-   Child Attached: This option is available when you have selected two tables for table configuration and have set a child-parent relationship. This option is available only for the parent table configuration. In the visualization, you will see when the child was attached in the process.
-   Parent Attached: This option creates a node on the child process representing when a parent record was attached to a child.

</td></tr><tr><td>

Display Name \(Optional\)

</td><td>

Name to display for this activity. If no name is entered, the activity name displays the value provided for **Field**.

</td></tr><tr><td>

Choose activity values

</td><td>

You can choose to mine specific activity values for the selected field.

</td></tr><tr><td>

Activity values

</td><td>

This field is available only if you select the **Choose activity values** field.

 This field provides a list of values for the selected field that you want to mine.

 For example, you have chosen the **Incident** table. Now, you want to see records that went through Assignment group Service Desk and Assignment group Database. To see this data, you must select **Assignment group** as the **Field** and add **Service Desk** and **Database** from **List of values**.

</td></tr><tr><td>

Group activities

</td><td>

If you select to group activities, the process map reflects the group of changes for the activity as one change item. For example, suppose you configure **Assignment group** to report on and select group activities. -   Changes to assignment group occur and list in the audit log as: Group A &gt; Group B &gt; Group C.
-   Result: The data in the process map reflects as one change: 'Assignment group changed'.

If this option is not checked, the process map reflects records of each instance of change individually. Example: You configure **Assignment group** to report on, but don't select to group activities.

-   Changes to assignment group occur and list in the audit log as: Group A &gt; Group B &gt; Group C.
-   Result: The process map reflects each individual change made, continuing to reflect the changes as is standard from the audit log: 'Change: Group A &gt; Change: Group B &gt; Change: Group C'.

 ![Show changes as group](../image/show-changes-group.png "Changes are grouped")

 ![Changes shown as standard](../image/dont-show-changes-group.png "Changes shown as standard")

</td></tr><tr><td>

Grouped Activities name

</td><td>

Auto-generated name for grouped activities, or you can enter a different name for changes to the field that will reflect in the visualization.**Note:** This field is only available when the **Group activities** field is selected.

</td></tr><tr><td>

Activity of Interest

</td><td>

Whether field changes appear in the analyst workbench. **Note:** When this option is selected, field changes don’t appear in the analyst workbench, but can still be used in contextual conditions in transitions or findings.

</td></tr><tr><td>

Include empty start node

</td><td>

Includes an empty node on the process graph when the selected activity definition field is empty at the time of record creation.

</td></tr></tbody>
</table>**Parent Topic:**[Process Mining reference](../concept/process-mining-reference.md)

