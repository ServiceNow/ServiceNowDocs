---
title: Assign a bucket to a segment or an account
description: During the Allocation Setup stage in the workbench, you can assign expenses from buckets to accounts in the hierarchy.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Bucket assignments, Allocation Setup stage, Financial Management workbench, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Assign a bucket to a segment or an account

During the Allocation Setup stage in the workbench, you can assign expenses from buckets to accounts in the hierarchy.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  Drag a bucket to a specific account.

    You can also select multiple buckets and drag them to a specific account. If a bucket is allocated to an account, then the allocation method is always Allocate 100%.

    Alternatively, select one or multiple buckets. Click the **Assign bucket** icon \(![The allocation icon](../image/Bucket_allocation_icon.png)\) that contains the expenses you want to assign to a single account or multiple accounts by performing the following steps:

    1.  Under **Allocate Method**, select allocate to an account.

    2.  Under **Allocate To Segment**, select a segment.

    3.  Under **Allocate to Account**, select the segment account to which you want to assign all expenses in the selected buckets.

    4.  On the other hand, to assign the selected buckets to multiple accounts, click **Go** with the default **Multiple Accounts** selected under **Allocate To Account**.

        The Create Allocation Rule window appears showing you a list of **Selected Buckets** along with the selected account or option to choose the accounts in the selected segment. If you don’t want to allocate a bucket, select and delete the bucket.

2.  Drag a bucket to a segment or click the **Assign bucket** icon \(![The allocation icon](../image/Bucket_allocation_icon.png)\) to assign a bucket to a segment.

    You can assign a bucket to a segment one at a time. Multiple-bucket selection doesn’t apply for segment assignment. If the bucket allocation is to a segment, then you must select the allocation method from the choice list.

<table id="choicetable_lw3_zjd_yq"><tbody><tr><td id="d192590e152">

**__Equal__**

</td><td>

Expenses are assigned to the accounts by the same percentage.

</td></tr><tr><td id="d192590e164">

**__Manual__**

</td><td>

Expenses are assigned to the accounts by a specified percentage. Enter the amounts in the **Percentage** fields.

</td></tr><tr><td id="d192590e179">

**__Weighted__**

</td><td>

Expenses are assigned to the accounts using a weighted metric.If the metric is configured with [Total weight](t_CreateWeightedAllocationMetrics.md#enforce-allocation), you can’t split a bucket using that weighted metric.

</td></tr></tbody>
</table>3.  From the **Divide among** choice list, select a segment.

4.  If you’ve selected a weighted method, select a preconfigured metric from the **Divide using metric** choice list.

    The only metrics that are available are those metrics that specify the parent and child segments.

5.  Click **Create**.

6.  To know how the bucket amount was distributed previously to the segments or an account, click the bucket name.

    The bucket opens up in a pop-up displaying a message on top. The message displays the allocation method by which the bucket amount has been distributed, and the name of the segment to which the amount has been assigned. If the assignment is by **Allocate to account** method, then the message also displays the account name and the percentage of allocation.

    ![A sample message of bucket assignment information](../image/BucketAssignmentMessage.png "Sample message of bucket assignment information")


**Parent Topic:**[Bucket assignments](../concept/c_BucketAssignments.md)

