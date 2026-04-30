---
title: Allocation Setup stage - Legacy
description: The Allocate Setup stage enables you to assign expenses to accounts and segments.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Allocation Setup stage - Legacy

The Allocate Setup stage enables you to assign expenses to accounts and segments.

On the Allocation Setup page, the sub-buckets that you created appear in the left pane, except for sub-buckets that you excluded from the cost model. The segments and their accounts appear in the middle pane, in the hierarchy that you defined in the data definition stage. The summary in the right pane provides a breakdown of how the expenses are assigned to accounts in each segment.

In the Allocation Setup stage, you can:

-   View bucket contents and split buckets into smaller buckets, if necessary.
-   Create and modify rollups to specify exactly how expenses are applied to higher-level segments in the hierarchy.
-   Assign expenses to accounts.
-   Review assigned expenses and revert bucket assignments if necessary.
-   Filter the allocation setup segment account by amounts greater than, lesser than, or equal to a certain value.
-   [Configure the Display Records per segment](../task/t_ConfigureGeneralSettings.md#step_itfm_configset) pagination option in the Configuration tab to display 5, 10, 15, 25, or 50 accounts per page at the same time. The pagination option displays the selected number of accounts out of the total number of accounts in a segment per page. The right and left arrows help you to navigate to the next set of records until all the accounts in the segment are displayed.
-   Similarly, view selected number of accounts on the lighter workbench page by setting up the pagination option in the Configuration tab.

![Setting up allocations on the workbench](../image/Allocation_setup.png "Setting up allocations on the workbench")

## Basic allocation setup

This feature helps you to use allocation setup with ease especially while dealing with large accounts and allocation rules.

Configure basic allocation setup parameter to open the allocation setup UI in a lighter mode. Enabling basic allocation setup helps you to open the allocation setup page faster with minimal information, without having the UI loaded with the amount previews along with the accounts. Information in basic allocation setup is fetched only on demand.

Functionally, with basic allocation setup you can do all functions as in the regular allocation setup UI, where the primary purpose is to allocate bucket accounts and define rollup allocation rules. The icon indicators for buckets and rollups guide you when rules are defined in basic allocation setup.

**Note:** If you are a non-analyst licensed customer, the **Basic Allocation Setup** option is enabled automatically even though the option is disabled if:

-   The number of accounts in a segment exceeds the threshold value \(4000\)
-   The total number of accounts in the cost model exceeds the threshold value \(12000\)

With this parameter enabled, you cannot view the following details:

-   The amount preview displayed in each of the accounts.
-   The summary chart in the right pane.
-   The **See relationships** link in the accounts. However, you can view the accounts that each account rolls up to, on demand, in the **Accounts Rolling Up** tab in accounts pop-up.

## Missing money analysis

**Note:**

Missing money analysis is an extended and improved version of the allocation log functionality available before the Madrid release.

During the allocation setup stage, there is a possibility that the amount may not be rolled up correctly and the money may go missing during the process. The reasons can be due to errors in any of the following stages:

-   Bucket Allocation
-   Segment Rollup
-   Account Rollup

Missing money logs provide details of why a part of the amount may be missing and fail to reach the target segment or account as per the allocation rules that have been set, and an actionable link to resolve issues.

To [configure missing money logs](../task/t_ConfigureGeneralSettings.md), click the **Configuration** tab and toggle **Missing Money Analysis** to enable the logs. This action enables the **Missing Money Logs** \(![Missing money analysis log icon](../image/MissingMoneyLogsIcon.png)\) icon in the allocation setup stage of the workbench.

**Warning:** Enabling the log may delay the loading of the allocation setup page.

Missing money logs are categorized into segment rollup errors, account rollup errors, and bucket allocation errors listed in the choice list to help identify the missing amount during allocation and to categorically point out the incorrect rules and allocation issues. The segregation helps to resolve allocation and rollup issues quickly, and track how the money went missing instead of reaching its target.

Clicking the **Troubleshoot Errors/Warnings** link opens up a web page that guides you to take necessary actions with steps that you can follow to resolve each error.

-   **[View bucket contents - Legacy](../task/t_ViewBucketContents.md)**  
You can modify what you see in the list of buckets in the Bucketing stage of the IT Finance workbench.
-   **[Split buckets - Legacy](../task/t_SplitBuckets.md)**  
Buckets contain groomed general ledger expenses. These expenses can be associated with items like a cost center, vendor, department, or location.
-   **[Rollups for allocations - Legacy](c_RollupsForAllocations.md)**  
A rollup is an allocation rule that specifies how a lower-level account in the segment hierarchy connects to other accounts above it in the hierarchy. Rollups allow you to allocate expenses to the lower-level account and have expenses automatically allocated to the higher-level accounts.
-   **[Bucket assignments - Legacy](c_BucketAssignments.md)**  
Setting up an allocation means assigning the expenses in a bucket to an account in a segment or to several accounts in a segment.
-   **[Review assigned expenses - Legacy](../task/t_ReviewAssignedExpenses.md)**  
Review the expenses assigned to accounts and verify the information is correct in the Total Amount Allocated section in the right pane.
-   **[Verify the total amount allocated - Legacy](../task/t_VerifyTotalAmountAllocated.md)**  
The donut chart on the right shows the assigned expenses for all segments.
-   **[Preview an allocation from a bucket - Legacy](../task/t_PreviewAnAllocationFromABucket.md)**  
You can preview a graphical representation of how the workbench allocates the expenses in the bucket by opening the allocation viewer.
-   **[Revert bucket assignments - Legacy](../task/t_RevertBucketAssignments.md)**  
Reverting bucket assignments means taking the expenses out of the segments and accounts and leaving it in the bucket. Reverting buckets also deletes existing allocation lines for the working fiscal period that are associated with this bucket.

**Parent Topic:**[Financial Management workbench - Legacy](c_TheITFinanceWorkbench.md)

**Related topics**  


[The Data Definition stage - Legacy](c_TheDataDefinitionStage.md)

[The Data Cleansing stage - Legacy](c_TheDataCleansingStage.md)

[The Bucketing stage - Legacy](c_TheDataBucketingStage.md)

[The Allocation Review stage - Legacy](c_TheAllocationReviewStage.md)

[The Cost Models tab - Legacy](c_TheCostModelsTab.md)

[The Configuration tab - Legacy](c_TheConfigurationTab.md)

[Missing money logs factoring tips - Legacy](../reference/error-logs-troubleshooting-tips.md)

