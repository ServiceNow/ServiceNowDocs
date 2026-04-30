---
title: View accounts that roll up to an account
description: You can view the accounts that roll up to another account.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Rollups for allocations, Allocation Setup stage, Financial Management workbench, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# View accounts that roll up to an account

You can view the accounts that roll up to another account.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  Click the information icon \(![The information icon](../image/Information_icon.png)\) on an account.

    The account summary window appears, showing you:

    -   The total amount of money currently assigned to this account.
    -   The buckets that contribute expenses to this account.
    -   The method that this account uses to roll up to the parent segments.
    -   The accounts that roll up to this account.
    -   The accounts that this account rolls up to.
2.  To see the buckets that are allocated directly to this account, click **Show allocated buckets**.

3.  If you want to allocate one or more bucket amount \(among all the buckets allocated to this account, as mentioned in step 2\) to any specific account segment overriding the default rollups, then click the **Bucket Rollups** tab.

    You can do such a bucket based rollup using the None, Equal, Manual, Weighted, or Scripted methods.

    The other undefined buckets, which are not rolled up in this manner, follow the default rollup method.

    Navigate to **Financial Modeling** &gt; **Cost Models** &gt; **Allocation Rollups Override** to view the **From Account Segment**, **To Account Segment**, rollup metric, and type details of such an allocation.

    ![Bucket based rollup](../image/bucket-based-rollup.png "An example of bucket based rollup")

4.  Click the **Accounts Rolling Up** tab if it is not selected.

    You can see the accounts that roll up, and the buckets that comprise the **Total** expenses for the account.

5.  Click the information icon to view an account that rolls up or a bucket.

6.  To sort the list, click the gear icon and choose the number of items per page and specify how to sort the items.


**Parent Topic:**[Rollups for allocations](../concept/c_RollupsForAllocations.md)

**Related topics**  


[Create rollups from one account to another account](t_CreateRollupsOneAcctToAnother.md)

[Create rollups from one segment to another](t_CreateRollups1SegToAnother.md)

[Edit rollup records](t_ViewRollupRecords.md)

