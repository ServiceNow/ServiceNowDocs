---
title: Create rollups from one account to another account
description: You can create rollups from one account in the segment hierarchy to another account in a segment above it.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Rollups for allocations - Legacy, Allocation Setup stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create rollups from one account to another account

You can create rollups from one account in the segment hierarchy to another account in a segment above it.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  Click the hyperlink on the name of an account.

    The Account summary pop-up appears, showing you:

    -   The total amount of money currently assigned to the account.
    -   The buckets that contribute expenses to the account.
    -   The method that the account uses to roll up to the parent segments.
    -   The accounts that roll up to the account.
    -   The accounts that the account rolls up to.
2.  To see the buckets that are allocated directly to this account, click **Show allocated buckets** next to the **Total** value.

3.  Click the **Rollups** tab if it is not selected.

4.  Select a method from the **Rollup Method** choice list.

<table id="choicetable_rfd_nl1_yq"><tbody><tr><td id="d261452e115">

**__Segment's default method__**

</td><td>

Expenses follow the default rollup rule for CI relationships that was created during the Data Definition stage. This is the default option for items in the CMDB that roll up to other items in the CMDB.

</td></tr><tr><td id="d261452e127">

**__None__**

</td><td>

Expenses do not roll up to any parent accounts.

</td></tr><tr><td id="d261452e139">

**__Equal__**

</td><td>

Expenses roll up to the parent accounts by the same percentage. Specify the parent accounts.

</td></tr><tr><td id="d261452e151">

**__Manual__**

</td><td>

Expenses roll up to the parent accounts by a percentage that you specify. Enter the amounts in the **Percentage** fields.

</td></tr><tr><td id="d261452e166">

**__Weighted__**

</td><td>

Expenses roll up to parent accounts using a weighted metric that exists. The metrics available are those that specify a rollup to the segment that the parent account belongs to. If a metric has the **Enforce Relationship** option selected, the segment to which the child account belongs is also considered. If a metric does not have the **Enforce Relationship** option selected, the segment of the child account is ignored.

</td></tr><tr><td id="d261452e185">

**__Scripted__**

</td><td>

A script determines the rollup.

</td></tr></tbody>
</table>5.  To link the account with an item above it, click **Add Rollup**.

6.  Select a value in the **Parent Segment** choice list.

7.  Select an account from the **Parent Account** choice list.

8.  If you selected the manual rollup method, enter the amounts in the **Percentage** field.

9.  Enter as many rollups as necessary.

    The percentages must add up to 100%. To remove any of the accounts, click the delete icon \(![The delete icon](../image/Delete_icon.png)\).

10. Click **Save Changes** after making your changes.

    The rollup rules appear in the right pane under the donut chart.

11. To see only those accounts that a selected account rolls up to, click the relationship icon \(![The relationship icon](../image/ITFM_rel_icon.png)\) on the account.

    Only the linked accounts appear. The color of the account that is assigned the expense is a randomly assigned color by the workbench. The color matches the account's color on the donut chart.

    The up arrow icon \(![The up arrow icon](../image/ITFM_acc_seg.png)\) is indicative of rollups defined at segment or account level.

12. To show all accounts in the segment hierarchy again, click ![The relationship icon](../image/ITFM_rel_icon.png).

    When you create a rollup, the system automatically updates the system metric that is used to manage the segment relationships in the hierarchy. This metric is created by the application during the Data Definition stage.


**Parent Topic:**[Rollups for allocations - Legacy](../concept/c_RollupsForAllocations.md)

**Related topics**  


[View accounts that roll up to an account](t_ViewAccountsThatRollUp.md)

[Create rollups from one segment to another](t_CreateRollups1SegToAnother.md)

[Edit rollup records](t_ViewRollupRecords.md)

