---
title: Split buckets
description: Buckets contain groomed general ledger expenses. These expenses can be associated with items like a cost center, vendor, department, or location.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Allocation Setup stage, Financial Management workbench, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Split buckets

Buckets contain groomed general ledger expenses. These expenses can be associated with items like a cost center, vendor, department, or location.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

You can only split buckets that are not yet assigned to accounts.

## About this task

You can split the expenses in a bucket by any of the attributes such as cost center, vendor, department, or location. Starting with Istanbul release, you can use any custom attributes to split buckets. Use Financial Data Source Field Map for bringing additional attributes to split a bucket by enabling the **Used for Bucket split** option.

For example, if a bucket includes expenses for two different vendors, you can split the bucket into two smaller buckets, one for each vendor. Each split bucket contains the groomed general ledger expense associated with that vendor.

## Procedure

1.  Open the [Allocation Setup](../concept/c_TheAllocationSetupStage.md) stage in the workbench.

2.  In the **Allocation Setup** pane, click the split bucket icon \(![The bucket tree icon](../image/Bucket_tree_icon.png)\) for the bucket you want to split.

    The split bucket window appears, showing you the amount of money in the bucket.

3.  From the **Split by** list, either select an attribute that is associated with the groomed general ledger expense or select **Percentage**.

    -   If you select an attribute, the new buckets appear in the window with default names in the format \[original bucket name\] &gt; \[attribute name\].
    -   If you select **Percentage**, enter the percentages for the new buckets and give each bucket a name.
    -   If you select **Weighted** split method, you have the choice to split the bucket amount to any segment in the hierarchy based on the available metric.

        **Note:**

        If the metric is [Total weight](t_CreateWeightedAllocationMetrics.md#enforce-allocation) configured, then you cannot split a bucket using that weighted metric.

        After you split a bucket based on the **Weighted** method, you cannot split it further.

    A preview of the split buckets appears in the window along with the expense amounts for each bucket.

4.  Click **Split Bucket**.

5.  The application creates new buckets and splits the expenses among them according to your settings.

    Buckets that are split appear with a folder icon.

    ![A split bucket](../image/SplitBucketIcon.png "Split bucket")

6.  To view a newly split bucket with the other buckets that were split along with it, click the folder icon.

7.  To revert the bucket split, click **Unsplit Bucket**.

    ![Splitting the hardware bucket](../image/Split_buckets_hardware.png "Splitting the hardware bucket")


**Parent Topic:**[Allocation Setup stage](../concept/c_TheAllocationSetupStage.md)

**Related topics**  


[View bucket contents](t_ViewBucketContents.md)

[Rollups for allocations](../concept/c_RollupsForAllocations.md)

[Bucket assignments](../concept/c_BucketAssignments.md)

[Review assigned expenses](t_ReviewAssignedExpenses.md)

[Verify the total amount allocated](t_VerifyTotalAmountAllocated.md)

[Preview an allocation from a bucket](t_PreviewAnAllocationFromABucket.md)

[Revert bucket assignments](t_RevertBucketAssignments.md)

