---
title: Analytics Time sheet
description: The Analytics Time sheet provides comprehensive time sheet activities and reports to the time card approvers and time card users. The dashboard uses Performance Analytics to provide a trend of historical data and regular reports. It gives an overview of the time sheet activities of resources, time sheet approval and rejection rate, over-allocated and under-allocated resource counts.
locale: en-US
release: yokohama
product: PPM Collaboration
classification: ppm-collaboration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Analytics and reporting, Project Portfolio Management, Strategic Portfolio Management]
---

# Analytics Time sheet

The Analytics Time sheet provides comprehensive time sheet activities and reports to the time card approvers and time card users. The dashboard uses Performance Analytics to provide a trend of historical data and regular reports. It gives an overview of the time sheet activities of resources, time sheet approval and rejection rate, over-allocated and under-allocated resource counts.

**Important:** Starting with Yokohama release, **Time Sheet Dashboard** is renamed to **Analytics Time sheet** for new customers.

![Screenshot for Overview tab of Analytics Time sheet](../image/time-sheet-dashboard-overviewtab.png "Overview tab")

![Screenshot for Delinquent Activity tab of Analytics Time sheet](../image/time-sheet-dashboard-delinquenttab.png "Delinquent Activity tab")

![Screenshot for Analysis tab of Analytics Time sheet](../image/time-sheet-dashboard-analysistab.png "Analysis tab")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Portfolio manager: Needs visibility into time sheet activities of resources and actions that should be taken.|it\_portfolio\_manager|
|Program manager: Needs visibility into time sheet activities of resources and actions that should be taken.|it\_program\_manager|
|Project manager: Has access to the dashboards.|it\_project\_manager|
|Time card approver: Needs visibility into time sheet activities of resources and actions that should be taken.|timecard\_approver|
|Business stakeholder for PPM: Needs visibility into time sheet activities of resources and actions that should be taken.|sn\_ppm\_read|

## Indicators

The Overview, Delinquent Activity, and Analysis tabs in the dashboard contain widgets with the following indicators. The data for time sheets and time cards is collected from the \[time\_sheet\] table and the data for users is collected from the \[users\] table.

-   **PPM – Active Time Sheet Users**

    Count of active users with the timecard\_user role.

-   **PPM – % Late This Year**

    Percentage of time sheets late this year.

-   **PPM – % Late This Week**

    Percentage of time sheets late this week.

-   **PPM – % Late This Quarter**

    Percentage of time sheets late this quarter.

-   **PPM – % Late This Month**

    Percentage of time sheets late this month.

-   **PPM – Late Time Sheets This Month**

    Count of late time sheets this month. The indicator includes time sheets of the current month until the past week that are not in the Approved or Processed state.

-   **PPM – Late Time Sheets This Quarter**

    Count of late time sheets this quarter. The indicator includes time sheets of the current quarter until the past week that are not in the Approved or Processed state.

-   **PPM – Late Time Sheets This Week**

    Count of late time sheets this week. The indicator includes time sheet of the past week that are not in the Approved or Processed state.

-   **PPM – Late Time Sheets This Year**

    Count of late time sheets this year. The indicator includes time sheets of the current year until the past week that are not in the Approved or Processed state.

-   **PPM – Total Time Sheets Last Week**

    Total number of time sheets for the past week.

-   **PPM – Total Time Sheets This Month**

    Total number of time sheets for the weeks in the current month.

-   **PPM – Total Time Sheets This Quarter**

    Total number of time sheets for the weeks in the current quarter.

-   **PPM – Total Time Sheets This Year**

    Total number of time sheets for the weeks in the current year.

-   **PPM – Time Sheets Approved This Week**

    Count of time sheets approved this week. The indicator includes time sheets in the Approved or Processed state.

-   **PPM – Time Sheets Missing This Week**

    Count of users with the timecard\_user role who did not submit time sheet for the current week.

-   **PPM – Time Sheets Pending This Week**

    Count of time sheets pending this week. The indicator includes time sheets for the current week in the Pending state.

-   **PPM – Time Sheets Recalled This Week**

    Count of time sheets recalled this week. The indicator includes time sheets for the current week in the Recalled state.

-   **PPM – Time Sheets Rejected This Week**

    Count of time sheets rejected this week. The indicator includes time sheets for the current week in the Rejected state.

-   **PPM – Time Sheets Submitted This Week**

    Count of time sheets submitted this week. The indicator includes time sheets for the current week in the Submitted state.


## Breakdowns

-   User
-   Manager
-   Department
-   Cost Center
-   Portfolio
-   Program
-   Project

## Data visualizations

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rejected

</td><td>

Single score ![Single-score chart](../../performance-analytics/image/single-score.png)

</td><td>

Number of time cards that are in the Rejected state for the last 30 days.

</td></tr><tr><td>

Late

</td><td>

Single score ![Single-score chart](../../performance-analytics/image/single-score.png)

</td><td>

Number of time cards that were submitted late in the last 30 days.

</td></tr><tr><td>

Pending Approvals

</td><td>

Single score ![Single-score chart](../../performance-analytics/image/single-score.png)

</td><td>

Number of time cards that have approval pending in the last 30 days.

</td></tr><tr><td>

By State

</td><td>

Bar chart ![Bar chart](../../performance-analytics/image/column-icon.png)

</td><td>

Number of time cards in the last 30 days, grouped by their state.

</td></tr><tr><td>

By Category

</td><td>

Heat map ![Heat map chart](../../performance-analytics/image/heatmap.png)

</td><td>

Breakdown of time spent \(hours\) by a resource across different project time categories in the last 30 days.

</td></tr><tr><td>

By Resource

</td><td>

List ![List chart](../../performance-analytics/image/scorecard-icon.png)

</td><td>

The list of time cards submitted by a resource in 30 days.

</td></tr><tr><td>

Total Hours

</td><td>

Bar chart ![Bar chart](../../performance-analytics/image/column-icon.png)

</td><td>

Total time \(hours\) spent on by different categories.

</td></tr><tr><td>

Total Hours by Week Starts On

</td><td>

Time series line ![time series line chart](../../performance-analytics/image/line-ts-icon.png)

</td><td>

Weekly trend of the total time \(hours\) spent on different categories over a period of time.

</td></tr><tr><td>

Time Sheets Over 40 Hours

</td><td>

Bar chart ![Bar chart](../../performance-analytics/image/column-icon.png)

</td><td>

Count of time sheets over 40 hours indicating over-allocated resources.This report does not refresh when you select portfolio, program, or project.

</td></tr><tr><td>

Allocated vs Actual Hours

</td><td>

Time series step ![Time series step chart](../../performance-analytics/image/step-ts-icon.png)

</td><td>

Monthly trend comparing the total allocated hours versus actual hours for all time card users.

</td></tr><tr><td>

Time Cards By Expense Type

</td><td>

Bar chart ![Bar chart](../../performance-analytics/image/column-icon.png)

</td><td>

Time cards grouped by expense types: Capital Expense \(Capex\) and Operating Expense \(Opex\).

</td></tr></tbody>
</table>**Parent Topic:**[Project Portfolio Management Platform Analytics Solutions](project-portfolio-content-pack.md)

