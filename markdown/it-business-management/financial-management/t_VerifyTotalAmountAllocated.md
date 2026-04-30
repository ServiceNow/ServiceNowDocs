---
title: Verify the total amount allocated - Legacy
description: The donut chart on the right shows the assigned expenses for all segments.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Allocation Setup stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Verify the total amount allocated - Legacy

The donut chart on the right shows the assigned expenses for all segments.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## About this task

By default, the calculations in both the donut chart and the segment hierarchy include data from the new rules that you created in the workbench, and any existing rules that you previously created. You can choose to turn off the pre-existing rules, called **User Rules**, so that you see only the calculations from your newly created rules.

## Procedure

1.  On the **Preview** tab, select a segment from the **Total Amount Assigned** list to view the allocation for that segment.

    The breakdown for each account appears below the donut chart.

2.  To change whether or not to refresh the information in the donut chart automatically when you make changes, click the gear icon \(![The gear icon](../image/Gear_icon_workbench.png)\) on an account to view the allocation summary, and click the **Refresh Automatically** toggle.

    ![The Preview tab](../image/Donut_chart_allocation_setup.png "The Preview tab")

3.  Click the **User Rules** tab to view the allocation rules and rollups that you manually set up outside of the workbench.

    On this tab, you can perform the following actions:

    -   Click a rule name to open the Cost Allocation Rule form for that rule.
    -   Click the preview icon \(![The preview icon](../image/Preview_icon.png)\) to preview the allocation for that rule in the allocation viewer.
    -   Click the **Show** check box to include allocation lines from existing, user-created rules in the calculations for assigned buckets. When you select this check box, the application includes existing allocation lines that are active on the accounts. The amounts that you see in the segments and in the donut chart are affected by the inclusion of these allocation lines. You shouldn’t select this option if you want the calculated values to show only what you assign from buckets.
    -   Click **See all rules** to see a list of all allocation rules in the application.

        ![The User Rules tab](../image/User_rules_tab.png "The User Rules tab")


**Parent Topic:**[Allocation Setup stage - Legacy](../concept/c_TheAllocationSetupStage.md)

**Related topics**  


[View bucket contents - Legacy](t_ViewBucketContents.md)

[Split buckets - Legacy](t_SplitBuckets.md)

[Rollups for allocations - Legacy](../concept/c_RollupsForAllocations.md)

[Bucket assignments - Legacy](../concept/c_BucketAssignments.md)

[Review assigned expenses - Legacy](t_ReviewAssignedExpenses.md)

[Preview an allocation from a bucket - Legacy](t_PreviewAnAllocationFromABucket.md)

[Revert bucket assignments - Legacy](t_RevertBucketAssignments.md)

