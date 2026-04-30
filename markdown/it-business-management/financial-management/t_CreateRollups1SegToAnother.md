---
title: Create rollups from one segment to another
description: A segment can roll up to the segment above it in the hierarchy using a weighted metric.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Rollups for allocations - Legacy, Allocation Setup stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create rollups from one segment to another

A segment can roll up to the segment above it in the hierarchy using a weighted metric.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  Click the information icon \(![The information icon](../image/Information_icon.png)\) on a segment.

2.  In the **Rollup Method** choice list, select **Weighted**.

    1.  Select the metric in the **Divide using metric** choice list.

        The metric automatically weights the amounts by the values in the **Value** column.

    2.  To further change the amounts, modify the values in the **Percentage** column.

        ![An example rollup](../image/Segment_summary_workbench.png "Rollup example")

    3.  Click **Save Changes**.

3.  In the **Rollup Method** choice list, select **Scripted**.

    1.  On the form, fill in the fields.

<table id="table_jcw_1cl_gdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Scope

</td><td>

Enabling the **Account Scope** check box executes the rollup script defined for each of the accounts at the segment level. Disabling the check box executes the default rollup defined at the segment level, thereby overriding the rollup defined for each account with the sys\_id \(FromAccountID\).Instead of repeating similar rollup scripts for the accounts under a segment, you can provide the rollup scripts for individual accounts using the FromAccountID of each account. You can provide a default rollup for all the remaining accounts for which you have not provided the FromAccountID. You can provide all these rollups in a single script for execution.

</td></tr><tr><td>

Script

</td><td>

The script to rollup the accounts.

</td></tr></tbody>
</table>    2.  Click **Update**.

    Grouping segments by an attribute: You can categorize the segment accounts using the group by attribute if there are thousands of segment accounts. The accounts roll up to the grouped segments, just as they roll up to a non-grouped segment, and the allocation lines are generated in the itfm\_allocation\_breakdown table. Rolling up to grouped segments helps in better performance.


**Parent Topic:**[Rollups for allocations - Legacy](../concept/c_RollupsForAllocations.md)

**Related topics**  


[View accounts that roll up to an account](t_ViewAccountsThatRollUp.md)

[Create rollups from one account to another account](t_CreateRollupsOneAcctToAnother.md)

[Edit rollup records](t_ViewRollupRecords.md)

