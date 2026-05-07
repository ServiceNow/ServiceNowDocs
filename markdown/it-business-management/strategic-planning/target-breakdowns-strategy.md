---
title: Target breakdowns
description: Breaking down a target into smaller periods \(for example, Monthly\) helps you set a target value for each month and focus on that specific monthly target. The target breakdowns are automatically created based on the Check-in frequency and Target value distribution set for the target.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 6
breadcrumb: [Manage enterprise goals, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Target breakdowns

Breaking down a target into smaller periods \(for example, Monthly\) helps you set a target value for each month and focus on that specific monthly target. The target breakdowns are automatically created based on the Check-in frequency and Target value distribution set for the target.

The check-in frequency for a target can be set to Daily, Weekly, Monthly, Quarterly, or Yearly. Based on the Check-in frequency of the target, the corresponding target breakdowns are created. For example, if the Check-in frequency is set to Monthly for a target spanning for a year, 12 monthly target breakdowns are created. Planned target values are automatically set for each target breakdown based on the Target value distribution setting of the target.

**Note:** The target breakdowns feature isn’t supported for qualitative targets.

The following examples help you understand how the target progress is calculated for targets with different target distribution type.

-   **Example 1: Acquire 1200 new customers in the calender year 2026 \(Track non-cumulatively\)**

    In this example, you want to achieve a target of acquiring 1200 new customers in the calender year 2026 and track the progress monthly \(non-cumulatively\), then you can set the target as the following:

    -   Set the start date and end dates to 2026-01-01 and 2026-12-31, respectively
    -   Set the start value and final target values to 0 and 1200, respectively
    -   Set the Check-in frequency for the target to Monthly
    -   Set the Target value distribution to Split equally across the time period \(non-cumulative\)

        This Target value distribution means that the final target value is divided into 12 equal values \(planned target value for each target breakdown\) which aggregates to the final target value. You can edit the planned target value later from the respective target breakdown record as needed.

    ![Target breakdowns with monthly cumulative breakdowns.](../image/target-breakdowns-monthly-cumulative-strategy.gif)

    In this case, the application creates 12 target breakdowns \(January, February,………, and December\) for calender year 2026 and sets the Planned target value for each target breakdown to 100 \(Final target value divided by the number of target breakdowns\).

    Because the application sums up the actual value entered in each monthly target breakdown, you must enter the actual value that is achieved in the particular month for the target breakdown. For example, you acquired 100 customers in January, then enter 100 as the actual value in the January target breakdown. And, you acquired another 100 customers in February, then enter 100 as the actual value in the February target breakdown. Similarly, if you acquired another 100 in March and 100 in April, then enter 100 as the actual value in both the March and April target breakdowns.

    The application sums up the actual values entered in each monthly target breakdown and rolls up the sum value to the actual value of the main target. Then, the progress of the target and its goal are auto-updated.

-   **Example 2: Acquire 1200 new customers in the calender year 2026 \(Track cumulatively\)**

    In this example, you want to achieve a target of acquiring 1200 new customers in the calender year 2026 and track the progress monthly \(cumulatively\), then you can set the target as the following:

    -   Set the start date and end dates to 2026-01-01 and 2026-12-31, respectively
    -   Set the start value and final target values to 0 and 100, respectively
    -   Set the Check-in frequency for the target to Monthly
    -   Set the Target value distribution to Spread linearly across the time period \(cumulative\)

        This Target value distribution means that the final target value is divided linearly into 12 planned target values \(such a way that the value for the last monthly breakdown is equal to the final target value\). You can edit the planned target value later from the respective target breakdown record as needed.

    ![Target breakdowns with monthly non-cumulative breakdowns](../image/target-breakdowns-monthly-cumulative-strategy.gif)

    In this case, the application creates 12 target breakdowns \(January, February,………, and December\) for calender year 2026 and sets the Planned target value for the January, February,………, and December breakdowns to 100, 200,…….., and 1200 respectively.

    Because the application considers only the actual value entered in the latest monthly target breakdown, you must enter the cumulative actual value in the latest monthly target breakdown. For example, you acquired 100 customers in January, then enter 100 as the actual value in the January target breakdown. And, you acquired another 100 customers in February, then enter 200 as the actual value in the February target breakdown. Similarly, if you acquired another 100 in March and 100 in April, then enter 300 and 400 as the actual value in the March and April target breakdowns, respectively.

    The application considers the actual value entered in the latest monthly target breakdown and rolls up to the actual value of the main target. Then, the progress of the target and its goal are auto-updated.


## Graphical visualisation of target progress

The **Overview** tab in the target’s record page provides graphical visualization for the trend of the target progress based on the planned target value and the actual value of the breakdowns. You can also edit the planned target and view the check-in history of the target actuals selecting the **Show check-in history** in the **Actuals check-in information** section.

![Graphical visualisation of target progress.](../image/trend-of-a-target-strategy.gif)

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

