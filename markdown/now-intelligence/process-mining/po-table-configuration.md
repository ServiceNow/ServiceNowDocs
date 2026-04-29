---
title: Set up a table configuration
description: Define the kind of data or process that you want to view and analyse in your graph. You must select a specific table \(parent table\) that has the data that you want to analyse.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a project using Classic view, Use, Process Mining, Platform Analytics]
---

# Set up a table configuration

Define the kind of data or process that you want to view and analyse in your graph. You must select a specific table \(parent table\) that has the data that you want to analyse.

## Before you begin

Role required: sn\_process\_mining\_power\_user

## Procedure

1.  Open your project, and select the **Table Configurations** tab.

2.  Select **New**.

    A new **Table Configuration** page is displayed.

    ![Table configuration](../image/multi-dimension-1.png)

3.  Enter a name for the table configuration in the **Name** field.

4.  In the **Table Condition** tab, fill in the fields.

<table id="table_ir5_v5f_2vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source type

</td><td>

The source for the table configuration. You can select a source type:

 -   Table: Any database table
-   Report source: A table that has reports
-   Archived data: An archived table


</td></tr><tr><td>

Include approvals

</td><td>

Whether approvals are included.

</td></tr><tr><td>

Table

</td><td>

Select the appropriate table.

</td></tr><tr><td>

Filter

</td><td>

Use the conditions in the Filter section to select the data that you want to analyze.**Note:** Avoid long transaction times by limiting data to 1 to 3 months period.

Select **Preview** to see the number of records available for the set filter.

</td></tr></tbody>
</table>5.  Select **Submit** to save the table configuration.

    You are taken to the Table Configuration page displaying the table configuration that you have created. Configure an activity definition for the table configuration. For more information, see [Configure an activity definition](configure-activity.md)


-   **[Configure multi-dimensional mining](configure-multidimensional-mining.md)**  
Use multi-dimensional mining to identify inefficiencies and improve performance by evaluating data from multiple related tables.
-   **[Configure advanced conditions: crop process](po-advanced-conditions.md)**  
Configure custom start and end conditions for your table configuration to define which part of the process should be included in the Process Mining project and made available for analysis.

**Parent Topic:**[Create a project using Classic view](create-proj.md)

