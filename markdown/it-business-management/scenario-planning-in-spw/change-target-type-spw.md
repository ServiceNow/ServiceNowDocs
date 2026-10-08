---
title: Change the type of a target
description: Update the target type when the way you measure a target changes. The change can reset planned and actual values in target breakdowns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/change-target-type-spw.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [target type, maintain above, maintain below, maintain constant, target breakdowns]
breadcrumb: [Manage portfolio plan goals, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Change the type of a target

Update the target type when the way you measure a target changes. The change can reset planned and actual values in target breakdowns.

## Before you begin

Role required: sn\_apw\_advanced.spw\_goal\_user and either sn\_align\_core.apw\_user or sn\_gf.goal\_admin

## About this task

You can edit the **Type** field on a saved target even after actuals are recorded. When you change the type, the unit of measure that you selected stays the same.

Depending on the target, a confirmation dialog box opens before the change is applied:

-   When the target has no actuals and has a check-in frequency, the dialog box displays this message: `Changing the target type from '*previous type*' to '*current type*' will reset the planned target values for each target breakdown. Do you want to proceed?`
-   When the target has actuals, the dialog box warns that changing the type between Maximize, Minimize, and Maintain types resets planned target values and actual values in the breakdowns. Back up your actual values before proceeding.

No dialog box opens when you change between two Maintain types, for example, from **Maintain above** to **Maintain constant**, or when you change to or from **Milestone**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  Select the portfolio plan that contains the target, and then select the **Goals and targets** tab.

3.  Open the target that you want to change.

4.  In the **Type** field, select the new target type.

    For a description of each type, see [Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-types-overview.md).

5.  If a confirmation dialog box opens, select **OK** or **Yes** to keep the new type.

    To keep the previous type, select **Cancel** or **No**. The **Type** field returns to its previous value, and the breakdowns and planned values aren't changed.

6.  Select **Save**.


## Result

The planned target values of the breakdowns are recalculated for the new type. For Maintain types, each breakdown's planned target is set to the final target value. If the target had actuals, the total actual value is added to the current breakdown period, or to the latest breakdown period if no current period exists. The progress is recalculated using the new type.

