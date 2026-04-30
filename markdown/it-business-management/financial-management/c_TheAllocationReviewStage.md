---
title: The Allocation Review stage
description: The Allocation Review stage allows you to review the allocation setup before you process the allocations.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Financial Management workbench, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# The Allocation Review stage

The Allocation Review stage allows you to review the allocation setup before you process the allocations.

## Allocation Setup Review

On the Review page, these summaries are available:

-   **Bucketing**: The percentage of expenses that are assigned to buckets on the Bucketing stage.
-   **Allocation Setup**: The percentage of buckets that are assigned to accounts in the segment hierarchy on the Allocation Setup stage.
-   **Others**: Detailed allocation information, such as the expense amounts that are to be allocated to segments, the amount that was cleansed in the data cleansing stage, and the amounts in the unassigned buckets and assigned buckets.

![Reviewing an allocation setup](../image/Allocation_review.png "Reviewing an allocation setup")

## Allocation

You can trigger allocation runs for multiple cost models for various fiscal periods concurrently by queuing the allocation jobs to the allocation engine. This also allows multiple users on the same instance to queue their requested allocation runs. When the allocation engine has completed an allocation run, a confirmation message appears.

-   The engine automatically picks up the next job in queue after the current job is complete.
-   You can queue any number of allocation jobs for multiple cost models and fiscal periods.
-   You can cancel a job \(stop the engine\) when the job is in progress thereby saving the engine runtime for the next job in queue.
-   You can also dequeue a job from the jobs that are in queue by removing it from the queue, if you do not want to run it.

With this enhancement, you can view the last run details of the cost model and its breakdown details with links to allocations and unit costs.

-   **View on Cost Analysis**: View the cost lines for analysis.
-   **View Expense Lines**: \(For customers upgrading from a previous version to Xanadu\) If you had enabled the **Generate GL Expense Lines** check box in the Financial Model form for the existing cost models, then you can view the GL expense lines of the cost model after the allocation engine is run. The GL expense lines will not be generated for the cost models you create after upgrading to Xanadu.

    **Important:** This feature is only available to customers who own an ITBM Analyst license.

-   **View Cost Lines**: View the cost allocation aggregates.
-   **View Cost Line Breakdowns**: The cost allocation breakdown aggregates for the cost model. If **Run On Demand Only** flag is set to true, then the allocation engine does not generate breakdown lines. To explicitly generate the breakdown lines, [generate breakdown allocations](../task/t_CreateBreakdownRelationship.md#generate-breakdown-relation) in the **Breakdown Relationships** related list of the Financial Model form.
-   **View Unit Costs**: View the unit costs.

You can also view the details of the current cost model that is in progress and the total number of allocation jobs in queue. Also, view the current job progress with the status of the current allocation run and its details.

View Cost Tree: View all the segment accounts contributing to the selected account in a hierarchical view. You can further drill, on each segment account, down in the hierarchy.

1.  Click **View Cost Tree**.
2.  Select a segment in the **Segment** choice list.
3.  Select an account from the **Account** choice list.
4.  Click **Go**.

-   **[Allocate expenses with the workbench](../task/t_AllocateExpensesWithTheWorkbench.md)**  
If any of this information looks incorrect, go back to a previous stage and make the necessary modifications.

**Parent Topic:**[Financial Management workbench](c_TheITFinanceWorkbench.md)

**Related topics**  


[The Data Definition stage](c_TheDataDefinitionStage.md)

[The Data Cleansing stage](c_TheDataCleansingStage.md)

[The Bucketing stage](c_TheDataBucketingStage.md)

[Allocation Setup stage](c_TheAllocationSetupStage.md)

[The Cost Models tab](c_TheCostModelsTab.md)

[The Configuration tab](c_TheConfigurationTab.md)

[Missing money logs factoring tips](../reference/error-logs-troubleshooting-tips.md)

