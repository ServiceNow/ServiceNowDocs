---
title: Set filter conditions
description: Set filter conditions to limit the scope of your analysis.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scoping your analysis, Create a project or template using Project Builder, Using Process Mining, Process Mining, Platform Analytics]
---

# Set filter conditions

Set filter conditions to limit the scope of your analysis.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## About this task

Setting filters is an optional task for project creation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

    If you continue from the **Set Objectives** page, you are on the **Scope your analysis** page.

2.  Select **Edit** for the project that you want to edit.

3.  Select the edit button for the **Scope your analysis** section.

4.  Select **Filter conditions** from the left bar.

    **Tip:** Select **Advanced view** on the top-right corner if you want to edit the project in the Classic view.

    ![Filter conditions](../image/filter-cond.png)

5.  Fill the form with details.

<table id="table_cdk_gnq_vkb"><tbody><tr><td>

Source

</td><td>

It’s automatically populated based on your selection in the **Set objectives** tab.

</td></tr><tr><td>

Select

</td><td>

It’s automatically populated based on the table that you have selected in the **Set objectives** tab.

</td></tr><tr><td>

Filters

</td><td>

Select any field from the root table that you want to filter the data by.

</td></tr><tr><td>

Related List Condition

</td><td>

Select the number of records that you want to view.

</td></tr><tr><td>

Crop process

</td><td>

Crop the process to view a specific area of the process by specifying a start and end condition. All events that occurred before the start condition and after the end condition will not appear in the process graph.

 **Note:** You can specify the crop process on the same field that you have chosen to set your activity definition. Therefore, set the activity definition for the project, before setting the crop process.

 Select the + sign beside Start condition and End condition. Set a process start and process end condition.

 Example: If a project is set with the State as the activity definition, you have the following path:

 **New -&gt; Open -&gt; Work in Progress -&gt; Resolved -&gt; Work in Progress -&gt; Resolved -&gt; Closed**

 If a stop condition is specified on last occurrence of resolved the model would look like this: **New -&gt; Open -&gt; Work in Progress -&gt; Resolved -&gt; Work in Progress -&gt; Resolved**.

 If the stop condition was configured on the first occurrence of resolved the model would be **New -&gt; Open -&gt; Work in Progress -&gt; Resolved** like this

</td></tr></tbody>
</table>6.  Select **Save**.


**Parent Topic:**[Scoping your analysis](../concept/scope-analysis.md)

