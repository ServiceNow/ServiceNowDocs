---
title: Legacy: Problem Premium dashboard
description: This dashboard uses advanced features such as interactive filters and workbench widgets to provide a broad view of problem reports, both current and over time.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Legacy: Problem Management Platform Analytics Solutions, Problem Management, IT Service Management]
---

# Legacy: Problem Premium dashboard

This dashboard uses advanced features such as interactive filters and workbench widgets to provide a broad view of problem reports, both current and over time.

**Important:**

Starting in Xanadu release, the Problem premium dashboard is deprecated. Users can use [Problem dashboard](performance-analytics/problem.md) to view, and track the open problems.

![Process by Age tab](../image/problem-premium-process-age.png "Process by Age tab")

![Problem premium dashboard overview tab](../image/problem-premium-overview.png "Overview tab")

**Note:** The Overview tab has the same contents as the Problem Overview dashboard.

![Problem Premium dashboard Data Quality tab](../image/problem-premium-data-quality.png "Data Quality tab")

![Process KPIs for Problem Premium dashboard](../image/problem-premium-kpis.png "Process KPIs tab")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|All roles concerned with Problem Management|itil to see the list of Problem records|

## Indicators

-   **Number of open problems**

    Problems on the Problem \[problem\] table created on or before today and with no Closed date. This indicator is used in several other indicators on the dashboard.

-   **Number of closed problems**

    Problems on the Problem \[problem\] table closed today. This indicator is used in several other indicators on the dashboard.

-   **Average age of open problems**

    The score for this indicator is calculated according to the formula \[\[Summed age of open problems\]\] / \[\[Number of open problems\]\] / 24

-   **Average re-assignment of open problems**

    The average number of times an open problem gets reassigned. The score for this indicator is calculated according to the formula \[\[Summed re-assignment of open problems\]\] / \[\[Number of open problems\]\].

-   **Average age of updated since of open problems**

    The average time in days since the last update of an open problem. The score for this indicator is calculated according to the formula \[\[Summed age of updated since of open problems\]\] / \[\[Number of open problems\]\] / 24.

-   **% of new critical problems**

    The score for this indicator is calculated according to the formula \( \[\[Number of new problems &gt; Priority = 1 - Critical\]\] / \[\[Number of new problems\]\] \) \* 100

-   **Average close time of problems**

    The score for this indicator is calculated according to the formula \[\[Summed duration of closed problems\]\] / \[\[Number of closed problems\]\] / 24

-   **% of problems reassigned at least once**

    The score for this indicator is calculated according to the formula \( \[\[Number of reassigned open problems\]\] / \[\[Number of open problems\]\] \* 100 \).

-   **% of problems closed on first assignment**

    The score for this indicator is calculated according to the formula \( \[\[Number of problems closed on first assignment\]\] / \[\[Number of closed problems\]\] \* 100 \).

-   **Average reassignment count of closed problems**

    The average value of the Reassignment Count field on closed problems, where Reassignment Count is not empty.

-   **% of open problems classified as known error**

    The score for this indicator is calculated according to the formula \( \[\[Number of open problems classified as known error\]\] / \[\[Number of open problems\]\] \) \* 100.

-   **% of closed problems without any close notes**

    The score for this indicator is calculated according to the formula \( \[\[Number of closed problems without close notes\]\] / \[\[Number of closed problems\]\] \) \* 100.

-   **% of open problems with at least one incident**

    The score for this indicator is calculated according to the formula \( \[\[Number of open problems with at least one incident\]\] / \[\[Number of open problems\]\] \) \* 100.


The following indicators are not shown directly on the dashboard but are used in calculating formulas:

-   Summed age of open problems
-   Summed age of updated since of open problems
-   Summed duration of closed problems
-   Summed re-assignment of open problems
-   Number of reassigned open problems
-   Number of problems closed on first assignment
-   Number of open problems classified as known error
-   Number of closed problems without close notes
-   Number of open problems with at least one incident

## Breakdowns

-   Age
-   Priority
-   State
-   Assignment Group

## Data visualizations

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Critical open problems

</td><td>

Single Score ![single score icon](../../performance-analytics/image/single-score.png)

</td><td>

All open problems where Priority is 1 - Critical. This report tells you at a glance how many top priority problems there are.

</td></tr><tr><td>

Unassigned problems

</td><td>

Single Score ![single score icon](../../performance-analytics/image/single-score.png)

</td><td>

All open problems where 'Assigned to' is empty. These are the problems you have to assign.

</td></tr><tr><td>

Overdue problems

</td><td>

Single Score ![single score icon](../../performance-analytics/image/single-score.png)

</td><td>

All open problems where Escalation = Overdue

</td></tr><tr><td>

Open problems

</td><td>

Single Score ![single score icon](../../performance-analytics/image/single-score.png)

</td><td>

All open problems

</td></tr><tr><td>

Problems not updated for 7 days

</td><td>

Single Score ![single score icon](../../performance-analytics/image/single-score.png)

</td><td>

Open problems where the value in the Updated field is more than 7 days ago

</td></tr><tr><td>

Open problems older than 30 days

</td><td>

Single Score ![single score icon](../../performance-analytics/image/single-score.png)

</td><td>

Open problems where the value in the Created field is more than 30 days ago

</td></tr><tr><td>

Open problems - Grouped

</td><td>

Horizontal Bar ![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)

</td><td>

Open problems grouped by Priority

</td></tr><tr><td>

Open problems older than 30 days - Grouped

</td><td>

Horizontal Bar ![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)

</td><td>

Open problems where the value in the Created field is more than 30 days ago, grouped by Priority

</td></tr><tr><td>

Problems by Priority and State

</td><td>

Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Open Problems grouped on a matrix of Priority and State

</td></tr><tr><td>

Open problems older than 30 days by Priority and State

</td><td>

Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Open problems where the value in the Created field is more than 30 days ago, grouped on a matrix of Priority and State

</td></tr><tr><td>

Open problems not updated in last 30 days by assignment group

</td><td>

Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Open problems where the value in the Updated field is more than 30 days ago, grouped on a matrix of State and Assignment Group

</td></tr><tr><td>

Problems Opened per Week

</td><td>

Line![line trend icon](../../../reuse/reporting/image/line-trend.svg)

</td><td>

Count of all problems opened this year, trending by Opened per Week

</td></tr><tr><td>

Problems Closed per Week

</td><td>

Line![line trend icon](../../../reuse/reporting/image/line-trend.svg)

</td><td>

Count of all problems closed this year, trending by Closed per Week

</td></tr><tr><td>

Open Problems Where Assignee Is Not Active

</td><td>

Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Open problems where the value of Assigned to Active is false, grouped on a matrix of State and Assignment Group

</td></tr><tr><td>

Problems Pending a Change Request that is Already Closed

</td><td>

Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Open problems where the Change request has a State value of 3, meaning the request is closed, grouped on a matrix of State and Assignment Group

</td></tr></tbody>
</table>