---
title: Create a business rule for high-level planning
description: To enable high-level planning on a table that is not a planning item in Strategic Planning Workspace, create a business rule to allow assigning a rank value for all future records of this table.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [High-level planning configuration in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Create a business rule for high-level planning

To enable high-level planning on a table that is not a planning item in Strategic Planning Workspace, create a business rule to allow assigning a rank value for all future records of this table.

## Before you begin

[Populate global rank for high-level planning items](populate-global-rank-for-high-level-planning-items.md).

Role required: admin

## About this task

All future records of your high-level planning entity must have a global rank so that when your planning managers reorder and prioritize items of this type in their portfolio plan, their rank is automatically updated. To enable this auto assigning of rank value to any new records, create a business rule.

For this task, consider the example of creating a business rule on the Strategic Priority \[sn\_gf\_strategy\], to enable auto-assignment of rank value for all its future records.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Search for and open your planning item table.

    For example, search for and open the Strategic Priority \[sn\_gf\_strategy\] table.

3.  Right-click the form header and select **Configure** &gt; **Business Rule**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_vsr_jh2_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the rule.For example, **Strategic Priority rank insert rule**.

</td></tr><tr><td>

Table

</td><td>

Table on which this business rule is applied.For this example, select **Strategic Priority \[sn\_gf\_strategy\]**.

</td></tr><tr><td>

Advanced

</td><td>

Option to enable advanced settings for this business rule.

</td></tr></tbody>
</table>6.  In the Advanced related list, enter the following code in the **Script** field.

    ```
    (function executeRule(current, previous /*null when async*/)
    {
        var spwRankingHelper = new sn_align_core.SPWRankingHelper();
        var rankConfig = spwRankingHelper.getRankConfiguration(current.getTableName());
        if (rankConfig.isValidRecord())
        {
            var sequencer = new sn_align_core.AlignmentPlanningRankProcessor(rankConfig.getValue("table"), rankConfig.getValue("column"));
            sequencer.generateNewIndex(current);
        }
    })
    (current, previous);
    ```

7.  In the When to run related list, enable the **Insert** option.

8.  Save the form.


## Result

This task is the end of the series of tasks to enable high-level planning on a table that does not extend the Planning Item \[sn\_align\_planning\_item\] table. After this task is complete, you can notify your planning managers that they can start creating portfolio plans for the configured entity type.

See [Managing portfolio plans in Strategic Planning Workspace](../concept/managing-portfolio-plans-in-alignment-planner-workspace.md).

