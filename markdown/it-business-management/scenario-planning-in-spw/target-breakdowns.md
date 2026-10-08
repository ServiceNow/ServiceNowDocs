---
title: Target breakdowns in Strategic Planning
description: Breaking down a target into smaller periods \(for example, Monthly\) helps you set a target value for each month and focus on that specific monthly target. The target breakdowns are automatically created based on the Check-in frequency and Target value distribution set for the target.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/target-breakdowns.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 7
breadcrumb: [Manage portfolio plan goals, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Target breakdowns in Strategic Planning

Breaking down a target into smaller periods \(for example, Monthly\) helps you set a target value for each month and focus on that specific monthly target. The target breakdowns are automatically created based on the Check-in frequency and Target value distribution set for the target.

The check-in frequency for a target can be set to Daily, Weekly, Monthly, Quarterly, or Yearly. Based on the Check-in frequency of the target, the corresponding target breakdowns are created. For example, if the Check-in frequency is set to Monthly for a target spanning for a year, 12 monthly target breakdowns are created. Planned target values are automatically set for each target breakdown based on the Target value distribution setting of the target.

**Note:** The target breakdowns feature isn’t supported for qualitative targets.

The following examples help you understand how the target progress is calculated for targets with different target distribution type.

-   **Example 1: Acquire 1200 new customers in the calender year 2025 \(Track non-cumulatively\)**

    In this example, you want to achieve a target of acquiring 1200 new customers in the calender year 2025 and track the progress monthly \(non-cumulatively\), then you can set the target as the following:

    -   Set the start date and end dates to 2025-01-01 and 2025-12-31, respectively
    -   Set the start value and final target values to 0 and 1200, respectively
    -   Set the Check-in frequency for the target to Monthly
    -   Set the Target value distribution to Split equally across the time period \(non-cumulative\)

        This Target value distribution means that the final target value is divided into 12 equal values \(planned target value for each target breakdown\) which aggregates to the final target value. You can edit the planned target value later from the respective target breakdown record as needed.

    \[Omitted image "target-breakdowns-monthly-non-cumulative.gif"\] Alt text: Target breakdowns with monthly cumulative breakdowns.

    In this case, the application creates 12 target breakdowns \(January, February,………, and December\) for calender year 2025 and sets the Planned target value for each target breakdown to 100 \(Final target value divided by the number of target breakdowns\).

    Because the application sums up the actual value entered in each monthly target breakdown, you must enter the actual value that is achieved in the particular month for the target breakdown. For example, you acquired 100 customers in January, then enter 100 as the actual value in the January target breakdown. And, you acquired another 100 customers in February, then enter 100 as the actual value in the February target breakdown. Similarly, if you acquired another 100 in March and 100 in April, then enter 100 as the actual value in both the March and April target breakdowns.

    The application sums up the actual values entered in each monthly target breakdown and rolls up the sum value to the actual value of the main target. Then, the progress of the target and its goal are auto-updated.

-   **Example 2: Acquire 1200 new customers in the calender year 2025 \(Track cumulatively\)**

    In this example, you want to achieve a target of acquiring 1200 new customers in the calender year 2025 and track the progress monthly \(cumulatively\), then you can set the target as the following:

    -   Set the start date and end dates to 2025-01-01 and 2025-12-31, respectively
    -   Set the start value and final target values to 0 and 100, respectively
    -   Set the Check-in frequency for the target to Monthly
    -   Set the Target value distribution to Spread linearly across the time period \(cumulative\)

        This Target value distribution means that the final target value is divided linearly into 12 planned target values \(such a way that the value for the last monthly breakdown is equal to the final target value\). You can edit the planned target value later from the respective target breakdown record as needed.

    \[Omitted image "target-breakdowns-monthly-cumulative.gif"\] Alt text: Target breakdowns with monthly non-cumulative breakdowns

    In this case, the application creates 12 target breakdowns \(January, February,………, and December\) for calender year 2025 and sets the Planned target value for the January, February,………, and December breakdowns to 100, 200,…….., and 1200 respectively.

    Because the application considers only the actual value entered in the latest monthly target breakdown, you must enter the cumulative actual value in the latest monthly target breakdown. For example, you acquired 100 customers in January, then enter 100 as the actual value in the January target breakdown. And, you acquired another 100 customers in February, then enter 200 as the actual value in the February target breakdown. Similarly, if you acquired another 100 in March and 100 in April, then enter 300 and 400 as the actual value in the March and April target breakdowns, respectively.

    The application considers the actual value entered in the latest monthly target breakdown and rolls up to the actual value of the main target. Then, the progress of the target and its goal are auto-updated.


## Target breakdowns for Maintain type targets

When the **Type** field of a target is set to **Maintain above**, **Maintain below**, or **Maintain constant**, the planned target of every target breakdown, at every level, is set to the final target value. If the final target value is empty, the planned targets are set to 0. You can edit the planned target of a breakdown later. The **Target value distribution** field doesn't apply to Maintain types.

For example, if you set a Maintain above target of 75 with a quarterly check-in frequency for 2026, four quarterly breakdowns are created, each with a planned target of 75.

Enter the actual value that you measured in each breakdown period. The **Actuals to date** value of the target shows the actual value of the latest breakdown period that has an actual. Parent breakdowns, such as a year above its quarters, also take the actual value of their latest child breakdown.

When you change a Maintain-type target, its breakdowns are updated as follows:

-   Start date moved later or end date moved earlier: the breakdowns that fall outside the new date range are removed. The remaining breakdowns keep their planned targets and actuals.
-   Start date moved earlier or end date moved later: breakdowns are added for the new periods, with the planned target set to the final target value and no actual value.
-   Final target value changed: the planned target of every breakdown is updated to the new final target value, and the status and progress are recalculated.
-   Check-in frequency changed: the breakdowns are regenerated for the new frequency. Where the old and new breakdowns share a period, such as the same month or quarter, the latest actual value and status from that period are copied to the new breakdowns.

For how progress is calculated from the breakdowns, see [Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-types-overview.md). To change the type of a target that already has breakdowns, see [Change the type of a target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/change-target-type-spw.md).

## Graphical visualisation of target progress

The **Progress** tab in the target’s side panel provides graphical visualization for the trend of the target progress based on the planned target value and the actual value of the breakdowns. You can also edit the planned target and view the check-in history of the target actuals from the **Progress** tab.

\[Omitted image "trend-of-a-target-spw.gif"\] Alt text: Graphical visualisation of target progress.

## Benefits of target breakdowns

The target breakdowns feature helps you when you want to set a target for a period but want to track the progress of the target in smaller periods such as daily, weekly, monthly, quarterly, and yearly. For example, you have set a target for a year with start value and final target values of 0 and 1200, respectively. Also, you want to set monthly targets of 100 for each quarter. In this case, you can break down the target into monthly targets and set a target value for each month so that you can focus on the specific monthly target and update your actuals against those monthly targets.

The target breakdowns feature has the following benefits:

-   Break down the long-term targets into short-term intervals such as Daily, Weekly, Monthly, Quarterly, and Yearly for a better tracking or reporting of your progress
-   Set or modify a planned target value for each target breakdown as needed
-   Update the actual value for each target breakdown and track the progress of the main target
-   Focus on the specific short-term target \(target breakdown\) rather than the whole target
-   Track the progress of your short-term and long-term targets cumulatively or non-cumulatively
-   Visualize the trend of the target's process wrt the planned target in the line or bar chart

## How the actual value is calculated when the check-in frequency set to None

When the check-in frequency is set to None for a target, the actual value must be entered in the **Actuals to date** field in the main target record. The actual value entered must be cumulative irrespective of the time period of the target. Target breakdowns aren’t created when the check-in frequency is set to None.

## Target breakdowns in target automation

If you’ve enabled the target automation feature for a target and set the check-in frequency and Target value distribution, the target automation feature automatically updates the actual value in the respective target breakdown based on the check-in due date. After the actual value of a target breakdown is updated, the value is rolled up to rolls up to the actual value of the main target. Then, the progress of the target and its goal are auto-updated.

