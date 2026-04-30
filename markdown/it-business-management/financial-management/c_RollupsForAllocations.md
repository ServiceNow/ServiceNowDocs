---
title: Rollups for allocations - Legacy
description: A rollup is an allocation rule that specifies how a lower-level account in the segment hierarchy connects to other accounts above it in the hierarchy. Rollups allow you to allocate expenses to the lower-level account and have expenses automatically allocated to the higher-level accounts.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Allocation Setup stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Rollups for allocations - Legacy

A rollup is an allocation rule that specifies how a lower-level account in the segment hierarchy connects to other accounts above it in the hierarchy. Rollups allow you to allocate expenses to the lower-level account and have expenses automatically allocated to the higher-level accounts.

Rollups can be account-specific or segment-specific. Account-specific rollups specify how expenses roll up from one specific account to one or more accounts above it. Segment-specific rollups specify how expenses in all the accounts for a segment roll up to all the accounts in the segment above it, that is the parent level. You can also roll up segments to any segment preceding in the hierarchy, that is to the grandparent level.

Rollups specified for an individual account take precedence over the rollup specified for the segment. For example, if you create these two rollups:

-   An account-specific rollup that allocates expenses in the email account in the business service segment to the IT account in the business unit segment.
-   A segment-specific rollup that allocates expenses in the business service segment to the business unit segment.

Then the account-specific rollup allocates the expenses. The segment-specific rollup does not allocate any expenses.

Account-specific level rollup supports rolling to any parent or grandparent account in the hierarchy. You can roll up the expenses to any account up in the hierarchy, and not necessarily to the immediate parent in the hierarchy.

Rollups can not only be up in the hierarchy, you can also roll up amounts to accounts in the sibling segments.

Configure the rollup at the account level to any parent segment in the hierarchy, by selecting the **Parent Segment** in the Rollups popup.

## Total weight support for allocations using weighted metric

If you use a weighted metric that is enabled with [total weight support](../task/t_CreateWeightedAllocationMetrics.md#enforce-allocation), then the metric calculates the allocation percentage accurately in the following total weight calculations:

-   At segment level rollup, where **allocate to** metric is used and accounts do not have any rollup, the total percentages of all accounts in the segment add up to be less than 100%.
-   At segment level rollup, where **allocate to** metric is used, the percentage of each account in the segment is calculated based on the consumption weight of the account.
-   At account level rollup, where the account level rollup rule overrides the segment level rollup rule, the total percentage of all accounts adds up to be less than 100%.
-   At account level rollup, the percentage of each account is calculated based on the consumption weight of the account.
-   When allocating a bucket amount to a segment, the total percentage allocated to the segment adds up to be less than 100%.
-   When allocating a bucket amount to a segment, the percentage allocated individually to each account in the segment is calculated based on the consumption weight of the account.

-   **[View accounts that roll up to an account](../task/t_ViewAccountsThatRollUp.md)**  
You can view the accounts that roll up to another account.
-   **[Create rollups from one account to another account](../task/t_CreateRollupsOneAcctToAnother.md)**  
You can create rollups from one account in the segment hierarchy to another account in a segment above it.
-   **[Create rollups from one segment to another](../task/t_CreateRollups1SegToAnother.md)**  
A segment can roll up to the segment above it in the hierarchy using a weighted metric.
-   **[Edit rollup records](../task/t_ViewRollupRecords.md)**  
You can view and edit records for segment rollups and account rollup if necessary.

**Parent Topic:**[Allocation Setup stage - Legacy](c_TheAllocationSetupStage.md)

**Related topics**  


[View bucket contents - Legacy](../task/t_ViewBucketContents.md)

[Split buckets - Legacy](../task/t_SplitBuckets.md)

[Bucket assignments - Legacy](c_BucketAssignments.md)

[Review assigned expenses - Legacy](../task/t_ReviewAssignedExpenses.md)

[Verify the total amount allocated - Legacy](../task/t_VerifyTotalAmountAllocated.md)

[Preview an allocation from a bucket - Legacy](../task/t_PreviewAnAllocationFromABucket.md)

[Revert bucket assignments - Legacy](../task/t_RevertBucketAssignments.md)

